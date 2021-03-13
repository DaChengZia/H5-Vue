<template>
  <!-- <div class="wallet-wrap" id="wallet">
    <div class="wallet-account">
      <div class="wallet-account-coin">
        <div class="wallet-account-coin-title">
          <div></div>多多币</div>
          <p>12369</p>
      </div>
      <div class="wallet-account-detail">
        <div class="account-detail-item paydetail">
          <div></div>收支明细
        </div>
        <div class="account-detail-item ruledetail">
          <div></div>赚取规则
        </div>
      </div>
    </div>
    <div class="wallet-container">
        <div class="wallet-banner">
          <div class="wallet-banner-img"></div>
          <div class="wallet-banner-time">还有<span>09</span>：<span>26</span>：<span>39</span>过期</div>
        </div>
        <div class="wallet-list">
            <div class="wallet-list-item">
              <div class="wallet-list-item-left wallet-list-item-discount">
                <div></div>砍价神券</div>
              <div class="wallet-list-item-right"></div>
            </div>
            <div class="wallet-list-item">
              <div class="wallet-list-item-left wallet-list-item-redpacket">
                <div></div>红包</div>
              <div class="wallet-list-item-right"></div>
            </div>
            <div class="wallet-list-item">
              <div class="wallet-list-item-left wallet-list-item-phonebill">
                <div></div>话费</div>
              <div class="wallet-list-item-right"></div>
            </div>
        </div>
    </div>
  </div> -->
  <rules />
</template>

<script>
import rules from './rules.vue';

export default {
  name: 'Wallet',
  components: {
    rules
  }
}
</script>