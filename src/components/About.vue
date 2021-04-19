<template>
    <div class="mt-24 grid grid-cols-2">
        <div class="">

            <div class="mb-12 mr-4">
                <header class="font-bold text-left text-2xl mb-2">About me</header>
                <p class="text-left text-gray-700 leading-relaxed p-2">
                    My name is Christophe Adriaensens. I started coding not so long ago. Now I'm a full stack developer with strong interest in everything web dev. Coffee, music and 26-inch bike enthousiast. Happy young dad of a energetic 5-year old girl.
                </p>
            </div>
            
            <header class="font-bold text-left text-xl mb-2">Skills</header>
            <ul class="text-left text-gray-700 leading-relaxed p-2">
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
                <li>php</li>
                <li>React, Vue</li>
                <li>Laravel</li>
            </ul>

            <div class="mt-4 p-2 flex gap-4">
                <a class="social-media" href="https://github.com/chadriae"><img src="../assets/github.png" class="h-12 social-media"></a>
                <a href="https://www.linkedin.com/in/christophe-adriaensens/"><img src="../assets/linkedin.png" class="h-12 social-media"></a>
                <a href="https://twitter.com/chadriae"><img src="../assets/twitter.png" class="h-12 social-media"></a>
            </div>
        </div>
        <div class="p-4">
            <img class="h-96" @mouseover="hover = true" @mouseleave="hover = false" :src="image">
        </div>
    </div>
</template>

<script>
export default {
  data () {
      return {
          recentImage: require("../assets/christopheNew.jpeg"),
          oldImage: require("../assets/christopheOld.jpeg"),
          hover: false
      }
  },
  computed: {
      image: function () {
           if (this.hover) {
                return this.oldImage;
            } else {
                return this.recentImage;
            }
      }
  }
}
</script>

<style scoped>
    .social-media:hover {
        opacity: 0.5;
    }
</style>
