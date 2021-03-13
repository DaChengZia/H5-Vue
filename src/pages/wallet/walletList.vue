<template>
  <div class="wallet-transaction-list-wrap">
    <div
      class="wallet-transaction-list"
      :class="{'wallet-transaction-list-add': item.type === 'add'}"
      v-for="(item,index) in data"
      :key="index"
      >
      <div class="wallet-transaction-list-left">
        <p>{{item.title}}</p>
        <div>
          <span>2021-02-19</span>
          <span>00:45:02</span>
        </div>
      </div>
      <div class="wallet-transaction-list-right">{{item.amount}}</div>
    </div>
  </div>
</template>

<script>
const data = [
  {
    title: '邀请好友',
    amount: '+20',
    type: 'add'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '邀请好友',
    amount: '+20',
    type: 'add'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '邀请好友',
    amount: '+20',
    type: 'add'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '邀请好友',
    amount: '+20',
    type: 'add'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '邀请好友',
    amount: '+20',
    type: 'add'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },
  {
    title: '兑换话费',
    amount: '-2000',
    type: 'remove'
  },

]
export default {
  name: "walletList",
  data() {
    return {
      data
    }
  }
}
</script>
