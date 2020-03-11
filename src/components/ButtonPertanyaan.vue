<template>
    <div>
        <button class="button is-primary is-medium"
            @click="isCardModalActive = true">
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
                            <p class="subtitle is-6">waktu tersisa <strong>60</strong>s</p>
                        </div>
                    </div>

                    <div class="content">
                        <p>
                        {{ pertanyaan }}
                        </p>
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
        waktumenjawab: Number
    },
    data(){
        return{
            isCardModalActive : false,
            waktumenjawab: 60
        }
    }
}
</script>