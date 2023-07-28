<script setup>
    const margin = 'margin: 120px 0'
    const aboutImage = 'https://preview.colorlib.com/theme/launch/images/about.svg'
    const aboutsecondaryTitle = 'About'
    const aboutTitle = 'About Us'
    const aboutDescription = "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast <br><br> Separated they <span style='background-color: #F2F6FF'>live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia."
    const features = [
        {symbol:'✓', title:'There live the blind texts'},
        {symbol:'✓', title:'Far far away behind the word'},
        {symbol:'✓', title:'Their place and supplies'}
    ]
    const member = 59
    const team = 14
</script>
<template>
    <div :style="margin">
        <div class="container" id="about">
            <div class="row">
                <div class="col-lg-8 col-md-8 col-sm-8 my-4">
                    <img :src="aboutImage" :alt="aboutTitle">
                </div>
                <div class="col-lg-4 col-md-4 col-sm-4">
                    <p class="fw-bold text-primary">{{ aboutsecondaryTitle }}</p>
                    <h2 class="mb-4">{{ aboutTitle }}</h2>
                    <p v-html="aboutDescription" class="my-4"></p>
    
                    <div v-for="feature in features" :key="index" class="my-3">
                        <span class="text-primary">{{ feature.symbol }}</span> {{ feature.title }}
                    </div>
                    <div class="row my-5">
                        <div class="col-6">
                            <h2>{{ member }}M</h2>
                            <p>MEMBERS</p>
                        </div>
                        <div class="col-6">
                            <h2>{{ team }}</h2>
                            <p>TEAM</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>