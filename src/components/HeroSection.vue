<script setup>
    const image = 'https://preview.colorlib.com/theme/launch/images/market-launch-pana.svg'
    const backgroundImage = 'https://preview.colorlib.com/theme/launch/images/dots.png.webp'
    const heroTitle = 'Promote Your Products by Colorlib'
    const primaryColor = '#0B5ED7'
</script>
<template>
    <div class="container">
        <div class="row my-5">
            <div class="col-5">
                <h1 class="fw-bold text-black mb-5" style="font-size: 4rem">{{ heroTitle }}</h1>
                <p class="text-secondary">
                    Another cool free html css template by <a href="#" class="text-primary" style="text-decoration: none;">Colorlib</a> Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast
                </p>
                <div class="d-grid d-md-block">
                    <button class="btn btn-primary m-1" type="button">See Features</button>
                    <button class="border border-primary btn btn-white text-primary m-1" type="button">Pricing</button>
                </div>
            </div>
            <div class="col-7">
                <img :src="image" alt="">
            </div>
        </div>
    </div>
</template>