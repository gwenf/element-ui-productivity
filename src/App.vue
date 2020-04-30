<template>
  <div id="app">
    <TopNav :openDrawer="openDrawer" />
    <el-main>
      <router-view />
    </el-main>
    <el-drawer
      :visible.sync="drawer"
      :with-header="false">
      <span>Hi there!</span>
    </el-drawer>
  </div>
</template>

<script>
import TopNav from './components/TopNav.vue'

export default {
  name: 'app',
  components: {
    TopNav
  },
  data() {
    return {
      drawer: false
    }
  },
  methods: {
    openDrawer() {
      this.drawer = true
    }
  }
}
</script>

<style>
#app {
  font-family: 'Open Sans', sans-serif;
}
</style>
