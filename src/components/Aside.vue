<template>
  <el-aside width="250px" style="background-color: rgb(238, 241, 246)" >
    <el-menu>
      <SubMenu
        v-for="menudata in menus" 
        v-bind:menuIndex="menudata.id"
        v-bind:menuTitle="menudata.menuTitle"
        v-bind:menuGroupDatas="menudata.menuGroupDatas"
        @open-cont="openCount"
      ></SubMenu>
    </el-menu>
  </el-aside>
</template>

<script>
import SubMenu from './SubMenu.vue'

export default {
  name: 'Aside',
  props: {
    menus: Array
  },
  components: {
    SubMenu
  },
  methods: {
    openCount: function (msg) {
      this.$emit("hello", msg)
    }
  },  
}
</script>

<style>
  .el-aside {
    color: #2c3e50;
  }
</style>
