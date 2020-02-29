<template>
    <div class='swiper'>
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide>
                <img src="@/assets/img/swiper1.png" alt="">
            </swiper-slide>
            <swiper-slide>
                <img src="@/assets/img/swiper2.png" alt="">
            </swiper-slide>

            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    export default {
        data(){
            return {
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
        }
    }
</script>

<style scoped>
    .swiper{
        background: #fff9db;
        width: 100%;
        height: 3.2rem;
    }
    .swiper img{
        width: 100%;
        height: 3.2rem;
    }
    .swiper-pagination >>> .swiper-pagination-bullet-active{
        background: orange;
    }
    .swiper-pagination-fraction, .swiper-pagination-custom, .swiper-container-horizontal > .swiper-pagination-bullets{
        bottom:4px;
    }
</style>