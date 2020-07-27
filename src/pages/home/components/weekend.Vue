<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl"/>
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "HomeWeekend",
    data () {
        return {
            recommendList: [
                {
                    id: "0001",
                    imgUrl: "http://img1.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg",
                    title: '美丽普陀山',
                    desc: "人间仙境杭州，佛教圣地普陀山等你来玩！在这里静心接收佛家的洗礼，用心感受佛文化"
                },
                {
                    id: "0002",
                    imgUrl: "http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg",
                    title: '承载杭城的历史之地',
                    desc: "饱经沧桑的地方诉述着这座城的段段衷肠"
                },
                {
                    id: "0003",
                    imgUrl: "http://img1.qunarzz.com/sight/source/1505/c1/1178c5696fcf57.jpg_r_640x214_a69542c6.jpg",
                    title: '杭州江南古镇',
                    desc: "古镇岂只有新叶？悠闲出游杭州古镇"
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
    .item-img-wrapper
        height: 0
        overflow: hidden
        padding-bottom: 33.9%
        .item-img
            width: 100%
    .item-info
        padding: .1rem
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
</style>