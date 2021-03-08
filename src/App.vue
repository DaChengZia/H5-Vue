<template>
  <div class="container" id="container">
    <div class="page tabbar js_show">
    <div class="page__bd">
        <div class="weui-tab">
            <div class="weui-tab__panel">
              <homePage />
            </div>
            <div class="weui-tabbar">
                <div class="weui-tabbar__item weui-bar__item_on">
                    <img src="./assets/icons/tabs/icon_home_h.png" class="weui-tabbar__icon" />
                    <p class="weui-tabbar__label">首页</p>
                </div>
                <div class="weui-tabbar__item">
                    <div class="weui-badge_wrap">
                        <img src="./assets/icons/tabs/icon_shopping_n.png" class="weui-tabbar__icon" />
                        <span class="weui-badge">8</span>
                    </div>
                    <p class="weui-tabbar__label">购物车</p>
                </div>
                <div class="weui-tabbar__item">
                    <img src="./assets/icons/tabs/icon_my_n.png" class="weui-tabbar__icon">
                    <p class="weui-tabbar__label">我的</p>
                </div>
            </div>
        </div>
    </div>
    </div>
  </div>
</template>

<script>
import { homePage } from './pages/index.js'
import $ from 'jquery'

export default {
  name: 'App',
  components: {
    homePage
  }
}
// for search input
$(function(){
    var $searchBar = $('#searchBar'),
        $searchResult = $('#searchResult'),
        $searchText = $('#searchText'),
        $searchInput = $('#searchInput'),
        $searchClear = $('#searchClear'),
        $searchCancel = $('#searchCancel');

    function hideSearchResult(){
        $searchResult.hide();
        $searchInput.val('');
    }
    function cancelSearch(){
        hideSearchResult();
        $searchBar.removeClass('weui-search-bar_focusing');
        $searchText.show();
    }

    $searchText.on('click', function(){
        $searchBar.addClass('weui-search-bar_focusing');
        $searchInput.focus();
    });
    $searchInput
        .on('blur', function () {
            if(!this.value.length) cancelSearch();
        })
        .on('input', function(){
            if(this.value.length) {
                $searchResult.show();
            } else {
                $searchResult.hide();
            }
        })
    ;
    $searchClear.on('click', function(){
        hideSearchResult();
        $searchInput.focus();
    });
    $searchCancel.on('click', function(){
        cancelSearch();
        $searchInput.blur();
    });
});
// for tabbar
$(function(){
    $('.weui-tabbar__item').on('click', function () {
        $(this).addClass('weui-bar__item_on').siblings('.weui-bar__item_on').removeClass('weui-bar__item_on');
    });
});
</script>

<style>
#app {
  height: 100%;
  width: 100%;
}
</style>
