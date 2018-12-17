<template>
  <section class="container">
    <div>
      <h1 class="title">
        Nuxt Catalog Page
      </h1>
      <link-button to="/">Default</link-button>
      <link-button to="/" theme="red">Red</link-button>
      <link-button to="/" theme="blue">Blue</link-button>
      <link-button to="/" theme="black">Black</link-button>
      <link-button to="/" theme="blue" :disabled="true">Disabled</link-button>
    </div>
  </section>
</template>

<script>
import LinkButton from '~/components/LinkButton.vue'

export default {
  components: {
    LinkButton
  }
}
</script>

<style>
.container {
  display: flex;
  justify-content: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 80px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
