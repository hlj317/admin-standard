<template>
  <el-container id="app"
                class="el-container">
    <aside-component></aside-component>
    <router-view class="view"></router-view>
  </el-container>

</template>

<style lang="less">
@import "./index.less";
</style>

<script>
import asideComponent from './components/aside-component.vue'
import headerComponent from './components/header-component.vue'
export default {
  data () {
    return {
      show: true,
      selectedNav: 'effect',
      myData: [
        {
          'type': 'effect',
          'name': '效果',
          'column': 6,
          'html': '暂无'
        },
        {
          'type': 'code',
          'name': '代码',
          'column': 6,
          'html': '<el-row :gutter="20"><el-col :span="6"><div class="grid-content bg-purple"></div></el-col><el-col :span="6"><div class="grid-content bg-purple"></div></el-col><el-col :span="6"><div class="grid-content bg-purple"></div></el-col><el-col :span="6"><div class="grid-content bg-purple"></div></el-col></el-row>'
        },
        {
          'type': 'api',
          'name': '文档',
          'column': 6,
          'html': '暂无2'
        },
        {
          'type': 'remark',
          'name': '备注',
          'column': 6,
          'html': '暂无3'
        }
      ]
    }
  },

  methods: {
    navSwitchFun: function (nav) {
      this.type = nav;
      this.selected = nav;
      this.selectedNav = nav;
    },
    isSelected: function (type) {
      return {
        'selected': this.selectedNav === type
      };
    },
    isShow: function (type) {
      return this.selectedNav === type;
    }
  },
  components: {
    asideComponent,
    headerComponent
  }
}
</script>
