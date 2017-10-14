<template>
  <div>数据请求失败</div>
</template>
<script>
    import { HEADDATA } from '../store/action_type'
    import {mapActions } from "vuex";
    export default {
        name: 'index',
        data() {
            return {}
        },
        created() {
            this.headdataFn(this)
            console.log(HEADDATA)
        },
        methods: {
            ...mapActions({
                headdataFn: HEADDATA.actions
            })
        }
    }
</script>
<style scoped>
    ul {font-size: 0.4rem}
    .mint-loadmore { font-size: 0.48rem }
</style>