<template>
    <div class="mt-24 grid grid-cols-2">
        <div class="">
            <div class="mb-12 mr-4">
                <header class="font-bold text-left text-2xl mb-2">About me</header>
                <p class="text-left text-gray-700 leading-relaxed">
                    My name is Christophe Adriaensens. I started coding not so long ago. Now I'm a full stack developer with strong interest in everything web dev. Coffee, music and 26-inch bike enthousiast.
                </p>
            </div>
            
            <header class="font-bold text-left text-xl mb-2">Skills</header>
            <ul class="text-left text-gray-700 leading-relaxed">
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
                <li>php</li>
                <li>React, Vue</li>
                <li>Laravel</li>
            </ul>
        </div>
        <div class="">
            <img @mouseover="hover = true" @mouseleave="hover = false" :src="image">
        </div>

    </div>
</template>

<script>
export default {
  name: 'About',
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

</style>
