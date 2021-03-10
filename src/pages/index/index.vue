<template>
    <!-- 如果是店铺首页添加class：homePage-storegoods -->
    <div class="homePage homePage-storegoods">
            <div class="store-details-container">
                <p>Today便利店</p>
                <div class="store-details-location">
                    <span></span>
                    湖北省武汉市洪山区南湖大道501
                </div>
            </div>
        <!-- <div class="collectCoin"></div> -->
        <div class="homePage_wrap">
            <!-- <div class="homePage_game">
                <div><img src="../../assets/icons/index/icon_turntable.png" alt="">幸运转盘</div>
                <div><img src="../../assets/icons/index/icon_jigsaw.png" alt="">拼什么拼</div>
                <div class="game_mission"><img src="../../assets/icons/index/icon_mission.png" alt="">赚多多币</div>
                <div><img src="../../assets/icons/index/icon_tank.png" alt="">坦克大战</div>
                <div><img src="../../assets/icons/index/icon_convent.png" alt="">兑话费</div>
            </div> -->

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
                        <!-- 首页 - 全部 -->
                        <!-- <div id="s0" class="weui-tab__content" style="display: block; opacity: 1;">
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
                            <div class="swiper_container">
                                <img class="swiper_item" src="../../assets/icons/index/banner.png" alt="">
                                <div class="swiper_dot_container">
                                    <div class="swiper_dot"></div>
                                    <div class="swiper_dot swiper_dot_active"></div>
                                </div>
                            </div>
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
                        </div> -->
                        <!-- 店铺首页 -->
                        <!-- <div id="s1" class="weui-tab__content" style="opacity: 1; display: block;">
                            <div class="store-goods-wrap store-goods-hot">
                                <div class="store-goods-tab-mainly">
                                    <div class="tab-mainly-item tab-mainly-item-selected tab-mainly-item-hot"><span>荐</span>热卖</div>
                                    <div class="tab-mainly-item">休闲食品</div>
                                    <div class="tab-mainly-item">酒水饮料</div>
                                    <div class="tab-mainly-item">粮油调料</div>
                                </div>
                                <div class="store-goods-container">
                                    <div class="store-goods-tab-secondary-container">
                                        //<div class="store-goods-title">热卖</div>
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
                        <!-- 六环服饰 -->
                        <!-- <div id="s2" class="weui-tab__content" style="opacity: 1; display: block;">
                            <div class="clothes-wrap">
                                <div class="clothes-banner">
                                    <img src="../../assets/icons/index/banner.png" alt="">
                                </div>
                                <div class="clothes-category-wrap">
                                <tab>
                                    <tab-item v-for="(item, index) in clothesTab" :key="index">
                                        <div class="clothes-category-item">
                                        <img src="../../assets/imgs/clothes.jpg" alt="">
                                        <p>{{item.title}}</p>
                                    </div>
                                    </tab-item>
                                </tab>
                                </div>
                                <div class="clothes-declare"><img src="../../assets/imgs/declare.jpg" alt=""></div>
                                <div class="clothes-container">
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/clothes1.jpg" alt="">
                                        <p>嘿马七作日系男士冬季立领短款加厚羽绒服潮防风宽松防水防水防水</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/clothes1.jpg" alt="">
                                        <p>嘿马七作日系男士冬季立领短款加厚羽绒服潮防风宽松防水防水防水</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/clothes1.jpg" alt="">
                                        <p>嘿马七作日系男士冬季立领短款加厚羽绒服潮防风宽松防水防水防水</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div> -->
                        <!-- 星夜生活 -->
                        <div id="s3" class="weui-tab__content" style="opacity: 1; display: block;">
                            <div class="clothes-wrap lifes-content">
                                <div class="clothes-banner">
                                <div class="swiper_container">
                                    <img class="swiper_item" src="../../assets/imgs/lifesbanner.jpg" alt="">
                                    <div class="swiper_dot_container">
                                        <div class="swiper_dot"></div>
                                        <div class="swiper_dot swiper_dot_active"></div>
                                    </div>
                                </div>
                                    <img src="../../assets/imgs/lifesbannertext.jpg" alt="">
                                </div>
                                <div class="clothes-category-wrap">
                                    <tab>
                                        <tab-item v-for="(item, index) in clothesTab" :key="index">
                                            <div class="clothes-category-item">
                                            <img src="../../assets/imgs/lifes.jpg" alt="">
                                            <p>{{item.title}}</p>
                                        </div>
                                        </tab-item>
                                    </tab>
                                </div>
                                <div class="clothes-container">
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/lifes1.jpg" alt="">
                                        <p>素士H5点吹风机梵高联名礼盒装</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/lifes1.jpg" alt="">
                                        <p>素士H5点吹风机梵高联名礼盒装</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                    <div class="clothes-item">
                                        <img class="clothes-item-img" src="../../assets/imgs/lifes1.jpg" alt="">
                                        <p>素士H5点吹风机梵高联名礼盒装</p>
                                        <div class="clothes-item-bottom">
                                            <span>￥378</span>
                                            <img src="../../assets/imgs/discount.jpg" alt="">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { Tab, TabItem } from '../../components/index.js';
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
    const clothesTab = [
        {
            src: '../../assets/imgs/goods.jpg',
            title: '新品速递',
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '冰点特价',
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '男装',
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '女装',
        },
        {
            src: '../../assets/imgs/goods.jpg',
            title: '鞋类',
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
            Tab,
            TabItem,
        },
        data () {
            return {
                tabList,
                tabList1,
                clothesTab,
                recommendData,
                storegoods
            }
        }
    }
</script>
