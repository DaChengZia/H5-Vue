<template>
  <div class="waterfall_container">
    <div class="waterfall_wrap" v-bind:class="{shouldfloat: isfloat}">
      <div class="waterfall_item">
        <img class="waterfall_item_img" src="../../assets/imgs/goods.jpg" alt="">
        <p>优乐多酸奶饮料牛奶100ml*20瓶</p>
        <div class="waterfall_item_bottom">
          <div><span class="waterfall_item_price">￥24.90</span>/盒</div>
          <div class="waterfall_item_add"></div>
        </div>
      </div>
      <div class="waterfall_item">
        <img class="waterfall_item_img" src="../../assets/imgs/goods.jpg" alt="">
        <p>优乐多酸奶饮料牛奶100ml*20瓶</p>
        <div class="waterfall_item_bottom">
          <div><span class="waterfall_item_price">￥24.90</span>/盒</div>
          <div class="waterfall_item_add"></div>
        </div>
      </div>
      <div class="waterfall_item">
        <img class="waterfall_item_img" src="../../assets/imgs/goods.jpg" alt="">
        <p>优乐多酸奶饮料牛奶100ml*20瓶</p>
        <div class="waterfall_item_bottom">
          <div><span class="waterfall_item_price">￥24.90</span>/盒</div>
          <div class="waterfall_item_add"></div>
        </div>
      </div>
      <div class="waterfall_item">
        <img class="waterfall_item_img" src="../../assets/imgs/goods.jpg" alt="">
        <p>优乐多酸奶饮料牛奶100ml*20瓶</p>
        <div class="waterfall_item_bottom">
          <div><span class="waterfall_item_price">￥24.90</span>/盒</div>
          <div class="waterfall_item_add"></div>
        </div>
      </div>
      <div class="waterfall_item">
        <img class="waterfall_item_img" src="../../assets/imgs/goods.jpg" alt="">
        <p>优乐多酸奶饮料牛奶100ml*20瓶</p>
        <div class="waterfall_item_bottom">
          <div><span class="waterfall_item_price">￥24.90</span>/盒</div>
          <div class="waterfall_item_add"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Waterfall',
    props: ['isfloat','isSmall']
  }
</script>