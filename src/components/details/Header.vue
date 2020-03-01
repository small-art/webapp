<template>
    <div class="header">
        <div class="header-left">
            <i class="iconfont"
            @click="toHome"
            >&#xe600;</i>
        </div>
        <div class="header-title">活动详情</div>
        <div class="header-right">
            <i class="iconfont">&#xe602;</i>
        </div>
    </div>
</template>

<script>
    export default {
        methods:{
            toHome(){
                this.$router.push({
                    path:'/'
                })
            }
        }
    }
</script>

<style scoped>
.header{
    background: #f7f7f7;
    height: 1.2rem;
    align-items: center;
    display: flex;
    justify-content: space-between;
    font-size: .6rem;
}
    .header-left{
        padding-left: .5rem ;
    }
.header .header-right{
        padding-right: .5rem ;
        font-weight: 700;
    }
</style>