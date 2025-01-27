<template>
    <div class="fixed top-0 left-0 w-full bg-white z-50 shadow-lg">
        <div :class="['lg:hidden flex justify-between items-center px-6 border-2'], !menuOpen ? 'hidden' : 'block'">
            <div>
                <p class="font-extrabold text-blue-900 text-2xl py-4">
                <a href="/">NAVALNORTH</a>
                </p>
            </div>

            <button @click="toggleMenu" class="text-3xl cursor-pointer hover:text-blue-900">
                <BxMenu/>
            </button>
        </div>

        <div class="transition-all duration-200 ease-in-out"
            :class="['lg:flex lg:justify-between lg:items-center lg:px-6 lg:border-2 bg-white z-10 fixed top-0 left-0 w-full lg:static',menuOpen ? 'block' : 'hidden']">
            <div class="flex justify-between items-center px-6 border-2 lg:border-none">
                <div class="flex justify-center items-center">
                    <p class="font-extrabold text-blue-900 text-2xl py-4">
                        <a href="/">NAVALNORTH</a>
                    </p>
                </div>

                <button @click="toggleMenu" class="text-3xl cursor-pointer hover:text-blue-900 lg:hidden ">
                    <AnOutlinedClose/>
                </button>
            </div>
    
            <nav class="border-x-2 border-b-2 lg:border-none">
                <ul class="flex flex-col lg:flex-row gap-6 lg:gap-10">
                    <li @click.prevent="scrollTo('ban')" class="group cursor-pointer hover:text-blue-900">
                        <div class="flex flex-col justify-center items-center">
                            <ClHouse01 class="text-2xl"/>
                            <div class="relative">
                                <p>Home</p>
                            <span class="absolute bottom-0 left-0 h-0.5 w-full bg-blue-900 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"></span>
                            </div>
                        </div>
                    </li>

                    <li @click.prevent="scrollTo('about')" class="group cursor-pointer hover:text-blue-900">
                        <div class="flex flex-col justify-center items-center">
                            <CoDoubleQuoteSansRight class="text-2xl"/>
                            <div class="relative">
                                <p>About</p>
                                <span class="absolute bottom-0 left-0 h-0.5 w-full bg-blue-900 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"></span>
                            </div>
                        </div>
                    </li>

                    <li @click.prevent="scrollTo('projects')" class="group cursor-pointer hover:text-blue-900">
                        <div class="flex flex-col justify-center items-center">
                            <IoOutlineConstruct class="text-2xl"/>
                            <div class="relative">
                                <p>Projects</p>
                                <span class="absolute bottom-0 left-0 h-0.5 w-full bg-blue-900 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"></span>
                            </div>
                        </div>
                    </li>

                    <li @click.prevent="scrollTo('skills')" class="group cursor-pointer hover:text-blue-900">
                        <div class="flex flex-col justify-center items-center">
                            <CgBulb class="text-2xl"/>
                            <div class="relative">
                                <p>Skills</p>
                                <span class="absolute bottom-0 left-0 h-0.5 w-full bg-blue-900 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"></span>
                            </div>
                        </div>
                    </li>

                    <li @click.prevent="scrollTo('contact')" class="group cursor-pointer hover:text-blue-900">
                        <div class="flex flex-col justify-center items-center">
                            <AnOutlinedMail class="text-2xl"/>
                            <div class="relative">
                                <p>Contact</p>
                                <span class="absolute bottom-0 left-0 h-0.5 w-full bg-blue-900 scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-200"></span>
                            </div>
                        </div>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>
  


<script setup>
    import { AnOutlinedMail, ClHouse01, CoDoubleQuoteSansRight, IoOutlineConstruct, CgBulb, BxMenu, AnOutlinedClose } from '@kalimahapps/vue-icons';
    import { ref } from 'vue';
    
    const menuOpen = ref(false);

    const toggleMenu = () => {
        menuOpen.value = !menuOpen.value
    }

    const scrollTo = (id) => {
        const target = document.getElementById(id);

        if (target) {
            target.scrollIntoView({ behavior: 'smooth' });
        };

        toggleMenu();
    };
 </script>