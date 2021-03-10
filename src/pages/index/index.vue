<template>
    <div class="homePage">
        <div class="collectCoin"></div>
        <div class="homePage_wrap">
            <div class="homePage_game">
                <div><img src="../../assets/icons/index/icon_turntable.png" alt="">幸运转盘</div>
                <div><img src="../../assets/icons/index/icon_jigsaw.png" alt="">拼什么拼</div>
                <div class="game_mission"><img src="../../assets/icons/index/icon_mission.png" alt="">赚多多币</div>
                <div><img src="../../assets/icons/index/icon_tank.png" alt="">坦克大战</div>
                <div><img src="../../assets/icons/index/icon_convent.png" alt="">兑话费</div>
            </div>
            <div class="homePage_container">
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
                <div class="weui-tab" id="t1" style="height:auto;">
                    <tab>
                        <tab-item :currentSelected="index === 0" :class="{'tab-selected-type1': index===0}" v-for="(item, index) in tabList" :key="index">{{item}}</tab-item>
                    </tab>
                    <div class="weui-tab__panel">
                        <div id="s0" class="weui-tab__content" style="display: block; opacity: 1;">
                            <!-- 老板推荐 -->
                            <div class="recommend">
                                <div class="recommend-head">
                                    <h2 class="recommend">老板推荐</h2>
                                    <div class="recommend-more">更多<span></span></div>
                                </div>
                                <div class="recommend-content">
                                    <div class="recommend-item" v-for="(item,index) in recommendData" :key="index">
                                        <img class="recommend-item-img" src="../../assets/imgs/goods.jpg" alt="">
                                        <p>{{item.title}}</p>
                                        <div class="recommend-item-bottom">
                                            <div><span class="recommend-item-price">{{item.price}}</span>{{item.others}}</div>
                                            <div class="recommend-item-add"></div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <!-- swiper轮播图 -->
                            <div class="swiper_container">
                                <img class="swiper_item" src="../../assets/icons/index/banner.png" alt="">
                                <div class="swiper_dot_container">
                                    <div class="swiper_dot"></div>
                                    <div class="swiper_dot swiper_dot_active"></div>
                                </div>
                            </div>
                            <!-- <Swiper :list="demo03_list" auto style="width:80%;margin:0 auto;" height="180px" dots-class="custom-bottom" dots-position="center"></Swiper> -->
                            <div class="weui-tab" id="t1_1" style="height:auto;">
                                <tab>
                                    <tab-item :currentSelected="index === 0" :class="{'tab-selected-type2': index===0}" v-for="(item, index) in tabList1" :key="index">{{item}}</tab-item>
                                </tab>
                                <div class="weui-tab__panel">
                                    <div id="s0" class="weui-tab__content" style="display: block; opacity: 1;">
                                        <Waterfall :isfloat='true' />
                                        <div id="s1" class="weui-tab__content" style="opacity: 1; display: none;">食品饮料</div>
                                        <div id="s2" class="weui-tab__content" style="opacity: 1; display: none;">粮油副食</div>
                                        <div id="s3" class="weui-tab__content" style="opacity: 1; display: none;">家居清洁</div>
                                    </div>
                                </div>
                            </div>
                            <div id="s1" class="weui-tab__content" style="opacity: 1; display: none;">本店好货</div>
                            <div id="s2" class="weui-tab__content" style="opacity: 1; display: none;">六环服饰</div>
                            <div id="s3" class="weui-tab__content" style="opacity: 1; display: none;">星夜生活</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { Waterfall, Tab, TabItem } from '../../components/index.js';
    const tabList = ['全部', '本店好货', '六环服饰', '星夜生活'];
    const tabList1 = ['热卖商品', '食品饮料', '粮油副食', '家居清洁', '食品饮料', '粮油副食', '家居清洁'];
    const recommendData = [
        {
            src: '../../assets/imgs/goods.jpg',
            title: '优乐多酸奶饮料牛奶100ml*20瓶',
            price: '￥24.90',
            others: '/盒'
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '优乐多酸奶饮料牛奶100ml*20瓶',
            price: '￥24.90',
            others: '/盒'
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '优乐多酸奶饮料牛奶100ml*20瓶',
            price: '￥24.90',
            others: '/盒'
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '优乐多酸奶饮料牛奶100ml*20瓶',
            price: '￥24.90',
            others: '/盒'
        },
    ]

    export default {
        name: 'homePage',
        components: {
            Waterfall,
            Tab,
            TabItem,
        },
        data () {
            return {
                tabList,
                tabList1,
                recommendData
            }
        }
    }
</script>
