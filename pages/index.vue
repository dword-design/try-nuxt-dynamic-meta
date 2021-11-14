<template>
  <div>
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  asyncData() {
    // fetch the data from somewhere
    return { title: 'Title for product', description: 'Description for product' }
  },
  head() {
    return {
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.description,
        },
        {
          hid: 'og:description',
          name: 'og:escription',
          content: this.description,
        },
      ]
    }
  }
}
</script>
