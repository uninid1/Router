<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
}

nav {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

nav a {
  margin: 0 10px;
  padding: 5px 10px;
  border-radius: 3px;
  background-color: #4CAF50;
  color: white;
  text-decoration: none;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>