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
      <div class="redpacket-item-wrap coupon-item-wrap">
        <div class="redpacket-item-row">
          <div class="redpacket-item">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              <div>可省<span>10</span>元</div>
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
          <div class="redpacket-item">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              <div>可省<span>10</span>元</div>
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
        </div>
         <div class="redpacket-item-row">
          <div class="redpacket-item ">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              <div>可省<span>10</span>元</div>
              <div class="redpacket-item-desc-button">立即使用</div>
            </div>
          </div>
         </div>
      </div>
    </div>
    <div class="wallet-container" v-if="num==1">
      <div class="redpacket-item-wrap coupon-item-wrap">
        <div class="redpacket-item-row">
          <div class="redpacket-item" :class="{'coupon-item-used': num==1}">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              已使用
            </div>
          </div>
          <div class="redpacket-item" :class="{'coupon-item-used': num==1}">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
              </div>
            </div>
            <div class="redpacket-item-desc">
              已使用
            </div>
          </div>
        </div>
         <div class="redpacket-item-row">
          <div class="redpacket-item" :class="{'coupon-item-used': num==1}">
            <div class="redpacket-item-amount">
              <div class="redpacket-item-amount-left">
                <p>￥10</p>
                <div>砍价神券</div>
              </div>
              <div class="redpacket-item-amount-right">
                <span>2021-12-31</span>
                <span>有效期至</span>
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
  name: "coupon",
  data() {
    return {
      num
    }
  },
}
</script>
