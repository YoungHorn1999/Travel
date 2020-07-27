<template>
    <div class="wrapper">
        <swiper ref="mySwiper" :options="swiperOptions" v-if="showSwiper">
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl"/>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    props: {
        list: Array
    },
    data() {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            }
        }
    },
    computed: {
        showSwiper() {
            return this.list.length
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