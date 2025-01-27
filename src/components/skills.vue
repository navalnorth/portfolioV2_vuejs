<template>
    <div id="skills" class="h-full w-full py-12">
        <div class="flex flex-col justify-center items-center px-8 lg:px-80">
            <div class="my-6">
                <h3 class="plus relative inline-block text-4xl font-medium">
                    Mes skills
                </h3>
            </div>

            <div class="w-full border-blue-800 border-4 p-4 my-6 flex flex-col justify-evenly">
                <p class="lg:text-3xl text-center font-bold">Ma stack</p>

                <div class="flex flex-wrap justify-center">
                    <img src="../assets/images/logos/flutter.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/fb.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/vue.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">

                    <img src="../assets/images/logos/node.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/mysql.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/tailwind.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/mongo.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/ts.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                </div>
            </div>

            <div class="w-full border-blue-800 border-4 p-4 my-6 flex flex-col justify-evenly">
                <p class="lg:text-3xl text-center font-bold">Mes outils</p>

                <div class="flex flex-wrap justify-center">
                    <img src="../assets/images/logos/wp.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">

                    <img src="../assets/images/logos/git.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/slack.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/trello.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">

                    <img src="../assets/images/logos/jira.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/figma.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/seo.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                    
                    <img src="../assets/images/logos/jest.png" class="lg:w-40 w-24 lg:my-4 my-2 mx-2 hover:shadow-md hover:shadow-blue-800 rounded-4xl">
                </div>
            </div>
        </div>

        <div class="flex justify-center items-center my-9">
            <button class="button mt-6 cursor-pointer overflow-hidden lg:text-3xl lg:px-6 lg:py-3 text-2xl px-4 py-2 hover:text-white text-blue-900 border-4 border-black
                            before:h-1 before:absolute before:bottom-0 before:w-full before:bg-blue-900 bg-white hover:bg-blue-900">
                <a href="#contact">Contactez-moi</a>
            </button>
        </div>
    </div>
</template>

<script setup>

</script>



<style scoped>
.plus {
    transition: color 0.2s;
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