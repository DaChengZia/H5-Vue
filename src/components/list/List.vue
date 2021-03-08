<template>
    <div class="list_container">
      <div class="list_title">Today便利店</div>
      <div class="list_item" v-if="true">
        <div class="list_left">湖北省武汉市洪山区南湖大道501</div>
        <div class="list_right">距您<span class="list_right_distance">500</span>m</div>
      </div>
      <div class="list_item" v-if="false">
        <div class="list_left">商品金额</div>
        <div class="list_right">距您<span class="list_right_distance">￥598.00</span>m</div>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'List'
  }
</script>