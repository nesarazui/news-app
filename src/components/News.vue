<template>
    <div>
        <h1>Top News</h1>
        <div v-bind:key="news.id" v-for="news in news">
            <NewsTitle v-bind:news="news"/>
            </div>
    </div>
</template>

<script>
import NewsTitle from './NewsTitle.vue'

export default {
    name: "News",
    components: {NewsTitle},
    props: ["news"]
}
</script>

<style lang="less" scoped>

</style>