<template>
    <el-menu-item-group>
        <template slot="title"> {{ groupTitle }} </template>
        <el-menu-item
            v-for="item in items"
            :key="item.id"
            :index="item.id + '-' + item.id"
            v-on:click="emitContent(item.content)"
        > <a :href="item.url" target="_blank" rel="noopener"> {{item.content}} </a> </el-menu-item>
    </el-menu-item-group>
</template>

<script>
export default {
  name: 'MenuItemGroup',
  props: {
     groupTitle: String,
     items: Array
  },
  methods: {
      emitContent: function (msg) {
          this.$emit('open-container', msg)
      }
  },
}
</script>

<style>
a {
  color: #42b983;
}
</style>