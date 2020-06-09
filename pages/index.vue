<template>
  <div class="container">
    <nav-menu></nav-menu>
    <div>
      <h1 class="title">
        srmorante.dev
      </h1>
      <h2 class="subtitle">
        Welcome to my personal page
      </h2>
      <div class="links">
        <nuxt-link to="/404" class="button--green">
          Under Construction 🏗
        </nuxt-link>
        <a
          href="https://github.com/srgmorante"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import NavMenu from '~/components/NavMenu'
export default {
  components: {
    NavMenu
  },
  head() {
    return {
      title: 'Welcome to Sergio Morante page'
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
