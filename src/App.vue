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

      <btn-pertanyaan picture_src="3.png" nomor=3 kategori="Komputer" pertanyaan="Seorang polisi sedang menginterogasi beberapa orang terduga kasus pencurian permata magis, dan mendapat hasil seperti di gambar. Jumlah pencuri dari keterangan para terduga adalah?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="4.png" nomor=4 kategori="Komputer" pertanyaan="Lima orang sahabat, Akkun, Becchan, Cesan, Didono, dan Essama melakukan kompetisi mengumpulkan sampah yang berserakan karena mereka cinta lingkungan. Juaranya adalah yang berhasil mengumpulkan sampah terbanyak dalam waktu 2 jam.Terdapat hasil seperti di gambar. Urutan juara yang memungkinkan adalah…" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="5.png" nomor=5 kategori="Komputer" pertanyaan="Perhatikan source code pada gambar. Berapa kali fungsi ini dipanggil dari ini(39)?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan picture_src="null.png" nomor=6 kategori="Komputer" pertanyaan=" Di laboratorium milik Ayah, aku ingat beliau pernah mengembangbiakkan sejenis mikroorganisme yang membelah diri setiap 1 tahun dan tidak akan mati. Saat itu umur ayah masih 33 tahun saat beliau memulai mengembangbiakkan organisme terseut. Saat ini umur ayah 115 tahun. Beliau sudah sakit-sakitan. Beliau menyampaikan pesan “bagilah mikroorganisme yang kukembangbiakkan. Buatlah 1 kelompok pada tiap harinya selama 1 minggu, dengan jumlah yang sama rata. Kemudian, bawakan sisanya kepadaku.” Minggu berikutnya aku memberikan sisa mikroorganisme yang tidak mendapat kelompok, dan sisanya adalah 2. Ternyata hal tersebut beliau lakukan agar dapat mengetahui berapa jumlah mikroorganisme pada saat awal beliau memulai pengembangbiakkan. Berapakah jumlahnya?"  :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="null.png" nomor=7 kategori="Komputer" pertanyaan="Wisnu memiliki sekumpulan kantong yang berisi koin isi masing-masing kantong tersebut adalah sebagai berikut K = {23,12,34,64,78,5,13,10,16,56,48,96,25,71,57}, Kantong-kantong tersebut akan dimasukan ke sebuah sistem lubang sehingga kantong-kantong tersebut akan tersusun rapi membentuk sebuah balanced binary tree. Bagaimana urutan kantong yang harus dimasukan ke sistem lubang tersebut?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

    </div>

    <!-- no 8 - 14 -->

    <div class="buttons flex-center">
      <btn-pertanyaan picture_src="null.png" nomor=8 kategori="Komputer" pertanyaan="Yusuf memiliki 245 pasang kaus kaki, kaus kaki tersebut terdiri atas warna merah, jingga, kuning, hijau, biru sama banyak, nila dan ungu. Pada bulan Desember Yusuf akan mengikuti sebuah perlombaan berupa perjalanan 100km berjalan kaki dengan perbekalan yang ada. Pagi hari saat perlombaan dimulai Yusuf bangun terlabat. Sehingga dia terburu-buru dan langsung mengambil banyak kaus kaki, berapa banyak kaus kaki minimal yang harus diambil agar terdapat minimal ada 2 pasang kaus kaki yang berbeda warna?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="9.png" nomor=9 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="10.png" nomor=10 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="11.png" nomor=11 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="12.png" nomor=12 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

      <btn-pertanyaan picture_src="13.png" nomor=13 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>
      
      <btn-pertanyaan picture_src="14.png" nomor=14 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

    </div>

    <!-- no 15 - 21 -->
      <div class="buttons flex-center">
        <btn-pertanyaan picture_src="15.png" nomor=15 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=16 kategori="Matematika" pertanyaan=" Pada suatu segita ABC , sudut C 3 kali lebih besar dari sudut A , dan sudut B 2 kali lebih besar dari sudut A. Maka perbandinagn (rasio) antara panjang AB dengan BC adalah ..." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="17.jpg" nomor=17 kategori="Komputer" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>



      </div>
    <!-- no 22 - 28 -->
      <div class="buttons flex-center">
        <btn-pertanyaan picture_src="null.png" nomor=22 kategori="Komputer" pertanyaan="Berapakah angka ketiga dari belakang yang bukan nol dari 18! ? (dimulai dari angka yang bukan nol adalah angka pertama)?."  :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=23 kategori="fisika" pertanyaan="Captain America melempar tamengnya yang memiliki berat 100 gr dari ketinggian 1 meter dari atas tanah dengan kecepatan 12 m/s. Ketika tamengnya mencapai ketinggian 2 meter, kecepatannya 8 m/s. Berapa pengurangan energi mekanik di sistem tersebut karena adanya gaya hambat?
        ." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="24.png" nomor=24 kategori="Komputer" pertanyaan="Apa keluaran dari program tersebut jika inputnya adalah 257,254,232?"></btn-pertanyaan>


        <btn-pertanyaan picture_src="null.png" nomor=25 kategori="Fisika" pertanyaan="Sebuah bola dilempar ke bawah dengan kecepatan 15 m/s dari ketinggian 60 m. Berapa kecepatan benda setelah energi potensial bola itu berkurang sepertiganya? (g = 10 m/s2)" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="26.png" nomor=26 kategori="Matematika" pertanyaan="Nilai terkecil yang positif dari operasi berikut ini adalah..." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=27 kategori="Matematika" pertanyaan="Sekumpulan data mempunyai rata-rata 12 dan jangkauan 6. Jika setiap nilai data dikurangi dengan a, kemudian hasilnya dibagi dengan b, ternyata menghasilkan data baru dengan rata-rata 2 dan jangkauan 3, maka nilai a + b = …." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=28 kategori="Matematika" pertanyaan="Dalam suatu segitiga ABC , diketahui sudut BAC= 55 , sudut ACB = 75 (dalam derajat) . D terletak pada sisi AB dan E pada sisi BC . Jika DB = BE , maka sudut BED (dalam derajat) adalah … " :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>



      </div>
    <!-- no 29 - 35 -->
      <div class="buttons flex-center">
        <btn-pertanyaan picture_src="null.png" nomor=29 kategori="Fisika" pertanyaan="Pada suatu hari, awan petir setinggi 1,77 km menyelimuti suatu wilayah di bumi. Awan petir dan tanah kemudian seakan-akan menjadi sebuah kapasitor. Beda potensial antara petir dan tanah adalah 30 kV dan terdeteksi ada muatan sebesar 270 nC di udara. Berapakah luas awan tersebut?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=30 kategori="Fisika" pertanyaan="Seseorang di planet bumi dapat melompat setinggi 1 m. Di planet dengan massa jenis dua per tiga dari bumi dan jari-jari dua kali bumi, berapakah tinggi orang tersebut dapat melompat? (Anggaplah dia mensuplai energi yang sama di kedua planet)" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="31.png" nomor=31 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="32.png" nomor=32 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="33.png" nomor=33 kategori="Matematika" pertanyaan="" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=34 kategori="Matematika" pertanyaan="Dalam suatu papan catur 7x7 terdapat 2 petak yang diwarnai dengan warna merah. 47 petak sisanya akan diwarnai dengan warna putih. 2 susunan warna dapat dianggap sama jika satu susunan dapat diperoleh melalui rotasi dari susunan kedua. Berapa banyak susunan warna berbeda yang mungkin pada papan catur tersebut?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>

        <btn-pertanyaan picture_src="null.png" nomor=35 kategori="Matematika" pertanyaan="Diberikan 2 buah kotak yang diisi oleh kelereng putih dan hitam. Total jumlah kelereng dari kedua kotak tersebut adalah 25 buah. Jika kita mengambil 1 kelereng pada masing-masing kotak, maka probabilitas kelereng yang terambil keduanya berwarna hitam adalah 17/25. Berapa probabilitas jika yang termbil keduanya adalah kelereng putih?" :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="this.clickhandler"></btn-pertanyaan>


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
