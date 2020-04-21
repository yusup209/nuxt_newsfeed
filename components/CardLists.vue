<template>
  <b-row class="margin-top: 15px">
    <b-col md="4" class="margin-top: 15px" v-for="(article, index) in articles" :key="index">
        <Card
        :img="article.urlToImage"
        :title="article.title"
        :author="article.author"
        :source="article.source.name"
        :url="article.url"/>
      <!-- <p>{{ article.title }}</p> -->
    </b-col>
  </b-row>
</template>

<script>
import Card from '@/components/Card'

export default {
  name: 'CardLists',
  components: {
    Card
  },
  data () {
    return {
      articles: null
    }
  },
  mounted () {
    // axios.$get('http://newsapi.org/v2/top-headlines?country=id&apiKey=e54e9c04ae504667a7e5a37e79c71921').then(res => (this.articles = res))
    // fetch('http://newsapi.org/v2/top-headlines?country=id&apiKey=e54e9c04ae504667a7e5a37e79c71921').then(res => res.json()).then(data => console.log(data.articles))
    fetch('http://newsapi.org/v2/top-headlines?country=id&apiKey=e54e9c04ae504667a7e5a37e79c71921').then(res => res.json()).then(data => (this.articles = data.articles))
    console.log('hello')
  }
}
</script>
