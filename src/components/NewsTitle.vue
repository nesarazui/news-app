<template>
    <div>
       <p>
          <a v-bind:href="news.url" target="_blank">{{news.title}}</a>
           
        </p>
        
    </div>
</template>

<script>
export default {
    name: "NewsTitle",
    props: ['news']
}
</script>

<style scoped>

</style>