<template>
<div class="container-fluid">
  <div class="row">
    <div class="col-auto p-0">
      <sidebar v-if="isDevTools"></sidebar>
    </div>
    <div class="col">
      <div class="container w-100" id="top-nav">
        <div id="nav" class="pt-3">
          <router-link to="/">Home</router-link> |
          <!-- <router-link to="/about">About</router-link> | -->
          <router-link to="/shelves">Shelves</router-link> |
          <router-link to="/dev-tools">Dev Tools</router-link>
        </div>
      </div>

      <router-view />
    </div>
  </div>

  <!-- <div id="nav" class="pt-3">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/dashboard">Shelves</router-link> |
    <router-link to="/dev-tools">Dev Tools</router-link>
  </div>
  
  <router-view /> -->
</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import Sidebar from './views-dev/Components/Sidebar.vue'
export default {
  data: function(){
    return {

    }
  },
  components: {
    Sidebar
  },
  computed: {
    // Checks if the page is a devTools page
    // Loads sidebar if a devtools page
    isDevTools: function(){
      return this.$route.name === 'Dev Tools - :shelf' || this.$route.name === 'Dev Tools'
    }
  }
}
</script>