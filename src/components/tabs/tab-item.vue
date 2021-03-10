<template>
  <div class="tab-item" :class="{'tab-selected': currentSelected,}">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'tab-item',
  props: {
    currentSelected: Boolean,
  }
}
</script>