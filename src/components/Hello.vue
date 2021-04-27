<template>
    <div class="text-left">
        <header class="roboto uppercase font-bold text-4xl mb-2" :class="(mode === 'dark') ? 'grey-font-color' : 'greenish-font-color'">Christophe Adriaensens</header>
        <p class="roboto font-bold text-xl mb-2" :class="(mode === 'dark') ? 'light-greenish-font-color' : 'blackish-font-color'">Junior full-stack developer</p>
        <p class="text-gray-700 ml-2" :class="(mode === 'dark') ? 'light-greenish-font-color' : 'blackish-font-color'">Based in Ghent</p>
    </div>
</template>

<script>
export default {
    props: ['mode']
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

.roboto {
    font-family: $roboto-font;
}

.greenish-font-color{
    color: $greenish-font-color;
    transition: $font-color-transition;
}

.light-greenish-font-color {
    color: $light-greenish-font-color;
    transition: $font-color-transition;
}

.grey-font-color {
    color: $white-color;
    transition: $font-color-transition;
}

.blackish-font-color {
    color: $dark-font-color;
    transition: $font-color-transition;
}
</style>
