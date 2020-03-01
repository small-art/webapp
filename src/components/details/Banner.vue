<template>
    <div class="banner">
        <div class="banner-img">
            <img :src="item.imgUrl" alt="">
        </div>
        <div class="banner-title">
            {{item.title}}
        </div>
    </div>
</template>

<script>
    export default {
        data(){
          return{
              item:''
          }
        },
        activated(){
          this.item=this.$route.query.item;
        }
    }
</script>

<style scoped>
.banner{
    height: 5.65rem;
    width: 100%;
}
    .banner img{
        width: 100%;
        height: 100%;
    }
    .banner-title{
        padding: .3rem;
        font-size: .4rem;
    }
</style>