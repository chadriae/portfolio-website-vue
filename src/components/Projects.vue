<template>
    <div class="mt-12 text-left">
        <header class="font-bold text-left text-2xl mb-2">Projects</header>
        <div class="flex md:grid grid-cols-2 gap-6">
            <div class="p-2 leading-loose relative shadow">
                <a class="" href="https://github.com/chadriae/king-size"><img @mouseover="hover = true" @mouseleave="hover = false" :src="chained"></a>
                <header class="uppercase font-semibold">Chained</header>
                <p class="text-gray-700 h-32">A website made for people who want to look for a local bicycle repairer. Repairers also get to make an account and share their specialties and locality.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://tailwindcss.com/"><img class="h-6 backdrop-filter grayscale" src="../assets/tailwind.png"></a>
                    <a href="https://vuejs.org/"><img class="h-6" src="../assets/vue.png"></a>
                    <a href="https://laravel.com/"><img class="h-6" src="../assets/laravel.png"></a>
                </div>
             </div>
            <div class="p-2 leading-loose relative shadow">
                <a class="" href="https://github.com/chadriae/php-mvc-Ismi"><img src="../assets/beconnect.png" class=""></a>
                <header class="uppercase font-semibold">BeConnect</header>
                <p class="text-gray-700 h-32">A place where BeCode-alumni could meet, register, update their profiles and talk about their experiences.</p>
                <div class="absolute bottom-2 inset-x-4 flex flex-row-reverse gap-2">
                    <a href="https://www.mysql.com/"><img class="h-6" src="../assets/mysql.png"></a>
                    <a href="https://www.php.net/"><img class="h-6" src="../assets/php.png"></a>
                </div>
            </div>
            <div class="p-2 leading-loose relative shadow">
                <a class="" href="https://github.com/chadriae/intro-react"><img src="../assets/todo.png" class=""></a>
                <header class="uppercase font-semibold">ToDo</header>
                <p class="text-gray-700 h-32">Simple and fun todo-app made with React. Added time, date and inspirational quotes.</p>
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
      data () {
      return {
          chainedStatic: require("../assets/chained.png"),
          chainedGif: require("../assets/chained.gif"),
          hover: false
      }
  },
  computed: {
      chained: function () {
           if (this.hover) {
                return this.chainedGif;
            } else {
                return this.chainedStatic;
            }
      }
  }
}
</script>

<style scoped>

</style>
