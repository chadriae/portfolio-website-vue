<template>
    <div class="mt-16 text-left ">
        <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="font-bold text-left text-2xl mb-2 ">Projects</header>
        <div class="md:grid grid-cols-2 gap-6">
            <div class="mb-4 card p-8 leading-loose relative rounded-lg shadow w-auto" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
                <a class="flex justify-center" href="https://github.com/chadriae/king-size"><img class="" @mouseover="chainedHover = true" @mouseleave="chainedHover = false" :src="chained"></a>
                <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="mt-6 uppercase font-semibold"><a href="https://github.com/chadriae/king-size">Chained</a></header>
                <p :class="(mode === 'dark') ? 'project-bg light-font-color ' : 'blackish-font-color'" class="h-36 mb-4 sm:mb-0" >A website made for people who want to look for a local bicycle repairer. Repairers also get to make an account and share their specialties and locality.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://tailwindcss.com/"><img class="h-6 backdrop-filter grayscale" src="../assets/tailwind.png"></a>
                    <a href="https://vuejs.org/"><img class="h-6" src="../assets/vue.png"></a>
                    <a href="https://laravel.com/"><img class="h-6" src="../assets/laravel.png"></a>
                </div>
             </div>
            <div class="mb-4 card p-8 leading-loose relative rounded-lg shadow" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
                <a class="flex justify-center" href="https://github.com/chadriae/php-mvc-Ismi"><img class="" @mouseover="beconnectHover = true" @mouseleave="beconnectHover = false" :src="beconnect"></a>
                <header :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="mt-6 uppercase font-semibold"><a href="https://github.com/chadriae/php-mvc-Ismi">BeConnect</a></header>
                <p :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'" class="h-32">A place where BeCode-alumni could meet, register, update their profiles and talk about their experiences.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://www.mysql.com/"><img class="h-6" src="../assets/mysql.png"></a>
                    <a href="https://www.php.net/"><img class="h-6" src="../assets/php.png"></a>
                </div>
            </div>
            <div class="mb-4 card p-8 leading-loose relative rounded-lg shadow" :class="(mode === 'dark') ? 'project-bg-dark' : 'background-white'">
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

<style scoped>
.project-bg-dark {
    background-color: #21272e;
    border: 1px solid #6a6969;
    transition: background 0.7s ease-in-out;
}

.light-font-color {
    color: rgba(255, 255, 255, 0.899);
    transition: color 0.7s ease-in-out;
}

.blackish-font-color {
    color: rgba(4, 4, 4, 0.838);
    transition: color 0.7s ease-in-out;
}

.background-white {
    background-color: white;
    border: 1px solid #f0f0f0;
    transition: 0.7s ease-in-out;
}

</style>
