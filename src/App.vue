<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/playcanvas">Basic</router-link> |
      <router-link to="/physics">Physics</router-link> |
      <router-link to="/tween">TweenJS</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  height: 100%;
}

body {
  overflow-x: hidden;
  margin: 0;
  max-height: 100%;
  height: 100%;
  width: 100%;
  position: relative;
  -webkit-tap-highlight-color: transparent;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  height: 80px;
  width: 100%;
  position: relative;
  top: 0;
  background-color: #fff;
  z-index: 100;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

a.powered-by-playcanvas {
  position: absolute;
  z-index: 100;
  bottom: 1rem;
  right: 1rem;

  img {
    display: block;
    width: 100%;
    height: auto;
  }
}

@media screen and (max-width: 768px) {
  a.powered-by-playcanvas {
    img {
      max-width: 150px;
    }
  }
}
</style>
