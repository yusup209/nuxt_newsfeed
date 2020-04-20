<template>
  <div>
    <TopNav />
    <b-container>
      <nuxt />
    </b-container>
  </div>
</template>

<script>
import TopNav from '@/components/TopNav'

export default {
  name: 'def_layout',
  components: {
    TopNav
  }
}
</script>
