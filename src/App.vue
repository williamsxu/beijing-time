<script setup>
import Clock from './components/Clock.vue'
</script>

<template>
  <div class="min-h-screen bg-gray-100">
    <header class="bg-blue-700 text-white p-4">
      <div class="container mx-auto">
        <h1 class="text-2xl font-bold text-center">北京时间</h1>
        <h2 class="text-lg text-center mt-1">在线标准北京时间校准</h2>
        <nav class="mt-4 flex justify-center space-x-6">
          <a href="#" class="hover:underline">首页</a>
          <a href="#" class="hover:underline">时间万年历</a>
          <a href="#" class="hover:underline">世界时间</a>
        </nav>
      </div>
    </header>

    <main class="container mx-auto py-8 px-4">
      <Clock />
      
      <div class="mt-8 bg-white rounded-lg shadow-md p-6">
        <h3 class="text-xl font-bold mb-4">关于北京时间</h3>
        <div class="mb-2">
          <span class="font-bold">地区：</span>中国 北京 Beijing
        </div>
        <div class="mb-4">
          <span class="font-bold">时区：</span>UTC/GMT +8.00 (东八区)
        </div>
        <p class="mb-2">北京时间又称中国标准时间。</p>
        <p class="mb-2">比格林威治时间(Greenwich Mean Time简称GMT)早8小时。</p>
        <p class="mb-2">北京时间是由位于陕西西安的中国国家授时中心计算得出。</p>
        <p>由于网络传输原因，现在北京时间校对显示时钟秒钟有毫秒级误差（桌面时钟）；点击这里进入旧版中国时间，此版本秒级闹钟可选择自选音乐作为闹铃；点击日历可写入不同日期日程安排和查询农历。</p>
      </div>

      <div class="mt-8 bg-white rounded-lg shadow-md p-6">
        <h3 class="text-xl font-bold mb-4">时间工具</h3>
        <div class="flex flex-wrap gap-2">
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">日期计算器</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">倒计时</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">闹钟</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">农历转换</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">黄历</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">时间戳</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">时间相关</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">生辰八字</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">时区</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">预产期</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">排卵期</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">时辰对照表</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">二十四节气表</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">活了多久</a>
        </div>
      </div>

      <div class="mt-8 bg-white rounded-lg shadow-md p-6">
        <h3 class="text-xl font-bold mb-4">世界国家时间热门查询</h3>
        <div class="flex flex-wrap gap-2">
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">美国时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">英国时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">加拿大时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">德国时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">法国时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">澳大利亚时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">日本时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">韩国时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">俄罗斯时间</a>
          <a href="#" class="px-3 py-1 bg-gray-200 rounded-full hover:bg-gray-300">印度时间</a>
        </div>
      </div>
    </main>

    <footer class="bg-gray-800 text-white p-6 mt-8">
      <div class="container mx-auto">
        <div class="text-center">
          <p class="mb-2">友情链接：標準時間 time in china 日本時間 金价 BMI 汇率 新华字典</p>
          <p class="mb-2">自2008年起，北京时间网标准时间对时时钟服务至现在</p>
          <p class="mb-2">© 2024 www.beijing-time.org</p>
          <p>京ICP备15019818号-2</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
