<template>
    <div class="banner">
        <transition
                enter-active-class='bounceInLeft'
                leave-active-class='zoomOutLeft'
        >
            <div class='banner-left animated' v-show='toshow'></div>
        </transition>
        <div class="banner-header">
            <div class='banner-top'>
        <div class="top-left"
        @click="toCity"
        >
            <!--添加一个跳转事件-->
           {{cityName}}
            <i class="iconfont">&#xe602;</i>
        </div>
        <div class="top-search">
            <i class="iconfont">&#xe635;</i>
            泰国
        </div>
        <div class="top-right">
            <img src="@/assets/img/show.png" alt=""
                 @click='toShow'
            >
        </div>
    </div>
           <div class='banner-swiper'>
            <swiper :options="swiperOption">
                <!-- slides -->
                <swiper-slide>
                    <img src="@/assets/img/banner1.png" alt="">
                </swiper-slide>
                <swiper-slide>
                    <img src="@/assets/img/banner2.png" alt="">
                </swiper-slide>
                <swiper-slide>
                    <img src="@/assets/img/banner3.png" alt="">
                </swiper-slide>

                <!-- Optional controls -->
                <div class="swiper-pagination"  slot="pagination"></div>
            </swiper>

        </div>
        </div>
    </div>

</template>

<script>
    import {mapState} from 'vuex'
    export default {
       data(){
           return{
               toshow:false,
               swiperOption:{
                   loop:true,
                   autoplay: {
                       delay: 2000, //自动切换
                       disableOnInteraction: false
                   },
                   pagination:{
                       el: '.swiper-pagination'
                   }
               }
           }
       },
        computed:{
            ...mapState(['cityName'])
        },
    methods:{
        toShow(){
            this.toshow=!this.toshow;
        },
        toCity(){
            this.$router.push({
                 path:"/city"
            })
        },

    }
       }
</script>

<style scoped>
    .banner-left{
        position: absolute;
        left: 0;
        top: 0;
        z-index: 99999;
        background: #000;
        width: 6.6666666rem;
        height: 100%;
    }
    .banner-header{
        background: #f5f5f5;
        width: 100%;
        height: 5.6rem;
        position: relative;
    }
    .banner-top{
        position: absolute;
        left: 0;
        top: .5rem;
        z-index: 2;
        height: .8rem;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .top-left{
        padding:.2rem .4rem;
        color:#fff;
        font-size:.4266666rem;
    }
    .top-search{
        flex: 1;
        color: #333333;
        background: #ffffff;
        border-radius: .1rem;
        font-size: .3733333rem;
        padding: .2rem .2rem;
    }
    .top-right{
        padding:.2rem .4rem;
    }
    .top-right img{
        height: .5333333rem;
        width: .5333333rem;
    }

    .banner-swiper{
        width: 100%;
        height: 100%;
    }
    .banner-swiper img{
        width: 100%;
        height: 100%;
    }
    .swiper-pagination >>> .swiper-pagination-bullet-active{
        background: orange;
    }
</style>