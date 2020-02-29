<template>
   <div class="home">
       <Banner></Banner>
       <Icons></Icons>
       <Tabs></Tabs>
       <Scroll></Scroll>
       <Swiper></Swiper>
       <Spike :spikeList="spikeList"></Spike><!--父组件传递子组件-->
       <Like :likeList="likeList"></Like>
       <Footer></Footer>
   </div>
</template>

<script>
    import Banner from './Banner'
    import Icons from './Icons'
    import Tabs from './Tabs'
    import Scroll from './Scroll'
    import Swiper from './Swiper'
    import Spike from './Spike'
    import Like from './Like'
    import Footer from './Footer'

    export default {
        data(){
            return{
          spikeList:[],
          likeList:[],
            }
        },
        components:{
            Banner,
            Icons,
            Tabs,
            Scroll,
            Swiper,
            Spike,
            Like,
            Footer
        },mounted(){
          this.http();
        },
        methods:{/*定一个方法请求接口*/
             http(){
                let That =this;
                this.axios.get("http://localhost:8081/api/dataHome.json")
                    .then((res)=>{
                        let data=res.data.data[0];
                     That.spikeList=data.spikeList;
                     this.likeList=data.likeList;
                    })
             }
        }
    }
</script>

<style scoped>
.home{
    overflow: hidden;
}
</style>