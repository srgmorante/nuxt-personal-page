<template>
  <nav>
    <h1>srmorante.dev</h1>
    <ul>
      <li v-for="route in routes" :key="route.name">
        <nuxt-link
          class="{'nuxt-link-active': isRouteActive(id)} menu-item"
          :to="route.path"
          >{{ route.name }}</nuxt-link
        >
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data: () => ({
    routes: [
      { path: '/', name: 'Home' },
      { path: '/about', name: 'About' },
      { path: '/projects', name: 'Projects' }
    ]
  }),
  methods: {
    isRouteActive(id) {
      return this.$route.path.includes(id) || false
    }
  }
}
</script>

<style>
nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 1rem;
  display: inline-flex;
  align-items: center;
  justify-content: space-between;
  color: white;
  background-color: #35495e;
}
nav > ul {
  list-style: none;
  display: flex;
  padding: 0;
}
.menu-item {
  text-decoration: none;
  color: white;
  margin: 0 0.5rem;
}

.nuxt-link-active,
.menu-item:hover {
  text-decoration: underline;
}
</style>
