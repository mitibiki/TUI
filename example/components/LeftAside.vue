<template>
  <div>
    <ul class="aside-item">
      <div class="navigate-group">开发指南</div>
      <li class="t-menu-item">
        <a href="#">
          <span>安装</span>
        </a>
      </li>
      <li class="t-menu-item">
        <a href="#">
          <span>快速上手</span>
        </a>
      </li>
      <li class="t-menu-item">
        <a href="#">
          <span>概览</span>
        </a>
      </li>
      <li class="t-menu-item">
        <a href="#">
          <span>定制主题</span>
        </a>
      </li>
      <li class="t-menu-item">
        <a href="#">
          <span>更新日志</span>
        </a>
      </li>
      <div class="navigate-group">组件</div>
      <!--基础组件-->
      <li class="t-menu-item-group">
        <div class="t-menu-item-title">
          Basic
        </div>
        <ul class="t-menu-item-list">
          <li v-for="(i, k) in basicList" :key="k">
            <router-link :to="i.route">
              <span>{{ i.name }}</span>
              <span class="chinese">{{ i.chinese }}</span>
            </router-link>
          </li>
        </ul>
      </li>
      <!--表单组件-->
      <li class="t-menu-item-group">
        <div class="t-menu-item-title">
          Form
        </div>
        <ul class="t-menu-item-list">
          <li v-for="(i, k) in formList" :key="k">
            <router-link :to="i.route">
              <span>{{ i.name }}</span>
              <span class="chinese">{{ i.chinese }}</span>
            </router-link>
          </li>
        </ul>
      </li>
      <!--数据展示组件-->
      <li class="t-menu-item-group">
        <div class="t-menu-item-title">
          Data
        </div>
        <ul class="t-menu-item-list">
          <li v-for="(i, k) in dataList" :key="k">
            <router-link :to="i.route">
              <span>{{ i.name }}</span>
              <span class="chinese">{{ i.chinese }}</span>
            </router-link>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      basicList: [
        {
          route: '/button',
          name: 'Button',
          chinese: '按钮'
        },
        {
          route: '/dialog',
          name: 'Dialog',
          chinese: '提示框'
        },
        {
          route: '/layout',
          name: 'Layout',
          chinese: '栅格'
        }
      ],
      formList: [
        {
          route: '/input',
          name: 'Input',
          chinese: '输入框'
        },
        {
          route: '/input-number',
          name: 'InputNumber',
          chinese: '计数器'
        },
        {
          route: '/checkbox',
          name: 'CheckBox',
          chinese: '多选框'
        },
        {
          route: '/radio',
          name: 'Radio',
          chinese: '单选框'
        },
        {
          route: '/select',
          name: 'Select',
          chinese: '下拉框'
        },
        {
          route: '/cascader',
          name: 'Cascader',
          chinese: '级联'
        },
        {
          route: '/datepicker',
          name: 'Datepicker',
          chinese: '日期选择器'
        },
        {
          route: '/timepicker',
          name: 'Timepicker',
          chinese: '时间选择器'
        },
        {
          route: '/form',
          name: 'Form',
          chinese: '表单'
        }
      ],
      dataList: [
        {
          route: '/table',
          name: 'Table',
          chinese: '表格'
        },
        {
          route: '/tag',
          name: 'Tag',
          chinese: '标签'
        },
        {
          route: '/progress',
          name: 'Progress',
          chinese: '进度条'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped="">
  @import "../styles/leftAside";
</style>
