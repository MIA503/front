<template>
    <el-submenu :index="{ menuIndex }" >
        <template slot="title">
            <i class="el-icon-message"></i> {{menuTitle}}
        </template>
        <MenuItemGroup 
            v-for="menuGroupData in menuGroupDatas"
            :key="menuGroupData.id"
            :groupTitle="menuGroupData.groupTitle"
            :items="menuGroupData.items"
            @open-container="openContainer"
        ></MenuItemGroup>
    </el-submenu>
</template>

<script>
import MenuItemGroup from './MenuItemGroup.vue'

export default {
  name: 'SubMenu',
  props: {
      menuIndex: String,
      menuTitle: String,
      menuGroupDatas: Array
  },
  components: {
      MenuItemGroup
  },
  methods: {
      openContainer: function (msg) {
          this.$emit("open-cont", msg)
      }
  },
}
</script>

<style>
el-submenu {
    display: inline-block;
    text-align:left
}
</style>
