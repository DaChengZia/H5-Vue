<template>
  <div class="panel_wrap">
            <div class="panel_title">选中门店</div>
            <div class="panel_container">
                <List />
            </div>
        </div>
</template>

<script>
import List from '../list/List.vue'

export default {
  name: 'Panel',
  components: {
    List
  }
}
</script>