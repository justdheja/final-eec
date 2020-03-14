<template>
  <div id="app">
    <div class="container">

    

    <h1 class="title has-text-centered">
      <img src="./assets/logotc.png" alt=""> <br>
      <span class="corporation-games">FINAL EEC</span><br>
      <!-- <span id="minutes">{{ minutes }}</span>
      <span id="middle">:</span>
      <span id="seconds">{{ seconds }}</span> -->
    </h1>

    <!-- <Timer date="03 April 2020 21:00"></Timer> -->

    <!-- no 1 - 7 -->
    <div class="buttons flex-center">
      <btn-pertanyaan picture_src="null.png" nomor=1 kategori="Fisika" pertanyaan=" Suatu muatan 3 mC awalnya diam kemudian diberi tegangan 1,5 V. Karenanya,  muatan itu bergerak memasuki daerah dengan medan magnet homogennya sebesar 300 mT. Jika massa muatan tersebut adalah 1 gram, gaya magnet yang akan dialami oleh muatan itu adalah sebesar … N" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      
      <btn-pertanyaan picture_src="null.png" nomor=2 kategori="Fisika" pertanyaan="Sebuah muatan +4 nC berada pada titik asal dan sebuah muatan -9 nC berada pada x=2 cm. Jika diletakkan sebuah proton, pada titik koordinat x mana gaya total  yang dialami proton adalah nol?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=3 kategori="Fisika" pertanyaan=" Sebuah muatan titik sebesar 1,8 µC terletak di tengah-tengah sebuah kubus dengan rusuk 27.5 cm. Hitung fluks listrik yang menembus permukaan kubus tersebut?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=4 kategori="Fisika" pertanyaan=" Sebuah bola kuningan berdiameter 2 cm diberi muatan sebesar 2 nC. Berapakah besar medan listrik di permukaannya?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>


      <btn-pertanyaan picture_src="null.png" nomor=5 kategori="fisika" pertanyaan="Konduktor dengan panjang 35 m memiliki hambatan sebesar 21 ohm dan memiliki luasan penampang sebesar 1 mm2. Hitung konduktivitas konduktor tersebut!" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan picture_src="null.png" nomor=6 kategori="fisika" pertanyaan="Hitung panjang kawat tembaga yang memiliki diameter 2 mm dan resistansi 2 ohm, apabila konduktivitas tembaga bernilai 5,8 x 107 S/m !" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan picture_src="null.png" nomor=7 kategori="fisika" pertanyaan="Sepotong kawat yang berpotongan melintang seragam memiliki resistansi 0,6 Ω. Jika panjang kawat diubah menjadi tiga kali mula mula dan diameter diubah menjadi dua kali mula mula, maka berapakah nilai resistansinya setelah dilakukan perubahan terhadap diameter dan panjang kawat? (Temperatur dianggap konstan)" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
    </div>

    <!-- no 8 - 14 -->

    <div class="buttons flex-center">
      <btn-pertanyaan picture_src="null.png" nomor=8 kategori="fisika" pertanyaan="Kuat medan listrik pada titik berjarak 2 cm dari sebuah bola berdiameter 1 cm adalah 50.000 N/C. Berapakah besar muatan (dalam nC) bola?" :timPenjawab="timpenjawab"
      :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=9 kategori="Matematika" pertanyaan="Segi enam ABCDEF memiliki sisi-sisi yang sama panjang.  adalah sudut siku-siku, sedangkan keempat sudut sisanya memiliki besar sudut yang sama. Jika luas segi enam ini adalah  , berapakah panjang dari BF?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=10 kategori="Matematika" pertanyaan="Misalkan a, b, dan c adalah suatu bilangan real positif. Jika abc = 2,  ,  . Berapakah nilai yang tepat untuk  ?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=11 kategori="Matematika" pertanyaan="Hitung nilai  " :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=13 kategori="Matematika" pertanyaan=" Hitunglah nilai √(2019^2+4039) √(2019^2+4039)" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=14 kategori="Matematika" pertanyaan="Jika ab=cd=ef=64Tentukan hasil dari 5a2c-4c2e+e35b2d-4d 2f+f 3" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

    </div>

    <!-- no 15 - 21 -->
      <div class="buttons flex-center">
        
      </div>
    <!-- no 22 - 28 -->
      <div class="buttons flex-center">

      </div>
    <!-- no 29 - 35 -->
      <div class="buttons flex-center">

      </div>
    <!-- no 36 - 42 -->
      <div class="buttons flex-center">

      </div>
    <!-- no 43 - 49 -->
      <div class="buttons flex-center">

      </div>
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
    background: #000000;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #434343, #000000);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #434343, #000000); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    height: 100vh;
    // width: 200vh;
    padding-top: 8vh;
}
.buttons {
  display: inline
}
</style>
