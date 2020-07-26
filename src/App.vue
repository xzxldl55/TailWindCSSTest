<template>
  <div id="app" class="h-full">
    <loginTailWind msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import loginTailWind from './components/loginTailWind.vue'

export default {
  name: 'App',
  components: {
    loginTailWind
  }
}
</script>
