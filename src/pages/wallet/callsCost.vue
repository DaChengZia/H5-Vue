<template>
  <div class="wallet-wrap" id="wallet">
    <div class="wallet-tab-wrap">
      <div class="wallet-tab-container">
          <div class="wallet-tab-item" :class="{'wallet-tab-item-active': num==0}" @click="num=0">
            未使用
          </div>
          <div class="wallet-tab-item"  :class="{'wallet-tab-item-active': num==1}" @click="num=1">
            已使用
          </div>
      </div>
    </div>
    <div class="wallet-container" v-show="num==0">
      <div class="wallet-tab-list wallet-tab-list-style1">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>1</span>元</div>
        </div>
        <div class="wallet-tab-list-right">立即兑换</div>
      </div>
      <div class="wallet-tab-list wallet-tab-list-style2">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>2</span>元</div>
        </div>
        <div class="wallet-tab-list-right">立即兑换</div>
      </div>
      <div class="wallet-tab-list wallet-tab-list-style3">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>5</span>元</div>
        </div>
        <div class="wallet-tab-list-right">立即兑换</div>
      </div>
    </div>
    <div class="wallet-container" v-show="num==1">
      <div class="wallet-tab-list wallet-tab-list-style1">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>1</span>元</div>
        </div>
        <div class="wallet-tab-list-used"></div>
      </div>
      <div class="wallet-tab-list wallet-tab-list-style2">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>2</span>元</div>
        </div>
        <div class="wallet-tab-list-used"></div>
      </div>
      <div class="wallet-tab-list wallet-tab-list-style3">
        <div class="wallet-tab-list-left">
          <div>话费券</div>
          <div><span>5</span>元</div>
        </div>
        <div class="wallet-tab-list-used"></div>
      </div>
    </div>
  </div>
      
</template>

<script>
const num = 0;
export default {
  name: "callsCost",
  data() {
    return {
      num
    }
  },
  methods: {
    handleClick: function() {
      
    }
  }
}
</script>