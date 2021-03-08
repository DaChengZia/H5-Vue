<template>
<div class="weui-tab" id="t1" style="height:auto;">
  <div class="weui-navbar">
      <div class="weui-navbar__item tab-green">
          全部
      </div>
      <div class="weui-navbar__item">
          本店好货
      </div>
      <div class="weui-navbar__item">
          六环服饰
      </div>
      <div class="weui-navbar__item">
          星夜生活
      </div>
  </div>
  <div class="weui-tab__panel">
    <div id="s0" class="weui-tab__content" style="display: block; opacity: 1;">全部</div>
    <div id="s1" class="weui-tab__content" style="opacity: 1; display: none;">本店好货</div>
    <div id="s2" class="weui-tab__content" style="opacity: 1; display: none;">六环服饰</div>
    <div id="s3" class="weui-tab__content" style="opacity: 1; display: none;">星夜生活</div>
  </div>
</div>
</template>

<script>

export default {
  name: 'Tabs',
}
</script>

<style lang="less" scoped>

</style>
