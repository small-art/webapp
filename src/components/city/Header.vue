<template>
    <header>
         选择城市
        <i class="iconfont" @click="toHome">&#xe600;</i>
    </header>
</template>

<script>
    export default {
      methods:{/*方法*/
          toHome(){ /*函数*/
              this.$router.push({
                  path:'/'
              })
          }
      }
    }
</script>

<style scoped>
    header{
        background: #fed101;
        text-align: center;
        height: 1.173rem;
        line-height: 1.173rem;
        color: #333;
        font-size:.433333333rem;
        position: relative;
    }
    header i{
        position: absolute;
        right: .3rem;

    }
</style>