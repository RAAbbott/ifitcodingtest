<template>
  <div id="app" @click="handler">
    <Header/>
    <Home/>
    <Footer/>
  </div>
</template>

<script>
import Home from './views/Home.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import { EventBus as bus } from './shared/eventBus';

export default {
  components: {
    Home,
    Header,
    Footer
  },

  methods: {
    handler(event) {
      bus.$emit('bodyClick', event);
    }
  }
}
</script>

<style>
#app {
  font-family: proxima-nova,Helvetica Neue,Helvetica,Arial,sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 13px;
  font-weight: 500;
  overflow-x: hidden;
}
</style>
