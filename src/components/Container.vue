<template>
  <el-container>
    <el-header style="text-align: right; font-size: 12px">
      <el-dropdown>
        <i class="el-icon-setting" style="margin-right: 15px"></i>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>查看</el-dropdown-item>
          <el-dropdown-item>新增</el-dropdown-item>
          <el-dropdown-item>删除</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <span>Hello World!</span>
    </el-header>
    
    <el-main>
         <h1>{{ content }}</h1>
         <Babel v-if="content === 'babel'"/>
         <Eslint v-else-if="content === 'eslint'"/>
    </el-main>
  </el-container>
</template>

<script>
import HelloWorld from './HelloWorld.vue'
import Babel from './container/babel.vue'
import Eslint from './container/eslint.vue'

export default {
  name: 'Container',
  props: {
    content: String
  },
  components: {
    HelloWorld,
   Babel,
   Eslint
  }

}
</script>
<style>
    .el-header {
    background-color: #42b983;
    color: #333;
    line-height: 60px;
  }
</style>
