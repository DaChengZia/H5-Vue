<template>
    <!-- 如果是店铺首页添加class：homePage-storegoods -->
    <div class="homePage">
            <div class="store-details-container">
                <p>Today便利店</p>
                <div class="store-details-location">
                    <span></span>
                    湖北省武汉市洪山区南湖大道501
                </div>
            </div>
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
                <div class="search-bar-container">
                    <div class="search-bar">
                        <div class="search-icon"></div>
                        <input class="search-input" type="text" placeholder="找找你想要的吧">
                    </div>
                    <div class="search-bar-message"></div>
                </div>
                <div class="weui-tab" id="t1">
                    <tab>
                        <tab-item :currentSelected="index === 0" :class="{'tab-selected-type1': index===0}" v-for="(item, index) in tabList" :key="index">{{item}}</tab-item>
                    </tab>
                    <div class="weui-tab__panel">
                        <!-- //首页 - 全部 -->
                        <div id="s0" class="weui-tab__content" style="display: block; opacity: 1;">
                            <!-- //老板推荐 -->
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
                            <!-- //swiper轮播图 -->
                            <div class="swiper_container">
                                <img class="swiper_item" src="../../assets/icons/index/banner.png" alt="">
                                <div class="swiper_dot_container">
                                    <div class="swiper_dot"></div>
                                    <div class="swiper_dot swiper_dot_active"></div>
                                </div>
                            </div>
                            <!-- //<Swiper :list="demo03_list" auto style="width:80%;margin:0 auto;" height="180px" dots-class="custom-bottom" dots-position="center"></Swiper> -->
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
                        </div>
                        <!-- 店铺首页 -->
                        <!-- <div id="s1" class="weui-tab__content" style="opacity: 1; display: block;">
                            <div class="store-goods-wrap">
                                <div class="store-goods-tab-mainly">
                                    <div class="tab-mainly-item">热卖</div>
                                    <div class="tab-mainly-item tab-mainly-item-selected">休闲食品</div>
                                    <div class="tab-mainly-item">酒水饮料</div>
                                    <div class="tab-mainly-item">粮油调料</div>
                                </div>
                                <div class="store-goods-container">
                                    <div class="store-goods-tab-secondary-container">
                                        <div class="store-goods-tab-secondary-wrap">
                                            <div class="store-goods-tab-secondary">
                                                <div class="tab-secondary-item tab-secondary-item-selected">饮用水</div>
                                                <div class="tab-secondary-item">碳酸饮料</div>
                                                <div class="tab-secondary-item">运动类</div>
                                                <div class="tab-secondary-item">其他</div>
                                            </div>
                                            <div class="store-goods-tab-secondary-arrow secondary-arrow-expand"></div>
                                        </div>
                                        <div class="store-goods-tab-secondary-sort">
                                            <div class="tab-secondary-sort-price tab-secondary-sort-icon">
                                                价格
                                                <span></span>
                                            </div>
                                            <div class="tab-secondary-sort-amount">销量</div>
                                        </div>
                                    </div>
                                    <div class="store-goods-item-wrap">
                                        <div class="store-goods-item" v-for="(item,index) in storegoods" :key="index">
                                            <img src="../../assets/imgs/storegoods.jpg" alt="">
                                            <div class="store-goods-item-details">
                                                <p>{{item.title}}</p>
                                                <div class="store-goods-item-details-wrap">
                                                    <div class="store-goods-item-price">
                                                        <span>{{item.price}}</span>{{item.others}}
                                                    </div>
                                                    <div class="store-goods-item-add"></div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div> -->
                        <div id="s2" class="weui-tab__content" style="opacity: 1; display: none;">六环服饰</div>
                        <div id="s3" class="weui-tab__content" style="opacity: 1; display: none;">星夜生活</div>
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
    ];
    const storegoods = [
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
        },
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
        },
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
        },
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
        },
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
        },
        {
            src: '../../assets/imgs/storegoods.jpg',
            title: '屈臣氏（Watsons）饮用水400ml',
            price: '￥2.49',
            others: '/瓶'
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
                recommendData,
                storegoods
            }
        }
    }
</script>
