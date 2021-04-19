<template>
    <div class="mt-12 text-left">
        <header class="font-bold text-left text-2xl mb-2">Articles</header>
        <div v-for="article in articles" v-bind:key="article.id">
            {{ article.title }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            articles: []
        }
    },
    methods: {
        async fetchArticles() {
            try {
                const axios = require('axios');
                const url = 'https://dev.to/api/articles?username=chadriae'
                const response = await axios.get(url)
                this.articles = response.data
                console.log(this.articles)
          }
          catch (error){
              console.log(error)
          }
        }
    },
    mounted() {
        this.fetchArticles();
    }
}
</script>

<style scoped>

</style>
