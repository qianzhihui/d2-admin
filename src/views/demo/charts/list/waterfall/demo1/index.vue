<template>
  <d2-container :filename="filename">
    <template slot="header">一般</template>
    <div class="inner">
      <ve-waterfall :data="chartData" v-bind="pubSetting"></ve-waterfall>
    </div>
    <template slot="footer">
      <d2-link-btn title="更多示例和文档" link="https://v-charts.js.org"/>
    </template>
  </d2-container>
</template>

<script>
import list from '@/views/demo/charts/list/_mixin/list.js'
export default {
  mixins: [
    list
  ],
  data () {
    return {
      filename: __filename,
      chartData: {
        columns: ['活动', '时间'],
        rows: [
          { '活动': '吃饭', '时间': 4 },
          { '活动': '睡觉', '时间': 10 },
          { '活动': '打豆豆', '时间': 5 }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.inner {
  position: absolute;
  top: 20px;
  right:  20px;
  bottom: 20px;
  left: 20px;
}
</style>
