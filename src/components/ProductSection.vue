<script setup>
    import { Icon } from '@iconify/vue';
    const sliderImage = 'https://preview.colorlib.com/theme/launch/images/dashboard.jpg.webp'
    const margin = 'margin: 120px 0'

    const features = [

        {
            id:1, 
            icon:'bi:app-indicator', 
            title:'Grow Your Business', 
            content:'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
            bgColor: 'background-color:#6FE7DD'
        },

        {
            id:2, 
            icon:'bi:arrow-repeat', 
            title:'Build Products', 
            content:'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
            bgColor:'background-color:#FFC93C'
        },

        {
            id:3, 
            icon:'ph:briefcase', 
            title:'Success Every Day', 
            content:'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
            bgColor:'background-color:#F73859'
        },

        {
            id:4, 
            icon:'bi:collection', 
            title:'Bring Ideas to Life', 
            content:'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
            bgColor:'background-color:#407BFF'
        }

    ]

</script>

<template>
    <div :style="margin">
        <div class="container">
            <div class="text-center my-5">
                <h1>Advantage of using our products</h1>
                <p class="text-secondary">Far from the countries Vokalia and Consonantia</p>
            </div>
            <div class="row">
                <div class="col-6" v-for="feature in features" :key="id">
                    <div class="row">
                        <div class="col-2 my-4">
                            <span :style="feature.bgColor" class="m-1 p-3 rounded-4"><Icon :icon="feature.icon" width="30" height="30" color="white" /></span>
                        </div>
                        <div class="col-10 my-3">
                            <h3 style="font-weight: 500; font-size: 18px;">{{ feature.title }}</h3>
                            <p style="color: #777;">{{ feature.content }}</p>
                            <a href="#" style="text-decoration: none;">Learn More</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped></style>