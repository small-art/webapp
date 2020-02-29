<template>
    <div class='scroll'>
        <div class='scroll-content'>
            <div class='scroll-right'>
                <ul :class='{aniamtedTop}'>
                    <li v-for='item in scrollList' :key="item.id">
                        <img src="@/assets/img/scroll.png" alt="">
                        {{item.title}}
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data () {
            return{
                aniamtedTop:false,
                scrollList:[
                    {
                        id:0,
                        title:"清迈旅游落地签如何搞定？360°带你了解泰北小城清迈"
                    },
                    {
                        id:1,
                        title:"港珠澳大桥怎么走？穿梭巴士预约及过关全攻略"
                    },
                    {
                        id:2,
                        title:"港珠澳大桥怎么走？穿梭巴士预约及过关全攻略"
                    },
                    {
                        id:3,
                        title:"清迈旅游落地签如何搞定？360°带你了解泰北小城清迈"
                    },
                    {
                        id:4,
                        title:"港珠澳大桥怎么走？穿梭巴士预约及过关全攻略"
                    },
                    {
                        id:5,
                        title:"清迈旅游落地签如何搞定？360°带你了解泰北小城清迈"
                    }
                ]
            }
        },
        mounted(){
            setInterval(this.showScroll,2000);
        },
        methods:{
            showScroll(){
                this.aniamtedTop=true;
                setTimeout(()=>{
                    this.scrollList.push(this.scrollList[0]);
                    this.scrollList.shift();
                    this.aniamtedTop=false;
                },500)
            }
        }
    }
</script>

<style scoped>
    .aniamtedTop{
        /*定义animatedTop类*/
        transition: all .5s;
        margin-top:-.66666666rem;
    }
.scroll{
    padding: .3rem 0;
}
    .scroll-content{
        background: url("http://localhost:8081/img/scroll.png") no-repeat;
        background-size:100%;
        width: 100%;
        height: 1.33333333rem;
        position: relative;
    }
.scroll-right{
    position: absolute;
    right:0;
    width: 8.13333333rem;
    height: 1.3333333rem;
    overflow: hidden;
}

li{
    font-size:.35rem;
    color:#333;
    line-height: .66666666rem;
    overflow: hidden;
    text-overflow:ellipsis;
    white-space: nowrap;
}
li img{
    width: .16rem;
    height: .16rem;
}
</style>