<template>
  <div class="flex items-center justify-center h-full">
    <!-- 中屏以上最大宽度设限 -->
    <div class="flex max-w-sm md:max-w-4xl">
      <!-- 中屏以上form宽度1/2，小屏则自动继承父级（flex+下面的image隐藏了） -->
      <div class="bg-white md:w-1/2 p-8">
        <h1 class="text-gray-700 text-3xl mb-4">登录</h1>
        <form action="" class="text-gray-600">
          <div class="my-3">
            <input type="email" placeholder="Email" class="border rounded w-full py-2 px-4 outline-none">
          </div>
          <div class="my-3">
            <input type="password" placeholder="Password" class="border rounded w-full py-2 px-4 outline-none">
          </div>
          <div class="my-3 flex justify-between">
            <label>
              <input type="checkbox">
              Remember me
            </label>
            <a href="" class="text-blue-500">forgot email or password?</a>
          </div>
          <div class="my-3 flex">
            <button class="border rounded w-1/2 py-2">注册</button>
            <button class="border rounded w-1/2 py-2 border-blue-700 bg-blue-600 text-white ml-1">登录</button>
          </div>
          <div class="my-3 text-xs text-center mt-8 text-gray-600">
            &copy;2020.......
          </div>
        </form>
      </div>
      <!-- 小屏隐藏，中屏级以上1/2宽度 -->
      <div class="hidden md:block w-1/2 relative">
        <div class="absolute bottom-0 right-0 text-xs text-gray-400 m-4">Image By tuwanjun</div>
        <img src="../assets/hs.jpg" alt="" class="w-full h-full object-cover">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'loginTailWind',
  props: {
    msg: String
  }
}
</script> 
