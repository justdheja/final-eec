<template>
  <div id="app" class="container">

    <h1 class="title has-text-centered">
      Final EEC
    </h1>

    <div class="block">
        <b-radio v-model="timpenjawab"
            name="name"
            native-value="Flint">
            Flint
        </b-radio>
        <b-radio v-model="timpenjawab"
            name="name"
            native-value="Silver">
            Silver
        </b-radio>
    </div>

    <div class="buttons flex-center">
      <btn-pertanyaan nomor=1 pertanyaan="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Recusandae sed quo dicta odit. Ipsa, quisquam. Maiores, temporibus libero facere porro dolorum esse explicabo eum iusto amet quibusdam, facilis suscipit pariatur." waktumenjawab=90 :timPenjawab="timpenjawab"></btn-pertanyaan>
      <btn-pertanyaan nomor=2 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=3 pertanyaan="hello"></btn-pertanyaan>
      <btn-pertanyaan nomor=4 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=5 pertanyaan="hello"></btn-pertanyaan>
      <btn-pertanyaan nomor=6 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=7 pertanyaan="hallo"></btn-pertanyaan>
      <btn-pertanyaan nomor=8 pertanyaan="hallo"></btn-pertanyaan>
    </div>
  </div>
</template>

<script>
import BtnPertanyaan from './components/ButtonPertanyaan.vue'

export default {
  name: 'App',
  components: {
    BtnPertanyaan
  },
  data(){
    return{
      timpenjawab: ''
    }
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
