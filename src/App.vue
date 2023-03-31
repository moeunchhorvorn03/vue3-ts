<template>
<div>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/contact">Contact</router-link>
  </nav>
  <router-view/>
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

nav {
  padding: 30px;
  background-color: #2c3e50;
}

nav a {
  text-decoration: none;
  font-weight: bold;
  color: #ffffff;
}

nav a.router-link-exact-active {
  color: #2c3e50;
  background: #ffffff;
  padding: 6px;
}
</style>
