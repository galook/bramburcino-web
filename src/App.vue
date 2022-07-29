<template>
  <nav>
    <h1>🥔 Brambůrčino</h1>
  </nav>
  <router-view />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin: 0;
}
nav {
  display: flex;
  flex-direction: row;
  background-color: #2c3e50;
  padding-left: 1rem;
  color: white;
  margin: -8;
}
</style>
