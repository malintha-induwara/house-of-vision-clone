<script>
import Swiper from 'swiper';
import { Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';
import VisionTest from '@/assets/images/vision.png'
import GlucomaTest from '@/assets/images/glaucoma.png'
import ColorTest from '@/assets/images/color.png'
import VisualTest from '@/assets/images/visual.png'


export default {
    data() {
        return {
            VisionList: [
                {
                    id: 1,
                    title: "Vision Test",
                    image: VisionTest,
                    paragaph: " Through eye examiations to ascertain optimal clarity and sharpness of vision.",
                    alt: "Vision Test"
                },
                {
                    id: 2,
                    title: "Glaucoma Test",
                    image: GlucomaTest,
                    paragaph: "Utilizing advanced RM-9800 autorefractors for refractive assessments and glaucoma monitoring",
                    alt: "Glaucoma Test"
                },
                {
                    id: 3,
                    title: "Visual Test",
                    image: VisualTest,
                    paragaph: "Employing slit lamp examinations to meticulously assess and improve ocular health.",
                    alt: "Visual Testing"
                },
                {
                    id: 4,
                    title: "Color Test",
                    image: ColorTest,
                    paragaph: "Detailed evaluations using specialized tests to accurately gauge and refine color perception.",
                    alt: "Color Vision Testing"
                }
            ]
        }
    },

    mounted() {
        this.initSwiper();
    },

    methods: {
        initSwiper() {
            new Swiper('.swiper', {
                modules: [Pagination],
                slidesPerView: 1,
                spaceBetween: 15,
                pagination: {
                    el: '.swiper-pagination',
                    clickable: true,
                },
                breakpoints: {
                    340: {
                        slidesPerView: 2,
                    },

                    640: {
                        slidesPerView: 3,
                    },
                },
            });
        }
    }

}
</script>

<template>
    <div class="flex flex-col xl:p-6">
        <div class="flex justify-center">
            <h3
                class="px-4  mb-4 text-sm font-semibold rounded-xl text-blue-700 bg-blue-400/40 sm:text-base md:text-lg lg:text-xl">
                Our Services
            </h3>
        </div>

        <div class="hidden xl:flex justify-center p-5  ">
            <div
                class="grid gap-5 grid-cols-1 sm:grid-cols-2  lg:grid-cols-3  2xl:grid-cols-4 min-[1200px]:grid-cols-4">
                <div v-for="vision in VisionList" v-bind:key="vision.id" class="w-[285px]">
                    <img :src="vision.image" :alt="vision.alt" class="">
                    <h4 class="text-blue-700 text-3xl my-2  font-bold">
                        {{ vision.title }}
                    </h4>
                    <p class=" text-gray-700 ">
                        {{ vision.paragaph }}
                    </p>
                </div>
            </div>
        </div>
        <div class="xl:hidden">
            <div class="swiper max-w-[90%] lg:max-w-[80%]">
                <div class="swiper-wrapper">
                    <div v-for="vision in VisionList" :key="vision.title" class="swiper-slide">
                        <div class="flex flex-col px-2" >
                            <img :src="vision.image" :alt="vision.alt">
                            <h4 class="text-blue-700 text-2xl my-2 font-bold">
                                {{ vision.title }}
                            </h4>
                            <p class=" text-gray-700 mb-10">
                                {{ vision.paragaph }}
                            </p>
                        </div>
                    </div>
                </div>
                <div class="swiper-pagination"></div>
            </div>
        </div>
    </div>
</template>



<style></style>