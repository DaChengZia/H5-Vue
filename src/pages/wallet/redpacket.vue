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
    <div class="wallet-container" v-if="num==0">
      <div class="redpacket-item-wrap">
        <div class="redpacket-item-row">
          <div class="redpacket-item">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥0.58</p>
                <div>多多随机红包</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              可叠加使用
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
          <div class="redpacket-item">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥0.58</p>
                <div>多多随机红包</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              可叠加使用
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
        </div>
        <div class="redpacket-item-row">
          <div class="redpacket-item">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥0.58</p>
                <div>多多随机红包</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              可叠加使用
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="wallet-container" v-if="num==1">
      <div class="redpacket-item-wrap">
        <div class="redpacket-item-row">
          <div class="redpacket-item" :class="{'redpacket-item-used': num==1}">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥0.58</p>
                <div>多多随机红包</div>
              </div>
            </div>
            <div class="redpacket-item-desc">
              已使用
            </div>
          </div>
          <div class="redpacket-item" :class="{'redpacket-item-used': num==1}">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥0.58</p>
                <div>多多随机红包</div>
              </div>
            </div>
            <div class="redpacket-item-desc">
              已使用
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
      
</template>

<script>
const num = 0;
export default {
  name: "redpacket",
  data() {
    return {
      num
    }
  },
}
</script>