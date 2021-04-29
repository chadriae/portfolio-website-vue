<template>
    <div class="text-left">
        <header id="name" class="roboto uppercase font-bold text-5xl mb-2" :class="(mode === 'dark') ? 'grey-font-color' : 'blue-font-color'">Christophe Adriaensens</header>
        <p class="roboto font-bold text-xl mb-2" :class="(mode === 'dark') ? 'dark-border-color' : 'blackish-font-color'">Junior full-stack developer</p>
        <p class="text-gray-700 ml-2" :class="(mode === 'dark') ? 'grey-font-color' : 'blackish-font-color'">Based in Ghent</p>
    </div>
</template>

<script>
export default {
    props: ['mode']
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

#name {
    text-shadow: -2px 0px 0px rgb(167, 167, 167), 2px 0px 0px $pic-hover-color;
}

.roboto {
    font-family: $roboto-font;
}

.blue-font-color{
    color: $blue-font-color;
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

.dark-border-color {
    color: $dark-border-color;
}
</style>
