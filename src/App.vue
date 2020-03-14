<template>
  <div id="app" class="container">

    <h1 class="title has-text-centered">
      Final EEC <br>
      <!-- <span id="minutes">{{ minutes }}</span>
      <span id="middle">:</span>
      <span id="seconds">{{ seconds }}</span> -->
    </h1>

    <!-- <Timer date="03 April 2020 21:00"></Timer> -->

    <div class="buttons flex-center">
      <btn-pertanyaan nomor=1 kategori="Fisika" pertanyaan=" Suatu muatan 3 mC awalnya diam kemudian diberi tegangan 1,5 V. Karenanya,  muatan itu bergerak memasuki daerah dengan medan magnet homogennya sebesar 300 mT. Jika massa muatan tersebut adalah 1 gram, gaya magnet yang akan dialami oleh muatan itu adalah sebesar … N" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      
      <btn-pertanyaan nomor=2 kategori="Fisika" pertanyaan="Sebuah muatan +4 nC berada pada titik asal dan sebuah muatan -9 nC berada pada x=2 cm. Jika diletakkan sebuah proton, pada titik koordinat x mana gaya total  yang dialami proton adalah nol?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan nomor=3 kategori="Fisika" pertanyaan=" Sebuah muatan titik sebesar 1,8 µC terletak di tengah-tengah sebuah kubus dengan rusuk 27.5 cm. Hitung fluks listrik yang menembus permukaan kubus tersebut?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan nomor=4 kategori="Fisika" pertanyaan=" Sebuah bola kuningan berdiameter 2 cm diberi muatan sebesar 2 nC. Berapakah besar medan listrik di permukaannya?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>


      <btn-pertanyaan nomor=5 kategori="fisika" pertanyaan="Konduktor dengan panjang 35 m memiliki hambatan sebesar 21 ohm dan memiliki luasan penampang sebesar 1 mm2. Hitung konduktivitas konduktor tersebut!" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan nomor=6 kategori="fisika" pertanyaan="Hitung panjang kawat tembaga yang memiliki diameter 2 mm dan resistansi 2 ohm, apabila konduktivitas tembaga bernilai 5,8 x 107 S/m !" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan nomor=7 kategori="fisika" pertanyaan="Sepotong kawat yang berpotongan melintang seragam memiliki resistansi 0,6 Ω. Jika panjang kawat diubah menjadi tiga kali mula mula dan diameter diubah menjadi dua kali mula mula, maka berapakah nilai resistansinya setelah dilakukan perubahan terhadap diameter dan panjang kawat? (Temperatur dianggap konstan)" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan nomor=8 kategori="fisika" pertanyaan="Kuat medan listrik pada titik berjarak 2 cm dari sebuah bola berdiameter 1 cm adalah 50.000 N/C. Berapakah besar muatan (dalam nC) bola?" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      
    </div>
  </div>
</template>

<script>
import BtnPertanyaan from './components/ButtonPertanyaan.vue'
import Timer from './components/Timer'

export default {
  name: 'App',
  components: {
    BtnPertanyaan,
    Timer
  },
  data(){
    return{
      timpenjawab: null,
      timer: null,
      totalTime: 25 * 60,
      resetButton: false,
      timclass: 'button',
    }
  },
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
.buttons {
  display: inline
}
</style>
