<template>
  <el-menu
    :default-active="activeIndex"
    :router="true"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
  >
    <el-menu-item :route="{ name: 'home' }" index="1">Home</el-menu-item>
    <el-menu-item :route="{ name: 'tasks' }" index="2">Tasks</el-menu-item>
    <el-menu-item :route="{ name: 'calendar' }" index="3">Calendar</el-menu-item>
    <el-menu-item :route="{ name: 'table' }" index="4">Table</el-menu-item>
    <el-menu-item :route="{ name: 'form' }" index="5">Form</el-menu-item>

      <el-button @click="openDrawer" type="primary" style="margin-left: 16px;">
        menu
      </el-button>
  </el-menu>
</template>

<script>
export default {
  props: {
    openDrawer: Function
  },
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>
