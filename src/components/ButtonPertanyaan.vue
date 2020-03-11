<template>
    <div>
        <button :class="btnclass"
            @click="isCardModalActive = true, waktuberkurang(), startTimer()">
            {{ nomor }}
        </button>

        <b-modal :active.sync="isCardModalActive" :width="640" scroll="keep">
            <div class="card">
                <div class="card-content">
                    <div class="media">
                        <div class="media-left">
                            <figure class="image is-48x48">
                                <img src="../assets/logotc.png" alt="Image">
                            </figure>
                        </div>
                        <div class="media-content">
                            <p class="title is-4">{{ timPenjawab }}</p>
                            <p class="subtitle is-6">waktu tersisa <strong>{{ waktumenjawab }}</strong>s</p>
                        </div>
                    </div>

                    <div class="content">
                        <p>
                        {{ pertanyaan }}
                        </p>
                        <div class="buttons">
                            <button class="button is-success" @click="jawabanbenar()">
                                Benar
                            </button>
                            <button class="button is-danger" @click="salah()">
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
        nomor: Number,
        pertanyaan: String,
        kategori: String,
        timPenjawab: String,
        propclick: Function
        // waktumenjawab: Number
    },
    data(){
        return{
            isCardModalActive : false,
            btnclass: 'button is-primary',
            waktumenjawab: 10
        }
    },
    methods:{
        waktuberkurang(){
            if(this.waktumenjawab > 0){
                setInterval(() => {
                    this.waktumenjawab = this.waktumenjawab - 1
                }, 1000)
            } else {
                this.isCardModalActive = false
            }
        },
        jawabanbenar(){
            this.btnclass = 'button is-info',
            this.isCardModalActive = false,
            console.log(this.btnclass)
        }
    }
}
</script>