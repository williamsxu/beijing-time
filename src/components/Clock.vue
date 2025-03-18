<template>
  <div class="bg-white rounded-lg shadow-md p-6 text-center">
    <h2 class="text-3xl font-bold mb-4">现在北京时间</h2>
    <div class="mb-4">
      <div class="text-lg mb-2">{{ dateString }}</div>
      <div class="text-lg mb-4">农历 {{ lunarDate }}</div>
    </div>
    <div class="flex justify-center mb-6">
      <div class="clock-container flex items-center gap-1">
        <div class="time-box bg-blue-600 text-white text-4xl px-4 py-2 rounded">{{ hours }}</div>
        <div class="text-4xl">:</div>
        <div class="time-box bg-blue-600 text-white text-4xl px-4 py-2 rounded">{{ minutes }}</div>
        <div class="text-4xl">:</div>
        <div class="time-box bg-blue-600 text-white text-4xl px-4 py-2 rounded">{{ seconds }}</div>
      </div>
    </div>
    <button @click="refresh" class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600">刷新</button>
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
  
  // 这里简化处理农历，实际应用中应该使用专门的农历转换库
  lunarDate.value = '癸卯年二月初八';
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
  min-width: 70px;
  text-align: center;
}
</style> 