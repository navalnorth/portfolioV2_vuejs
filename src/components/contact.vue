<template>
    <div id="contact" class="flex flex-col bg-blue-900 w-full h-full">
        <div class="py-20">
            <div class="flex flex-col items-center justify-center">
                <h3 class="plus relative inline-block text-white text-4xl font-medium hover:delay-200 transition-colors duration-200">
                    Contact
                </h3>

                <h4 class="text-center text-white my-4" >
                    J'espère que ça vous a plu :)<br>
                    Si vous avez des questios n'hesitez pas !
                </h4>
            </div>

            <div class="flex justify-center items-center gap-4">
                <div>
                    <a href="mailto:moha_naval@live.com">
                        <img src="../assets/images/social/mail.png" class="w-16 h-16 my-16 cursor-pointer">
                    </a>
                </div>

                <div>
                    <a href="tel:+33753474050">
                        <img src="../assets/images/social/tel.png" class="w-16 h-16 my-16 cursor-pointer">
                    </a>
                </div>

                <div>
                    <a href="https://www.linkedin.com/in/mohamed-navalnorth-10061626b/">
                        <img src="../assets/images/social/lk.png" class="w-16 h-16 my-16 cursor-pointer">
                    </a>
                </div>

                <div>
                    <a href="https://github.com/navalnorth">
                        <img src="../assets/images/social/github.png" class="w-16 h-16 my-16 cursor-pointer">
                    </a>
                </div>
            </div>
        </div>

        <div class="bg-white w-full text-center py-18">
            <p>Copyright © 2025 - By Navalnorth</p>
        </div>
    </div>
</template>



<script>

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
</style>