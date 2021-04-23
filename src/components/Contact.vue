<template>
    <div class="text-left">
        <div class="mt-12 text-left">
            <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="font-bold text-left text-2xl mb-4">Contact me</header>
            <div class="text-gray-700 p-2">
                <div class="">
                    <a :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="inline-block mb-4" href="mailto:christophe.adriaensens@gmail.com"><img class="inline-block h-6 mr-4 " src="../assets/email.png" alt="email"><span class="sm:text-xl">christophe.adriaensens@gmail.com</span></a>
                    <br>
                    <a :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="inline-block" href="tel:00324732668232"><img class="inline-block h-6 mr-4" src="../assets/phone.png" alt="email"><span class="sm:text-xl">0032 472 66 82 32</span></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['mode']
}
</script>

<style scoped>
.light-font-color {
    color: rgba(255, 255, 255, 0.899);
    transition: color 0.7s ease-in-out;
}

.blackish-font-color {
    color: rgba(4, 4, 4, 0.838);
    transition: color 0.7s ease-in-out;
}
</style>
