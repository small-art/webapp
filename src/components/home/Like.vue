<template>
    <div class="like">
        <div class="like-list">
            <div class="like-top">
                <div class="top-left">
                    <span>户外与休闲</span>
                </div>
                <p class="top-right">更多></p>
            </div>
            <div class="like-bottom">
                <div class="bottom-header">
                    <div class="header-info">
                        <span>[热带云南]10-4月 春城昆明-建水古</span>
                        <span>￥9999起</span>
                    </div>
                </div>
                <ul>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                </ul>
            </div>
        </div>
        <div class="like-list">
            <div class="like-top">
                <div class="top-left">
                    <span>户外与休闲</span>
                </div>
                <p class="top-right">更多></p>
            </div>
            <div class="like-bottom">
                <div class="bottom-header">
                    <div class="header-info">
                        <span>[热带云南]10-4月 春城昆明-建水古</span>
                        <span>￥9999起</span>
                    </div>
                </div>
                <ul>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                    <li>
                        <img src="http://localhost:8081/img/like2.png" alt="">
                        <span class="title">春城昆明-建水古</span>
                        <span class="price">￥9999起</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>


</template>

<script>
    export default {}
</script>

<style scoped>
    .like {
        padding-bottom: 1.5rem;
        font-size: .35rem;
        margin-top: .8rem;
    }

    .like-list {
        margin-top: .4rem;
    }

    .like-top {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .like-top .top-left {
        position: relative;
        font-family: '宋体';
    }

    .like-top .top-left:before {
        position: absolute;
        content: "";
        background: #fed101;
        width: .1rem;
        height: .48rem;
        top: 0;
    }

    .like-top .top-left span {
        padding-left: .5rem;
        font-size: .5rem;
    }

    .like-top .top-right {
        padding-right: .5rem;
        color: #999;
        font-weight: 500;
        font-size: .4rem;
    }

    .like-bottom {
        padding: .3rem;
    }

    .like-bottom .bottom-header {
        background: url("http://localhost:8081/img/like1.jpg") no-repeat;
        width: 100%;
        height: 4.46666666rem;
        background-size: 100%;
        position: relative;
    }

    .like-bottom .bottom-header .header-info {
        position: absolute;
        bottom: .26rem;
        left: .2rem;
        display: flex;
        justify-content: space-between;
    }

    .like-bottom .bottom-header .header-info span:nth-child(1) {
        font-size: .5rem;
        color: #fff;
        font-weight: 700;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
        width: 5.78rem;
    }

    .like-bottom .bottom-header .header-info span:nth-child(2) {
        color: orange;
        font-weight: 500;
        font-size: .45rem;
        margin-left: 1rem;
    }

    .like-bottom ul {
        display: flex;
        justify-content: center;
        margin-top: .3rem;
    }
    .like-bottom ul li img {
        width: 2.96rem;
        height: 1.9574rem;
        padding: .133333333rem;
        border-radius:10%;
    }
    .like-bottom ul li span.title{
        font-size: .3rem;
        display: block;
        margin-top: .2rem;
    }
    .like-bottom ul li span.price{
        display: block;
        color: orange;
        font-weight: 500;
        font-size: .45rem;
    }
</style>