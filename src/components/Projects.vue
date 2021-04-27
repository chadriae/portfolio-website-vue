<template>
    <div class="mt-16 text-left ">
        <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="title font-bold text-left text-2xl mb-4">Projects</header>
        <div class="md:mx-auto md:grid grid-cols-2 gap-6 p-2">
            <div class="project mb-4 card p-8 leading-loose relative w-auto" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
                <a class="flex justify-center" href="https://github.com/chadriae/king-size"><img class="" @mouseover="chainedHover = true" @mouseleave="chainedHover = false" :src="chained"></a>
                <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="mt-6 uppercase font-semibold"><a href="https://github.com/chadriae/king-size">Chained</a></header>
                <p :class="(mode === 'dark') ? 'project-bg light-font-color ' : 'blackish-font-color'" class="h-36 mb-4 sm:mb-0" >A website made for people who want to look for a local bicycle repairer. Repairers also get to make an account and share their specialties and locality.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://tailwindcss.com/"><img class="h-6 backdrop-filter grayscale" src="../assets/tailwind.png"></a>
                    <a href="https://vuejs.org/"><img class="h-6" src="../assets/vue.png"></a>
                    <a href="https://laravel.com/"><img class="h-6" src="../assets/laravel.png"></a>
                </div>
             </div>
            <div class="project mb-4 card p-8 leading-loose relative" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
                <a class="flex justify-center" href="https://github.com/chadriae/php-mvc-Ismi"><img class="" @mouseover="beconnectHover = true" @mouseleave="beconnectHover = false" :src="beconnect"></a>
                <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="mt-6 uppercase font-semibold"><a href="https://github.com/chadriae/php-mvc-Ismi">BeConnect</a></header>
                <p :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="h-32">A place where BeCode-alumni could meet, register, update their profiles and talk about their experiences.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://www.mysql.com/"><img class="h-6" src="../assets/mysql.png"></a>
                    <a href="https://www.php.net/"><img class="h-6" src="../assets/php.png"></a>
                </div>
            </div>
            <div class="project mb-4 card p-8 leading-loose relative" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
                <a class="flex justify-center" href="https://github.com/chadriae/intro-react"><img class="" @mouseover="todoHover = true" @mouseleave="todoHover = false" :src="todo"></a>
                <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="mt-6 uppercase font-semibold"><a href="https://github.com/chadriae/intro-react">ToDo</a></header>
                <p :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="h-32">Simple and fun todo-app made with React. Added time, date and inspirational quotes.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://sass-lang.com/"><img class="h-6" src="../assets/scss.png"></a>
                    <a href="https://reactjs.org/"><img class="h-6" src="../assets/react.png"></a>
                </div>
            </div>
        </div> 
    </div>
</template>

<script>
export default {
    props: ['mode'],
    data () {
      return {
        chainedHover: false,
        beconnectHover: false,
        todoHover: false,
        chainedStatic: require("../assets/chained.png"),
        chainedGif: require("../assets/chained.gif"),
        beconnectStatic: require("../assets/beconnect.png"),
        beconnectGif: require("../assets/beconnect.gif"),
        todoStatic: require("../assets/todo.png"),
        todoGif: require("../assets/todo.gif"),
      }
  },
  computed: {
    chained() {
        if (this.chainedHover) {
            return this.chainedGif;
        } else {
            return this.chainedStatic;
        }
    },
    beconnect () {
        if (this.beconnectHover) {
            return this.beconnectGif;
        } else {
            return this.beconnectStatic;
        }
    },
    todo () {
        if (this.todoHover) {
            return this.todoGif;
        } else {
            return this.todoStatic;
        }
    }
  }
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

.title {
    font-family: $roboto-font;
}

.project-bg-dark {
    background-color: $dark-bg-color;
    border: 2px solid $dark-border-color;
    border-radius: 7px;
    transition: $transition;
}

.light-font-color {
    color: $white-color;
    transition: $font-color-transition;
}

.blackish-font-color {
    color: $dark-font-color;
    transition: $font-color-transition;
}

.background-white {
    background-color: $white-color;
    border: 2px solid black;
    border-radius: 7px;
    transition: $transition;
}

</style>
