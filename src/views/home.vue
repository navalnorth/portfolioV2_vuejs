<template>
    <div class="h-screen flex flex-col">
        <Navbar />
        <Ban />
    </div>
    
    <About />
    <Projecs />
</template>


<script setup>
import Navbar from '../components/navbar.vue';
import Ban from '../components/ban.vue';
import About from '@/components/about.vue';
import Projecs from '@/components/projecs.vue';
</script>