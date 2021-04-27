<template>
    <div class="text-left">
        <div class="mt-12 text-left">
            <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="title font-bold text-left text-2xl mb-4">Contact me</header>
            <div class="text-gray-700 p-2">
                <div class="">
                    <a :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="inline-block mb-4" href="mailto:christophe.adriaensens@gmail.com">
                        <img class="inline-block h-6 mr-4 align-top" src="../assets/email.png" alt="email" :class="(mode === 'dark') ? 'icons-inverted' : ''"><span class="sm:text-xl">christophe.adriaensens@gmail.com</span>
                    </a>
                    <br>
                    <a :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="inline-block" href="tel:00324732668232">
                        <img class="inline-block h-6 mr-4" src="../assets/phone.png" alt="email" :class="(mode === 'dark') ? 'icons-inverted' : ''"><span class="sm:text-xl">0032 472 66 82 32</span>
                    </a>
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

<style scoped lang="scss">
@import "../styles/_variables.scss";

.title {
    font-family: $roboto-font;
}

.light-font-color {
    color: $white-color;
    transition: $font-color-transition;
}

.blackish-font-color {
    color: $dark-font-color;
    transition: $font-color-transition;
}

.icons-inverted {
    filter: $full-filter-invert;
    transition: $transition;
}
</style>
