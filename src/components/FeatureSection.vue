<script setup>
    const highlightText = 'DIGITAL SERVICES'
    const image = 'https://preview.colorlib.com/theme/launch/images/dashboard.jpg.webp'
    const video = 'https://www.youtube.com/watch?v=6mttwIBcig0'
    const featureTitle = 'Selling Digital <br /> Services'
    const featureParagraph = 'Far far away, behind the word mountains, far <br /> from the countries Vokalia and Consonantia, <br /> there live the blind texts. Separated they live in <br /> Bookmarksgrove right at the coast'

    const ticks = [
        {id: 1, symbol: '✓', line: 'There live the blind texts'},
        {id: 2, symbol: '✓', line: 'Far far away behind the word'}
    ]

    const auth = {
        image: 'https://preview.colorlib.com/theme/launch/images/person_1.jpg',
        name: 'James Anderson',
        position: 'Facebook, Product Lead',
        message: '"<i>Separated they live in Bookmarksgrove right at <br /> the coast of the Semantics, a large language <br /> ocean. A small river named Duden flows by their <br /> place and supplies it with the necessary <br /> regelialia.<i/>"'
    }
</script>
<template>
    <div class="container" id="features">
        <div class="row my-5 d-flex align-items-center">
            <div class="col-lg-5 col-md-5 col-sm-5">
                <h6 class="text-primary">{{ highlightText }}</h6>
                <h1 class="text-black mb-4" v-html="featureTitle"></h1>
                <p class="text-secondary text-secondary" v-html="featureParagraph"></p>

                <div class="my-3">
                    <div v-for="tick in ticks" :key="id" class="tickmark">
                        <P>{{ tick.symbol }} <span>{{ tick.line }}</span></P>
                    </div>
                </div>

                <p class="text-secondary text-black" v-html="auth.message"></p>

                <div class="row my-4">
                    <div class="col-2">
                        <img style="max-width: 100%; border-radius: 50%;" :src="auth.image" alt="">
                    </div>
                    <div class="col-10">
                        {{ auth.name }} <br>
                        {{ auth.position }}
                    </div>
                </div>
                
            </div>
            <div class="col-lg-7 col-md-7 col-sm-7">
                <div class="border border-5">
                    <video controls :poster="image">
                        <source :src="video" type="video/mp4">
                        <source :src="video" type="video/ogg">
                        <source :src="video" type="video/webm">
                    </video>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container {
        margin-top: 250px;
    }

    video {
        max-width: 100%;
    }

    .thumbnail {
        width: 100px;
        height: 100px;
        border: 1px solid #ddd;
        margin: 10px;
    }

    .tickmark p {
        color: #2489FD;
    }
    .tickmark span {
        color: #000;
    }
</style>