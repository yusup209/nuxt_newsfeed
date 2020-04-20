<template>
  <b-row class="margin-top: 15px">
    <b-col md="4" class="margin-top: 15px">
        <Card />
        <p>
          {{articles}}
        </p>
    </b-col>
  </b-row>
</template>

<script>
import Card from '@/components/Card'

export default {
  async asyncData ({ app }) {
    const { articles } = await app.axios.$get('http://newsapi.org/v2/top-headlines?country=id&apiKey=e54e9c04ae504667a7e5a37e79c71921')

    return { articles }
  },
  name: 'CardLists',
  components: {
    Card
  }
}
</script>
