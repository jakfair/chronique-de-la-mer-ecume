<template>
  <router-view id="app" v-slot="{ Component }">
    <div id="content"
         @scroll="handleScroll">
      <nav>
        <router-link to="/">Home</router-link>
        |
        <router-link to="/about">About</router-link>
      </nav>
      <transition name="route" mode="out-in">
        <component :is="Component"></component>
      </transition>
    </div>
    <div class="background">
      <div class="background_wrapper">
        <div class="background_montain" id="bg_1"/>
        <div class="background_montain" id="bg_2"/>
        <img class="background_montain bg_3" src="~@/assets/fond_montagne/clouds_bg.png"/>
        <img class="background_montain bg_4" src="~@/assets/fond_montagne/glacial_mountains.png"/>
        <img class="background_montain bg_5" src="~@/assets/fond_montagne/clouds_mg_3.png"/>
        <img class="background_montain bg_6" src="~@/assets/fond_montagne/clouds_mg_2.png"/>
        <img class="background_montain bg_7" src="~@/assets/fond_montagne/clouds_mg_1.png"/>
      </div>
    </div>
  </router-view>
</template>

<script>
export default {
  methods: {
    handleScroll() {
      var scrollTop = document.getElementById('content').scrollTop
      document.getElementById('bg_1').style.transform = "translate(0," + scrollTop + "px)";
      document.getElementById('bg_2').style.transform = "translate(0," + scrollTop*2 + "px)";
    }
  }
}
</script>
<style>
#app {
  position: relative;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  min-height: 100vh;
}

#content {
  position: absolute;
  z-index: 2;
  height: 50vh;
  width: 100vw;
  overflow: scroll;
}

.background {
  position: absolute;
  z-index: 1;
}

.background_wrapper {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.background_montain {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
}

#bg_1 {
  background: url(~@/assets/fond_montagne/sky.png) center center;
  background-size: cover;
}

#bg_2 {
  background: url(~@/assets/fond_montagne/cloud_lonely.png) center center;
  background-size: cover;
}

@keyframes scaler {
  100% {
    transform: scale3d(1, 1, 1);
    opacity: 1;
  }
}

@media (prefers-reduced-motion: no-preference) {
  .background_montain-animation {
    animation-name: scaler;
    animation-duration: 1s;
    animation-iteration-count: 1;
  }
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}

.route-enter-active {
  transition: ass 1s ease-out;
}

.route-leave-to {
  opacity: 0;
  transform: translateX(100px);
}

.route-leave-active {
  transition: all 1s ease-in;
}
</style>
