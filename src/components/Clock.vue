<template>
  <div class="bg-white rounded-xl shadow-lg p-8 text-center relative overflow-hidden">
    <div class="absolute -top-10 -right-10 w-40 h-40 bg-blue-100 rounded-full opacity-50"></div>
    <div class="absolute -bottom-10 -left-10 w-40 h-40 bg-blue-100 rounded-full opacity-50"></div>
    
    <h2 class="text-4xl font-bold mb-6 text-blue-800 relative">现在北京时间</h2>
    
    <div class="mb-6 relative">
      <div class="text-xl mb-3 text-gray-700">{{ dateString }}</div>
      <div class="text-lg mb-5 text-gray-600 bg-blue-50 inline-block px-4 py-1 rounded-full">农历 {{ lunarDate }}</div>
    </div>
    
    <div class="flex justify-center items-center mb-8 relative">
      <div class="clock-container flex items-center">
        <div class="time-box bg-gradient-to-br from-blue-600 to-blue-700 text-white text-5xl px-5 py-3 rounded-lg shadow-md transform hover:scale-105 transition duration-300">{{ hours }}</div>
        <div class="text-4xl mx-2 text-blue-800 animate-pulse">:</div>
        <div class="time-box bg-gradient-to-br from-blue-600 to-blue-700 text-white text-5xl px-5 py-3 rounded-lg shadow-md transform hover:scale-105 transition duration-300">{{ minutes }}</div>
        <div class="text-4xl mx-2 text-blue-800 animate-pulse">:</div>
        <div class="time-box bg-gradient-to-br from-blue-600 to-blue-700 text-white text-5xl px-5 py-3 rounded-lg shadow-md transform hover:scale-105 transition duration-300">{{ seconds }}</div>
      </div>
    </div>
    
    <button @click="refresh" class="px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition duration-300 shadow-md relative font-medium">
      刷新
    </button>
    
    <div class="mt-4 text-xs text-gray-500">数据更新时间: {{ lastUpdated }}</div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

// 格式化数字为两位数
const padZero = (num) => {
  return num.toString().padStart(2, '0');
};

// 时间变量
const hours = ref('00');
const minutes = ref('00');
const seconds = ref('00');
const dateString = ref('');
const lunarDate = ref('');
const lastUpdated = ref('');

// 更新时间的函数
const updateTime = () => {
  const now = new Date();
  
  hours.value = padZero(now.getHours());
  minutes.value = padZero(now.getMinutes());
  seconds.value = padZero(now.getSeconds());
  
  // 格式化日期
  const year = now.getFullYear();
  const month = now.getMonth() + 1;
  const day = now.getDate();
  const weekdays = ['日', '一', '二', '三', '四', '五', '六'];
  const weekday = weekdays[now.getDay()];
  
  dateString.value = `${year}年${month}月${day}日 星期${weekday}`;
  
  // 更新农历（简化处理）
  const lunarYears = ['甲子', '乙丑', '丙寅', '丁卯', '戊辰', '己巳', '庚午', '辛未', '壬申', '癸酉',
                      '甲戌', '乙亥', '丙子', '丁丑', '戊寅', '己卯', '庚辰', '辛巳', '壬午', '癸未'];
  const lunarIndex = (year - 1924) % 60;
  const lunarYear = lunarYears[lunarIndex];
  
  // 简化的农历月份和日期（仅作展示用）
  const lunarMonths = ['正', '二', '三', '四', '五', '六', '七', '八', '九', '十', '冬', '腊'];
  const lunarDays = ['初一', '初二', '初三', '初四', '初五', '初六', '初七', '初八', '初九', '初十',
                     '十一', '十二', '十三', '十四', '十五', '十六', '十七', '十八', '十九', '二十',
                     '廿一', '廿二', '廿三', '廿四', '廿五', '廿六', '廿七', '廿八', '廿九', '三十'];
  
  // 使用日期的数值来模拟农历日期（非实际转换）
  const lunarMonth = lunarMonths[(month - 1) % 12];
  const lunarDay = lunarDays[(day - 1) % 30];
  
  lunarDate.value = `${lunarYear}年${lunarMonth}月${lunarDay}`;
  
  // 更新最后更新时间
  lastUpdated.value = `${hours.value}:${minutes.value}:${seconds.value}`;
};

// 刷新时间
const refresh = () => {
  updateTime();
};

// 定时器引用
let timer = null;

// 组件挂载时设置定时器
onMounted(() => {
  updateTime();
  timer = setInterval(updateTime, 1000);
});

// 组件卸载时清除定时器
onUnmounted(() => {
  if (timer) {
    clearInterval(timer);
  }
});
</script>

<style scoped>
.time-box {
  min-width: 100px;
  text-align: center;
}

@keyframes pulse-shadow {
  0% {
    box-shadow: 0 0 0 0 rgba(59, 130, 246, 0.5);
  }
  70% {
    box-shadow: 0 0 0 10px rgba(59, 130, 246, 0);
  }
  100% {
    box-shadow: 0 0 0 0 rgba(59, 130, 246, 0);
  }
}

.time-box {
  animation: pulse-shadow 2s infinite;
}
</style> 