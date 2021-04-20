<template>
    <div class="mt-24 grid grid-cols-2 justify-items-stretch">
        <div class="text-container">
            <div class="mb-12 mr-4">
                <header class="font-bold text-left text-2xl mb-2">About me</header>
                <p class="text-left text-gray-700 leading-relaxed p-2">
                    My name is Christophe Adriaensens. I started coding not so long ago. Now I'm a junior full stack developer with strong interest in everything web dev. Coffee, music and 26-inch bike enthousiast. Happy young dad of an energetic 5-year old girl.
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
</template>

<script>
export default {
  data () {
      return {
          recentImage: require("../assets/christopheNew.jpeg"),
          oldImage: require("../assets/christopheJane.jpeg"),
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

    /* Hover effect picture */
    .pic-container {
        position: relative;
        display: inline-block;
        background-color: rgba(255, 0, 0, 0.701);
    }

    .pic-container:before,
    .pic-container:after {
        content: '';
        display: block;
        background-color: rgba(255, 0, 0, 0.701);
        width: 8px;
        height: 8px;
        position: absolute;
        transition: all .15s ease;
    }

    .pic-container:before {
        top: 0;
        left: 0;
        transform-origin: top left;
        transform: rotate(-45deg) scale(0);
    }

    .pic-container:after {
        right: 0;
        bottom: 0;
        transform-origin: bottom right;
        transform: rotate(45deg) scale(0);
    }

    .pic {
        display: block;
        transform: translate(0, 0);
        transition: all .15s ease;
        position: relative;
        z-index: 10;
    }

    .pic-container:hover .pic {
        transform: translate(6px, -6px);
    }

    .pic-container:hover:before {
        transform: rotate(-45deg) scale(1);
    }

    .pic-container:hover:after {
        transform: rotate(45deg) scale(1);
    }
</style>
