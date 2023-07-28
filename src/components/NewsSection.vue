<script setup>
    import { Icon } from '@iconify/vue';
    const margin = 'margin: 120px 0'
    const bgColor= 'background-color:#F8F9FA'

    const newses = [
        {
            id: 1,
            thumbnail: 'https://preview.colorlib.com/theme/launch/images/person_1.jpg',
            posterName: 'James',
            uploadTime: 'Jun 14, 2020',
            newsTitle: 'Far far away behind the word mountains far from the countries'
        },
        {
            id: 2,
            thumbnail: 'https://preview.colorlib.com/theme/launch/images/person_2.jpg',
            posterName: 'Khan',
            uploadTime: 'Jun 14, 2020',
            newsTitle: 'Far far away behind the word mountains far from the countries'
        },
        {
            id: 3,
            thumbnail: 'https://preview.colorlib.com/theme/launch/images/person_3.jpg',
            posterName: 'Rob',
            uploadTime: 'Jun 14, 2020',
            newsTitle: 'Far far away behind the word mountains far from the countries'
        }
    ]
</script>
<template>
    <div :style="[margin, bgColor]">
        <div class="container py-5">
            <div class="text-center my-4">
                <h1 class="fw-normal">Our News</h1>
                <p class="text-secondary">Far from the countries Vokalia and Consonantia</p>
            </div>
            <div class="row">
                <div class="col-4" v-for="news in newses" :key="id">
                    <div class="card rounded-3 p-2" style="border: none;">
                        <div class="card-body">
                            <div class="row">
                                <div class="col-3">
                                    <img :src="news.thumbnail" :alt="news.posterName" style="width: 100%; border-radius: 50%;">
                                </div>
                                <div class="col-9">
                                    <h4>Posted by {{ news.posterName }}</h4>
                                    <span class="text-secondary">{{ news.uploadTime }}</span>
                                </div>
                            </div>
                            <p class="my-4 text-secondary">Digital Service, 4 min read </p>
                            <h2 class="fw-normal my-3">{{ news.newsTitle }}</h2>
                            <span style="cursor: pointer;"><Icon icon="formkit:arrowright" /></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>