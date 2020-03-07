<template>
  <div id="app" class="container">

    <h1 class="title has-text-centered">
      Final EEC
    </h1>

    <div class="buttons flex-center">
      <btn-pertanyaan nomor=1 pertanyaan="hello"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=1 pertanyaan="hello"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=1 pertanyaan="hello"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
    </div>
  </div>
</template>

<script>
import BtnPertanyaan from './components/ButtonPertanyaan.vue'

export default {
  name: 'App',
  components: {
    BtnPertanyaan
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
