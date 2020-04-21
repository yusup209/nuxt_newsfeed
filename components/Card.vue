<template>
  <div>
    <b-card
      :img-src="img"
      img-alt="Image"
      img-top
    >
      <b-card-text class="text-bold">
        <a :href="url" target="_blank">{{ title }}</a>
      </b-card-text>
      <b-card-text class="small text-muted">{{ author }} - {{ source }}</b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['img', 'title', 'author', 'source', 'url']
}
</script>

<style scoped>
  b-card{
    height: 405px
  }
  .card-img-top{
    height: 231px,
  }
</style>
