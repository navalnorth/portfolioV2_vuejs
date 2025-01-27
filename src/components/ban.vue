<template>
    <div class="relative" id="ban">
        <div class="relative">
            <img src="../assets/images/ban.jpg" class="w-full h-190 object-center object-cover">
            <div class="absolute inset-0 bg-blue-900 opacity-90"></div>
        </div>

        <div class="absolute inset-0 flex flex-col justify-center items-center text-white">
            <div class="space-y-1">
                <h1 class="typing text-lg lg:text-4xl font-bold text-center">Développeur web et mobile full-stack</h1>
                <h2 class="text-md lg:text-2xl text-center">Mohamed A.T. "Navalnorth"</h2>
            </div>

            <button class="plus mt-6 cursor-pointer overflow-hidden lg:text-3xl lg:px-6 lg:py-3 text-2xl px-4 py-2 hover:text-white text-blue-900 border-4 border-black
                            before:h-1 before:absolute before:bottom-0 before:w-full before:bg-blue-900 bg-white hover:bg-blue-900">
                <a href="#about">Découvrir</a>
            </button>
        </div>
    </div>
</template>

<style scoped>
.plus {
    position: relative;
    transition: background-color 0.2s, color 0.2s;
}
.plus:hover {
    transition-delay: 0.2s;
}
.plus::before {
    content: '';
    position: absolute;
    left: -100%;
    transition: transform 0.3s;
}
.plus:hover::before {
    transform: translateX(100%);
}

.typing {
    overflow: hidden;
    white-space: nowrap; 
    border-right: 2px solid white;
    animation: typing 4s steps(30, end) 1, blink 1.2s step-end infinite 2.5s;
    animation-fill-mode: forwards;
}
@keyframes typing {
    0% {
        width: 0;
    }
    50% {
        width: 100%; /* Texte entièrement tapé */
    }
    90% {
        width: 100%; /* Pause ici */
    }
    100% {
        width: 100%; /* Retour à 0 pour la boucle */
    }
}
@keyframes blink {
    0% {
        border-color: transparent;
    }
    50% {
        border-color: white;
    }
    100% {
        border-color: transparent;
    }
}
</style>
