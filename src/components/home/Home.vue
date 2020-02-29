<template>
   <div class="home">
       <Banner></Banner>
       <Icons></Icons>
       <Tabs></Tabs>
       <Scroll></Scroll>
       <Swiper></Swiper>
       <Spike></Spike>
       <Like></Like>
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
        components:{
            Banner,
            Icons,
            Tabs,
            Scroll,
            Swiper,
            Spike,
            Like,
            Footer
        }
    }
</script>

<style scoped>
.home{
    overflow: hidden;
}
</style>