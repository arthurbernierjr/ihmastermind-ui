<template lang="html">
  <div>
    <b-card
      title="Card Title"
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
    >
      <b-card-text
        v-html="article.excerpt.rendered"
      >
      </b-card-text>

      <b-button
        :href="`/${article.slug}`"
        variant="primary"
      >
        Go to Article
      </b-button>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'article-card',
  props: {
    article: {
      type: Object,
      required: true,
      default: () => ({})
    }
  }
}
</script>

<style lang="css" scoped>
</style>
