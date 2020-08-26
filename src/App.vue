<template>
  <div id="app">
    <div id="nav">
      <nav-bar/>
    </div>
    <div>
      <router-view/>
    </div>
    <Footer />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar/NavBar.vue'
import Footer from '@/components/Footer/Footer.vue'
export default {
  name: 'App',
  components: {
    NavBar,
    Footer
  }
}
</script>
<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.side-color {
    color: #50BE8C;
}

.sub-color {
    color: #566371;
}

.content {
  min-height: 85vh;
}

.post-title {
  color: #343F4A;
}

.post-sub-title {
  color: #566371;
}

.button-color {
  background-color: #50BE8C;
}
</style>
