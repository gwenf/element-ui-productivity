<template>
  <div id="app">
    <TopNav />
    <el-main>
      <router-view />
    </el-main>
  </div>
</template>

<script>
import TopNav from './components/TopNav.vue'

export default {
  name: 'app',
  components: {
    TopNav
  }
}
</script>

<style>
#app {
  font-family: 'Open Sans', sans-serif;
}
</style>
