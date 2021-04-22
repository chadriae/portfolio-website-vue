<template>
    <div class="mt-16 sm:grid grid-cols-2 justify-items-stretch">
        <div class="text-container">
            <div class="mb-12 mr-4">
                <header class="font-bold text-left text-2xl mb-2">About me</header>
                <p class="text-left text-gray-700 leading-relaxed p-2 text-lg">
                    My name is Christophe Adriaensens. I started coding not so long ago. Now I'm a junior full stack developer with strong interest in everything web dev. Coffee, music and 26-inch bike enthousiast. Happy young dad of an energetic 5-year old girl.
                </p>
            </div>
            
            <header class="font-bold text-left text-xl mb-2">Skills</header>
            <ul class="text-left text-gray-700 leading-relaxed p-2 text-lg">
                <li>HTML5</li>
                <li>CSS3 - Tailwind, Bootstrap</li>
                <li>JavaScript - Vue, React</li>
                <li>php - Laravel</li>
                <br>
                <span><a id="button" class="text-white py-1 px-2 rounded-lg shadow-lg font-bold" :href="pdfLink" download="cvChristopheAdriaensens">Download</a> my <span class="font-bold">cv</span> as a .pdf-file.</span>
            </ul>

            <div class="mt-4 p-2 flex gap-4">
                <a href="https://github.com/chadriae"><img src="../assets/github.png" class="h-12 social-media"></a>
                <a href="https://www.linkedin.com/in/christophe-adriaensens/"><img src="../assets/linkedin.png" class="h-12 social-media"></a>
                <a href="https://dev.to/chadriae"><img src="../assets/devto.png" class="h-12 social-media rounded-full"></a>
                <a href="https://twitter.com/chadriae"><img src="../assets/twitter.png" class="h-12 social-media"></a>
            </div>
        </div>
        <div class="pic-container h-96 w-72 mt-8 mr-4 justify-self-end">
            <div class="justify-self-end"><img class="pic h-96 w-auto" @mouseover="hover = true" @mouseleave="hover = false" :src="image"></div>
        </div>
    </div>
    <div class="text-left">
           
    </div>
</template>

<script>
export default {
  data () {
      return {
          recentImage: require("../assets/christopheNew.jpeg"),
          oldImage: require("../assets/christopheJane.jpeg"),
          hover: false,
          pdfLink: require("../assets/cv_ChristopheAdriaensens.pdf")
      }
  },
    computed: {
        image() {
            if (this.hover) {
                return this.oldImage;
            } else {
                return this.recentImage;
            }
        } 
    },
}
</script>

<style scoped>
    .social-media:hover {
        opacity: 0.5;
    }

    .pic {
        margin:10px;
        box-shadow:0 0 rgba(255, 0, 0, 0.625);
        transition:0.5s;
    }

    .pic:hover {
        box-shadow: -5px 5px rgba(255, 0, 0, 0.625);
        transform: translate(5px,-5px);
    }

    #button {
        background-color: #a3ddcb;
    }
</style>
