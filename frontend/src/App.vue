<template>
  <div id="app">
    <PaintView />
  </div>
</template>

<script>
import PaintView from '@/components/organisms/PaintView'

export default {
  name: 'App',
  components: {
    PaintView,
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
