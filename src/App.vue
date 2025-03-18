<script setup>
import Clock from './components/Clock.vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-b from-blue-50 to-white">
    <header class="bg-gradient-to-r from-blue-700 to-blue-600 text-white p-6 shadow-lg">
      <div class="container mx-auto">
        <h1 class="text-3xl font-bold text-center">北京时间</h1>
        <h2 class="text-xl text-center mt-2 text-blue-100">在线标准北京时间校准</h2>
        <nav class="mt-6 flex justify-center space-x-10">
          <a href="#" class="hover:text-blue-200 transition duration-200 font-medium text-lg">首页</a>
          <a href="#" class="hover:text-blue-200 transition duration-200 font-medium text-lg">时间万年历</a>
          <a href="#" class="hover:text-blue-200 transition duration-200 font-medium text-lg">世界时间</a>
        </nav>
      </div>
    </header>

    <main class="container mx-auto py-10 px-4">
      <Clock />
      
      <div class="mt-10 bg-white rounded-xl shadow-md p-8 transition duration-300 hover:shadow-lg">
        <h3 class="text-2xl font-bold mb-6 text-blue-700 border-b pb-2 border-blue-100">关于北京时间</h3>
        <div class="mb-3 flex items-center">
          <span class="font-bold text-gray-700 w-20">地区：</span>
          <span class="text-gray-800">中国 北京 Beijing</span>
        </div>
        <div class="mb-5 flex items-center">
          <span class="font-bold text-gray-700 w-20">时区：</span>
          <span class="text-gray-800">UTC/GMT +8.00 (东八区)</span>
        </div>
        <p class="mb-3 text-gray-700 leading-relaxed">北京时间又称中国标准时间。</p>
        <p class="mb-3 text-gray-700 leading-relaxed">比格林威治时间(Greenwich Mean Time简称GMT)早8小时。</p>
        <p class="mb-3 text-gray-700 leading-relaxed">北京时间是由位于陕西西安的中国国家授时中心计算得出。</p>
        <p class="text-gray-700 leading-relaxed">由于网络传输原因，现在北京时间校对显示时钟秒钟有毫秒级误差（桌面时钟）；<a href="#" class="text-blue-600 hover:text-blue-800 underline">点击这里</a>进入旧版中国时间，此版本秒级闹钟可选择自选音乐作为闹铃；<a href="#" class="text-blue-600 hover:text-blue-800 underline">点击日历</a>可写入不同日期日程安排和查询农历。</p>
      </div>

      <div class="mt-10 bg-white rounded-xl shadow-md p-8 transition duration-300 hover:shadow-lg">
        <h3 class="text-2xl font-bold mb-6 text-blue-700 border-b pb-2 border-blue-100">时间工具</h3>
        <div class="flex flex-wrap gap-3">
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">日期计算器</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">倒计时</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">闹钟</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">农历转换</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">黄历</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">时间戳</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">时间相关</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">生辰八字</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">时区</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">预产期</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">排卵期</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">时辰对照表</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">二十四节气表</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">活了多久</a>
        </div>
      </div>

      <div class="mt-10 bg-white rounded-xl shadow-md p-8 transition duration-300 hover:shadow-lg mb-10">
        <h3 class="text-2xl font-bold mb-6 text-blue-700 border-b pb-2 border-blue-100">世界国家时间热门查询</h3>
        <div class="flex flex-wrap gap-3">
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">美国时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">英国时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">加拿大时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">德国时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">法国时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">澳大利亚时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">日本时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">韩国时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">俄罗斯时间</a>
          <a href="#" class="px-4 py-2 bg-blue-50 rounded-lg hover:bg-blue-100 transition duration-200 text-blue-700">印度时间</a>
        </div>
      </div>
    </main>

    <footer class="bg-gradient-to-r from-gray-800 to-gray-900 text-white p-8">
      <div class="container mx-auto">
        <div class="text-center">
          <p class="mb-3 text-gray-300">友情链接：
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">標準時間</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">time in china</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">日本時間</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">金价</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">BMI</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">汇率</a>
            <a href="#" class="text-blue-300 hover:text-blue-200 mx-1">新华字典</a>
          </p>
          <p class="mb-3 text-gray-400">自2008年起，北京时间网标准时间对时时钟服务至现在</p>
          <p class="mb-3 text-gray-300">© 2024 www.beijing-time.org</p>
          <p class="text-gray-400 text-sm">京ICP备15019818号-2</p>
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
