<template>
  <div id="app">
    <ImageParentComponent>
    </ImageParentComponent>
  </div>
</template>

<script>
import ImageParentComponent from './components/ImageParentComponent.vue'

export default {
  name: 'App',
  components: {
    ImageParentComponent,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
