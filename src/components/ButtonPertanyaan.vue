<template>
    <div>
        <button :class="btnclass"
            @click="waktuberkurang(), startTimer()">
            {{ nomor }}
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
                            <p class="title is-4">{{ kategori }}</p>
                            <p class="subtitle is-6">waktu tersisa <strong>{{ waktumenjawab }}</strong>s</p>
                        </div>
                    </div>

                    <div class="content">
                        <div class="block">
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="A">
                                A
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="B">
                                B
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value="C">
                                C
                            </b-radio>
                            <b-radio v-model="timPenjawab"
                                name="name"
                                native-value= null>
                                
                            </b-radio>
                        </div>
                        <p>
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
        propclick: Function,
        btnclass : String
        // waktumenjawab: Number
    },
    data(){
        return{
            isCardModalActive : false,
            // btnclass: 'button is-primary',
            waktumenjawab: 10
        }
    },
    methods:{
        waktuberkurang(){
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
            if(this.timPenjawab === "A"){
                this.nomor = "A"
                this.btnclass = "button is-dark"
            } else if(this.timPenjawab === "B"){
                this.nomor = "B"
                this.btnclass = "button is-dark"
            } else if(this.timPenjawab === "C"){
                this.nomor = "C"
                this.btnclass = "button is-dark"
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