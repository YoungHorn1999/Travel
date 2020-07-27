<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl"/>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "HomeRecommend",
    data () {
        return {
            recommendList: [
                {
                    id: "0001",
                    imgUrl: "http://img1.qunarzz.com/sight/p0/2006/79/795f80bd0c876ba1a3.img.jpg_200x200_fa6a32f1.jpg",
                    title: '杭州乐园',
                    desc: "浪漫的杭州首站，浪漫的游乐园"
                },
                {
                    id: "0002",
                    imgUrl: "http://img1.qunarzz.com/sight/p0/1603/87/87146cf32fa8635e90.water.png_200x200_5a9bb741.png",
                    title: '西湖',
                    desc: "美丽的西湖，全年适合游玩"
                },
                {
                    id: "0003",
                    imgUrl: "http://img1.qunarzz.com/sight/p0/1807/26/269e0ea49ac0c512a3.img.jpg_200x200_65bf5c23.jpg",
                    title: '千岛湖中心湖',
                    desc: "美丽千岛湖欢迎您"
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        margin-top: .2rem
        line-height: .8rem
        background #eee
        text-indent: .2rem
    .item
        display: flex
        overflow: hidden
        height: 1.9rem
        .item-img
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title
                line-height: .54rem
                font-size: .32rem
                ellipsis()
            .item-desc
                line-height: .4rem
                color: #ccc
                ellipsis()
            .item-button
                line-height: .44rem
                margin-top: .16rem
                background: #ff9300
                padding: 0 .2rem
                border-radius: .06rem
                color: #fff
</style>