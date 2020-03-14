<template>
    <div>
        <button :class="btnclass"
            @click="waktuberkurang()">
            <span class="gotham">
                {{ nomor }}
            </span> 
        </button>

        <b-modal :active.sync="isCardModalActive" :width="640" scroll="keep" v-on:keyup.enter="jawabanbenar">
            <div class="card">
                <div class="card-content">
                    <div class="media">
                        <div class="media-left">
                            <figure class="image is-48x48">
                                <img src="../assets/logotc.png" alt="Image">
                            </figure>
                        </div>
                        <div class="media-content">
                            <p class="title is-4 has-text-black">{{ kategori }}</p>
                            <p class="subtitle is-6">waktu tersisa <strong>{{ waktumenjawab }}</strong>s</p>
                        </div>
                    </div>

                    <div class="content">
                        <div class="block">
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="DICARRY FERRY">
                                DICARRY FERRY
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="CC A">
                                CC A
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="PRINCE ALI">
                                PRINCE ALI
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value= null>
                                
                            </b-radio>
                        </div>
                        <p>
                        <img :src="resolve_img_url(picture_src)" alt="">
                        {{ pertanyaan }}
                        </p>
                        <div class="buttons">
                            <button class="button is-success" @click="jawabanbenar()">
                                Benar
                            </button>
                            <button class="button is-danger" @click="jawabansalah()">
                                Salah
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </b-modal>
    </div>
</template>

<script>
export default {
    props: {
        nomor: String,
        pertanyaan: String,
        kategori: String,
        timPenjawab: String,
        picture_src: String,
        propclick: {
            type: Function
        },
        // btnclass : String
        // waktumenjawab: Number
    },
    data(){
        return{
            isCardModalActive : false,
            btnclass: 'button is-primary',
            waktumenjawab: 60,
            imgsrc: '../assets/logo.png'
        }
    },
    methods:{
        resolve_img_url: function (path) {
            let images = require.context('../assets/', false, /\.png$|\.jpg$/)
            return images("./"+path)
        },
        waktuberkurang(){
            this.imgsrc = this.imgsrc + 'logo.png'
                this.isCardModalActive = true
                if(this.waktumenjawab > 0){
                    var x = setInterval(() => {
                                this.waktumenjawab = this.waktumenjawab - 1
                                if(this.waktumenjawab === 0){
                                    this.isCardModalActive = false
                                    // this.waktumenjawab = 10
                                }
                            }, 1000)
                    // this.waktumenjawab = 10
                } else {
                    this.waktumenjawab = 60
                }
            
        },
        jawabanbenar(){
            if(this.timPenjawab === "DICARRY FERRY"){
                this.nomor = "DICARRY FERRY"
                this.btnclass = "button is-danger"
            } else if(this.timPenjawab === "CC A"){
                this.nomor = "CC A"
                this.btnclass = "button is-warning"
            } else if(this.timPenjawab === "PRINCE ALI"){
                this.nomor = "PRINCE ALI"
                this.btnclass = "button is-success"
            }
            this.isCardModalActive = false,
            console.log(this.btnclass)
            
        },
        jawabansalah(){
            this.isCardModalActive = false
        }
    }
}
</script>

<style lang="scss">
.content{
    text-align: left;
}
</style>
