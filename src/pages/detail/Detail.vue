<template>
    <div>
        <detail-banner 
            :sightName="sightName"
            :bannerImg="bannerImg"
            :gallaryImgs="gallaryImgs"></detail-banner>
        <detail-header></detail-header>
        <div class="content"></div>
    </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import axios from 'axios'
export default {
    name: "Detail",
    components: {
        DetailBanner,
        DetailHeader
    },
    data () {
        return {
            sightName: '',
            bannerImg: '',
            gallaryImgs: '',
            categoryList: []

        }
    },
    methods: {
        getDetailInfo () {
            axios.get('api/detail.json', {
                params: {
                    id: this.$route.params.id
                }
            }).then(this.handleGetDataSucc)
        },
        handleGetDataSucc (res) {
            res = res.data
            if(res.ret && res.data){
                const data = res.data
                console.log(data)
            }
        }
    },
    mounted () {
        this.getDetailInfo()
    }
}
</script>

<style lang="stylus" scoped>
    .content
        height: 50rem
</style>