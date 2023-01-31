<template>
    <div class="partner-area ptb-100">
        <div class="container">
            <div class="partner-slides">
                <carousel
                    :autoplay="5000"
                    :settings='settings' 
                    :breakpoints='breakpoints'
                >
                    <Slide v-for="slide in carouselItems" :key="slide.id">
                        <div class="partner-card" data-aos="fade-up" data-aos-delay="80" data-aos-duration="800" data-aos-once="true">
                            <div class="image-list">
                                <img :src="slide.image" alt="partner">
                                <img :src="slide.imageHover" alt="partner">
                            </div>
                        </div>
                    </Slide>

                    <template #addons>
                    </template>
                </carousel>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from 'vue';
import { Carousel, Slide  } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';

export default defineComponent ({
    name: 'Partner',
    components: {
        Carousel,
        Slide,
    },
    data: () => ({
        settings: {
            itemsToShow: 1,
            snapAlign: 'center',
        },
        carouselItems: [
            {
                id: 1,
                image: require('../../assets/images/partner/Google.png'),
                imageHover: require('../../assets/images/partner/Google-Hover.png'),
            },
            {
                id: 2,
                image: require('../../assets/images/partner/tests/Discovery-Channel-earth-logo-removebg-preview.png'),
                imageHover: require('../../assets/images/partner/tests/Discovery-Channel-removebg-preview.png'),
            },
            {
                id: 3,
                image: require('../../assets/images/partner/tests/Marshall-removebg-preview.png'),
                imageHover: require('../../assets/images/partner/tests/Marshall-removebg-preview.png'),
            },
            {
                id: 4,
                image: require('../../assets/images/partner/tests/ipic-removebg-preview.png'),
                imageHover: require('../../assets/images/partner/tests/ipic.jpg'),
            },
            {
                id: 5,
                image: require('../../assets/images/partner/tests/Collector_wit_transparant.png'),
                imageHover: require('../../assets/images/partner/tests/60eec41e2d892dada353bab858fc0c3f-removebg-preview.png'),
            },
            {
                id: 6,
                image: require('../../assets/images/partner/tests/AQA_Logo_2020.png'),
                imageHover: require('../../assets/images/partner/tests/assessment-and-qualifications-alliance-aqa-logo-9E81DF2E0E-seeklogo.com.png'),
            },
        ],
        breakpoints: {
            0: {
                itemsToShow: 2,
                snapAlign: 'center',
			},
            576: {
                itemsToShow: 3,
                snapAlign: 'center',
            },
            768: {
                itemsToShow: 3,
                snapAlign: 'center',
            },
            1024: {
                itemsToShow: 4,
                snapAlign: 'center',
            },
            1200: {
                itemsToShow: 6,
                snapAlign: 'center',
            },
        },
    }),
})
</script>