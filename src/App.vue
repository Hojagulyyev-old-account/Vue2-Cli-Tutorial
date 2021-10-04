<template>
  <div id="mainapp">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link :to="{ name: 'Article'}">Articles</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style scoped>

#mainapp {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  text-align: center;
}

#nav router-link {
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  margin: 0px 5px;
}

#nav a.router-link-exact-active {
  color: #ca3c3c;
}
</style>
