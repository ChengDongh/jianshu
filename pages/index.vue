<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <!--banner-->
                    <div v-swiper:mySwiper="swiperOption" class="banner">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide" v-for="banner in banners">
                                <img :src="banner">
                            </div>
                        </div>
                        <div class="swiper-pagination swiper-pagination-white"></div>
                        <div class="swiper-button-next swiper-button-white"></div>
                        <div class="swiper-button-prev swiper-button-white"></div>
                    </div>
                    <!--推荐专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.png">
                            <span>文学</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg">
                            <span>IT @ 互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg">
                            <span>IT @ 互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.png">
                            <span>文学</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg">
                            <span>手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg">
                            <span>IT @ 互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg">
                            <span>手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg">
                            <span>IT @ 互联网</span>
                        </nuxt-link>
                        <nuxt-link class="more-hot-collection" to="collection/123">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div id="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <!--图片-->
                                <nuxt-link to="/p/123" class="wrap-img">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <!--正文部分-->
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <!--标题-->
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化为能力？这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认
                                        同，于是市场上出现很多读书方法，比如速度、多读、慢
                                        读、列读……不管你采用哪一种读书方法，最终都要回归
                                        到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">短篇小说</nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <!--正文部分-->
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/default-avatar.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">测试用户</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <!--标题-->
                                    <nuxt-link to="/p/123" class="title">
                                        如何把书中的知识转化为能力？这是我见过的最好的回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认
                                        同，于是市场上出现很多读书方法，比如速度、多读、慢
                                        读、列读……不管你采用哪一种读书方法，最终都要回归
                                        到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">短篇小说</nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <!--阅读更多-->
                    <nuxt-link to="/" class="load-more">
                        阅读更多
                    </nuxt-link>
                </div>
                <div class="col-4 aside">
                    <div class="board">
                        <nuxt-link to="/">
                            <img src="../assets/img/1.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/2.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/3.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/4.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/5.png" alt="">
                        </nuxt-link>
                    </div>
                    <nuxt-link to="/" class="download">
                        <img src="../assets/img/二维码.png">
                        <div class="info">
                            <div class="title">
                                扫描二维码
                                <i class="fa fa-angle-right"></i>
                            </div>
                            <div class="description">扫描二维码查看更多惊喜</div>
                        </div>
                    </nuxt-link>
                    <div class="recommend-author">
                        <div class="title">
                            <span>推荐作者</span>
                            <a href="javascript:void(0)" class="page-change" @click="rotate">
                                <i ref="refresh" class="fa fa-refresh"></i>
                                换一批
                            </a>
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/default-avatar.jpg">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9K字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/default-avatar.jpg">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9K字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/default-avatar.jpg">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9K字·7.2k喜欢
                                </p>
                            </li>
                        </ul>
                        <nuxt-link to="/" class="find-more">
                            查看更多
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <footer class="my-container">
            <div class="row">
                <div class="col-8 footer">
                    <nuxt-link class="footer-tag" to="/">设计者:赵成东</nuxt-link><em>·</em>
                    <nuxt-link class="footer-tag" to="/">联系我们:18917827459</nuxt-link><em>·</em>
                    <nuxt-link class="footer-tag" to="/">QQ:2738448913@qq.com</nuxt-link>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    import NuxtLink from "../.nuxt/components/nuxt-link";
    export default {
        data () {
            return {
                banners: [
                    '/banner1.jpg',
                    '/banner2.jpg',
                    '/banner3.jpg',
                    '/banner4.jpg',
                ],
                swiperOption: {
                    autoplay:{
                        delay:3000,//切换时间
                        stopOnLastSlide:false,//是否停止在最后一张
                        disableOnInteraction:false//禁止轮播
                    },
                    pagination: {
                        el: '.swiper-pagination',
                        dynamicBullets: true
                    },
                    navigation:{
                        nextEl:'.swiper-button-next',
                        prevEl:'.swiper-button-prev'
                    }
                },
                deg:360
            }
        },
        name: "index",
        components:{
            NuxtLink,
            myHeader
        },
        mounted(){

        },
        methods:{
            rotate:function () {
                this.deg = this.deg + 360
                this.$refs.refresh.style.transform = `rotate(${this.deg}deg)`;
            }
        }
    }
</script>

<style>

</style>