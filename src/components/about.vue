<template>
    <div id="about" class=" py-20">
        <div class="flex flex-col w-full lg:flex-row justify-center items-center lg:items-start lg:px-36 gap-20">
            <div class="image_container inline-block w-75 h-100 perspective-distant">
                <div class="card relative w-full h-full">
                    <div class="absolute flex flex-col text-center justify-center items-center border-4 border-blue-900 overflow-hidden backface-hidden w-full h-full">
                        <img src="../assets/images/moi.jpg" class="w-full h-full object-cover">
                    </div>

                    <div class="back absolute p-5 flex justify-normal items-center overflow-hidden backface-hidden w-full h-full text-white bg-blue-900">
                        <div>
                            <div class="space-y-1 mb-4 border-b border-white pb-4">
                                <p class="flex items-center gap-3"><CaEarthAmericasFilled/>Voyages</p>
                                <p>Thaïlande, Espagne, Maroc, Angleterre, Pays-Bas, Portugal</p>
                            </div>

                            <div class="space-y-1 mb-4 border-b border-white pb-4">
                                <p class="flex items-center gap-3"><FlFilledSportSoccer/>Sports</p>
                                <p>Tennis de Table, Football, Musculation</p>
                            </div>

                            <div class="space-y-1">
                                <p class="flex items-center gap-3"><McMovieLine/>Autres</p>
                                <p>Veile informatique & High-tech, Films, séries et surtout Breaking Bad</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="w-4/5 lg:w-3/5 space-y-6 flex flex-col justify-center text-center lg:text-left self-center">
                <div>
                    <h3 class="plus relative inline-block text-4xl font-medium">
                        A propos de moi
                    </h3>
                </div>

                <p>
                    Développeur web & mobile full-stack et auparavant chimiste,
                    je suis d'abord attiré par les experiences chimiques pour me tourner finalement vers les expériences informatiques.
                    Fluutter, Firebase, VueJs, Nodejs... nombreux sont les langages que je maîtrise mais le plus important est
                    de ne pas stagner, d'apprendre continuellement et d'évoluer.<br><br>
                    Ce portfolio reflète mon expertise et mon engagement à concevoir des solutions adaptées aux utilisateurs.
                    À la recherche d'un développeur polyvalent et créatif ? Contactez-moi pour en discuter !
                </p>
            </div>
        </div>

        <div class="flex justify-center items-center my-9">
            <button class="button mt-6 cursor-pointer overflow-hidden lg:text-3xl lg:px-6 lg:py-3 text-2xl px-4 py-2 hover:text-white text-blue-900 border-4 border-black
                            before:h-1 before:absolute before:bottom-0 before:w-full before:bg-blue-900 bg-white hover:bg-blue-900">
                <a href="#projects">Explorez</a>
            </button>
        </div>
    </div>
</template>

<script setup>
import { CaEarthAmericasFilled, FlFilledSportSoccer, McMovieLine } from '@kalimahapps/vue-icons';
</script>

<style scoped>
.image_container:hover .card {
    transform: rotateY(-180deg);
}
.card {
    transform-style: preserve-3d;
    transition: transform 0.6s ease-in-out;
}
.back {
    transform: rotateY(-180deg);
}


.plus {
    transition: color 0.2s;
    display: inline-block;
    position: relative;
}
.plus:hover {
    transition-delay: 0.2s;
}
.plus::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 3px;
    background-color: #1E40AF;
    transition: width 0.3s ease-in-out;
}
.plus:hover::before {
    width: 100%;
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