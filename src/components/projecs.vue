<template>
    <div id="projects" class="h-full w-full bg-blue-900 py-11">
        <div class="flex justify-center py-10">
            <h3 class="plus relative inline-block text-white text-4xl font-medium hover:delay-200 transition-colors duration-200">
                Mes projets
            </h3>
        </div>

        <div class="px-10">
            <Swiper :space-between="30" :loop="true" :pagination="{ clickable: true }" @slideChange="updateCurrentIndex"
                :breakpoints="{
                    1024: {slidesPerView: 3},
                    768: {slidesPerView: 2},
                    640: {slidesPerView: 1}
                }">
                <SwiperSlide v-for="(project, index) in projects" :key="index">
                    <div class="relative w-full h-50" @mouseover="hover = index" @mouseleave="hover = null">
                        <img :src="project.image" class="w-full h-full object-cover rounded-lg shadow-lg">

                        <div v-if="hover === index" class="absolute top-0 left-0 h-full w-full flex flex-col justify-center items-center bg-black bg-opacity-30 rounded-lg">
                            <h2 class="text-lg text-white my-2 text-center">
                                {{ project.title }}
                            </h2>

                            <div class="flex text-white gap-1 my-2">
                                <p v-for="(tag, idx) in project.tags" :key="idx" class="text-xs border-2 rounded-lg px-2 xl:py-1" :class="tag.color">
                                    {{ tag.name }}
                                </p>
                            </div>

                            <button class="my-4 hover:bg-blue-800 hover:rounded-lg">
                                <a :href="project.link" target="_blank" class="text-sm px-2 py-1 text-white border-2 border-white hover:border-none rounded-lg">
                                    Visiter
                                </a>
                            </button>
                        </div>
                    </div>

                    <p class="text-white text-center my-2 font-medium">
                        {{ project.grandTitle }}
                    </p>
                </SwiperSlide>
            </Swiper>
        </div>

        <div class="flex justify-center my-4">
            <div v-for="(project, index) in projects" :key="index" 
                :class="{'bg-white rounded-full mx-0.5': true, 
                    'opacity-100 w-4 h-2': currentIndex === index, 
                    'opacity-50 w-2 h-2': currentIndex !== index
                }">
            </div>
        </div>

        <div class="flex justify-center items-center my-9">
            <button class="button mt-6 cursor-pointer overflow-hidden lg:text-3xl lg:px-6 lg:py-3 text-2xl px-4 py-2 hover:text-white text-blue-900 border-4 border-black
                            before:h-1 before:absolute before:bottom-0 before:w-full before:bg-blue-900 bg-white hover:bg-blue-900">
                <a href="#skills">Mes compétences</a>
            </button>
        </div>
    </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";
import { ref } from "vue";
import nahlaImage from '@/assets/images/nahladelices.png';
import quiz from '@/assets/images/quiz.png';

const hover = ref(null);
const currentIndex = ref(0);

const updateCurrentIndex = (swiper) => {
    currentIndex.value = swiper.realIndex; 
};

const projects = ref([
    {
        image: nahlaImage,
        title: "Nahla Délices | CMS E-commerce",
        tags: [
            { name: "Wordpress", color: "border-green-600" },
            { name: "Woocommerce", color: "border-blue-400" },
            { name: "SEO & SEA", color: "border-blue-600" },
        ],
        link: "https://nahladelices.com/",
        grandTitle: "CMS e-commerce"
    },
    {
        image: quiz,
        title: "QuizApp",
        tags: [
            { name: "Vue.js", color: "border-green-600" },
            { name: "Node.js", color: "border-red-700" },
            { name: "MySQL", color: "border-yellow-500" },
        ],
        link: "https://navalnorth.com/quiz/",
        grandTitle: "Appication Quiz CRUD"
    },
    {
        image: nahlaImage,
        title: "Project 3",
        tags: [
            { name: "React", color: "border-red-600" },
            { name: "TypeScript", color: "border-blue-400" },
        ],
        link: "https://example.com",
        grandTitle: "Appication Quiz CRUD"

    },
    {
        image: nahlaImage,
        title: "Project 4",
        tags: [
            { name: "Laravel", color: "border-purple-600" },
            { name: "PHP", color: "border-yellow-400" },
        ],
        link: "https://example.com",
        grandTitle: "Appication Quiz CRUD"

    },
]);
</script>

<style scoped>
.plus::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background-color: #ffffff;
    transition: width 0.3s ease-in-out;
}
.plus:hover::before {
    width: 100%;
}

div[v-for] {
    transition: opacity 0.3s ease-in-out;
}

.button {
    position: relative;
    transition: background-color 0.2s, color 0.2s;
}
.button:hover {
    transition-delay: 0.2s;
}
.button::before {
    content: '';
    position: absolute;
    left: -100%;
    transition: transform 0.3s;
}
.button:hover::before {
    transform: translateX(100%);
}
</style>
