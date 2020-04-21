<template>
  <div>
    <TopNav />
    <b-container>
      <nuxt />
      <Footer />
    </b-container>
  </div>
</template>

<script>
import TopNav from '@/components/TopNav'
import Footer from '@/components/Footer'

export default {
  name: 'def_layout',
  components: {
    TopNav,
    Footer
  }
}
</script>
