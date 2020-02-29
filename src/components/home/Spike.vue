<template>
    <div class="spike">
        <swiper :options="swiperOption">
     <swiper-slide v-for="item in spikeList" :key="item.id">
                <div class="spike-content">
                    <div class="spike-top">
                        <img src="@/assets/img/spike1.png">
                        <span>距离结束</span>
                        <count-down
                                :currentTime="item.startTime"
                                :startTime="item.startTime"
                                :endTime="item.endTime"
                                :dayTxt="'天'"
                                :hourTxt="':'"
                                :minutesTxt="':'"
                                :secondsTxt="''">
                        </count-down>
                    </div>
                    <div class="spike-bottom">
                        <img :src="item.imgUrl">
                        <div class="bottom-title">
                            <p>{{item.title}}</p>
                            <div class="bottom-price">
                            <span>￥{{item.price}}
                            </span>
                                <p>剩下{{item.num}}个</p>
                            </div>
                        </div>
                    </div>
                </div>
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    import CountDown from 'vue2-countdown'
    export default {
        props:['spikeList'],
        components:{
            CountDown,/*在当前页面引入组件*/
        },
        data(){
            return{
                swiperOption:{
                    pagination:{
                        el: '.swiper-pagination'
                    }
                }
            }
        },
        mounted(){
            console.log(new Date().getTime()+5*24*3600)
        }
    }
</script>

<style scoped>
    .spike{
        width: 100%;
        height: 4.377777rem;
    }
    .spike-content{
        padding:.3rem; /*包一个元素就把padding整体撑开了*/
    }
    .spike-top{
        width: 100%;
        height: 1.2933333rem;
        display: flex;
        align-items: center;
        font-size:.35rem;
    }
    .spike-top img{
        height: .41333333rem;
        width: 1.89333333rem;
    }
    .spike-top span{
        margin-left:.15rem;
    }
    .spike-top div>>> span:nth-child(1){
        background: #ffffff;
        color: #000;
        font-weight: 900;
    }
    .spike-top > div{
        margin-left:.15rem;
    }
    .spike-top >>> div span {
        margin-left:.15rem;
        color: #fff;
        border-radius: .1rem;
        background: #8b8b8b;
        padding:0 .1rem;
    }
    .spike-bottom{
        display: flex;
        justify-content: space-between;
    }
    .spike-bottom img{
        width: 3.093333rem;
        height: 2.12rem;
    }
    .spike-bottom .bottom-title{
        width: 5.86rem;
    }

    .bottom-title p{
        line-height: .58rem;
        font-size: .35rem;
        color: #333;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;
        overflow: hidden;
    }
    .bottom-price{
        margin-top:.8rem;
        display: flex;
        justify-content: space-between;
        font-size: .35rem;
    }
    .bottom-price p{
        border: 1px solid #444;
        border-radius: .1rem;
        background: #fed101;
        margin-bottom: .1rem;
        width: 1.8rem;
        text-align: center;
    }

    .swiper-container{
        overflow: visible;
    }
    .swiper-pagination >>> .swiper-pagination-bullet-active{
        background: orange;
    }
    .swiper-pagination-fraction, .swiper-pagination-custom, .swiper-container-horizontal > .swiper-pagination-bullets{
        bottom:-.6rem;
    }
</style>