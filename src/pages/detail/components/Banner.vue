<template>
    <div>
        <div class="banner" @click="handleGallaryClick">
            <img class="banner-img" src="//img1.qunarzz.com/sight/p0/2006/79/795f80bd0c876ba1a3.img.jpg_600x330_243ce664.jpg"/>
            <div class="banner-info">
                <div class="banner-title">
                    杭州乐园（AAAA景区）
                </div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe635;</span>
                    18
                </div>
            </div>
        </div>
        <common-gallary 
            :imgs="imgs" 
            v-show="showGallary"
            @close="handleGallaryClose"
        >
        </common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name: "DetailBanner",
    data () {
        return {
            imgs: [
                'http://img1.qunarzz.com/sight/p0/2006/c7/c704ead5e2f167e4a3.img.jpg_r_800x800_3f24ebd9.jpg',
                'http://img1.qunarzz.com/sight/p0/2006/74/741f3c8b6062c773a3.img.jpg_r_800x800_6c293d77.jpg',
                'http://img1.qunarzz.com/sight/p0/1904/21/2137cf8b388d92b1a3.img.jpg_r_800x800_e817d203.jpg'
            ],
            showGallary: false
        }
    },
    methods: {
        handleGallaryClick () {
            this.showGallary = true
        },
        handleGallaryClose () {
            this.showGallary = false
        }
    },
    components: {
        CommonGallary
    }
}
</script>

<style lang="stylus" scoped>
    .banner 
        position: relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img
            width: 100%
        .banner-info
            position: absolute
            display: flex
            left: 0
            right: 0
            bottom: 0
            line-height: .6rem
            color: #fff
            background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
            .banner-title
                flex: 1
                font-size: .32rem
                padding: 0 .2rem
            .banner-number
                padding: 0 .4rem
                line-height: .32rem
                height: .32rem
                margin-top: .14rem
                border-radius: .2rem
                font-size: .24rem
                background: rgba(0, 0, 0, .8)
                .banner-icon
                    font-size: .24rem
</style>