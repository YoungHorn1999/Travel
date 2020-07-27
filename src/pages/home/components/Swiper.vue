<template>
    <div class="wrapper">
        <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl"/>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data() {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [
                {
                    id: "0001",
                    imgUrl: require("../../../assets/img/1.jpg")
                },
                {
                    id: "0002",
                    imgUrl: require("../../../assets/img/2.jpg")
                }
            ]
        }
    }
}
</script>

<style scoped lang="stylus">
    .wrapper >>> .swiper-pagination-bullet-active
        background #fff
        overflow: hidden
    .wrapper
        width: 100%
        height: 37vw
        .swiper-img 
            width: 100%
</style>