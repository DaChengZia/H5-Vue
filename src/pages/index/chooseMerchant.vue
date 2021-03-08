<template>
  <div class="chooseMerchant_Wrap" id="chooseMerchant">
        <div class="weui-search-bar" id="searchBar">
            <form class="weui-search-bar__form">
                <div class="weui-search-bar__box">
                    <i class="weui-icon-search"></i>
                    <input type="search" class="weui-search-bar__input" id="searchInput" placeholder="请输入门店或所在地址" required/>
                    <a href="javascript:" class="weui-icon-clear" id="searchClear"></a>
                </div>
                <label class="weui-search-bar__label" id="searchText">
                    <i class="weui-icon-search"></i>
                    <span>搜索</span>
                </label>
            </form>
        </div>
        <div class="chooseMerchant_container">
            <Panel />
            <Panel />
            <Panel />
        </div>
    </div>
</template>

<script>
import { Panel } from '../../components/index.js';

export default {
    name: 'chooseMerchant',
    components: {
        Panel
    }
}
</script>