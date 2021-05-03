<template>
  <div id="app">
    <div id="nav">
      <div :style="{ color: navbarColors[$route.path] }">Custom text in the navbar:</div>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      navbarColors: {
        '/': 'red',
        '/about': 'blue',
      },
    }
  },
}
</script>
