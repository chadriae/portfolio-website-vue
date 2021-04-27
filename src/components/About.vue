<template>
    <div class="mt-16 sm:grid grid-cols-2 justify-items-stretch">
        <div class="text-container">
            <div class="mb-12 mr-4">
                <header class="title font-bold text-left text-2xl mb-2" :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'">About me</header>
                <p class="text-left leading-relaxed p-2 text-lg" :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'">
                    My name is Christophe Adriaensens. I started coding not so long ago. Now I'm a junior full stack developer with strong interest in everything web dev. Coffee, music and 26-inch bike enthousiast. Happy young dad of an energetic 5-year old girl.
                </p>
            </div>
            
            <header class="title font-bold text-left text-2xl mb-2" :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'">Skills</header>
            <ul class="text-left leading-relaxed p-2 text-lg" :class="(mode === 'dark') ? 'light-font-color' : 'blackish-font-color'">
                <li>HTML5</li>
                <li>CSS3 - Tailwind, Bootstrap</li>
                <li>JavaScript - Vue, React</li>
                <li>php - Laravel</li>
                <br>
                <div class="my-8">
                    <a id="download-button" class="mr-1" :href="pdfLink" download="cvChristopheAdriaensens" :class="(mode === 'dark') ? 'button-blue' : 'button-green'">Download</a> 
                    my <span class="font-bold">cv</span> as a .pdf-file.
                </div>
            </ul>

            <div class="mt-4 mb-12 p-2 flex gap-4">
                <a href="https://github.com/chadriae"><img src="../assets/github.png" class="h-12 rounded-full social-media" :class="(mode === 'dark') ? 'social-media-inverted' : ''"></a>
                <a href="https://www.linkedin.com/in/christophe-adriaensens/"><img src="../assets/linkedin.png" class="h-12 social-media rounded-full" :class="(mode === 'dark') ? 'social-media-inverted' : ''"></a>
                <a href="https://dev.to/chadriae"><img src="../assets/devto.png" class="h-12 social-media rounded-full" :class="(mode === 'dark') ? 'social-media-inverted' : ''"></a>
                <a href="https://twitter.com/chadriae"><img src="../assets/twitter.png" class="h-12 social-media rounded-full" :class="(mode === 'dark') ? 'social-media-inverted' : ''"></a>
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
    props: ['mode'],
    data () {
        return {
            recentImage: require("../assets/christopheNew3.jpeg"),
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

<style scoped lang="scss">
@import "../styles/_variables.scss";

#download-button {
    color: black;
    font-family: $roboto-font;
    border: 3px solid black;
    border-bottom: 6px solid black;
    padding: 5px 15px 5px 15px;
    border-radius: 7px;
    font-weight: bold;
    letter-spacing: 1px;
    box-shadow: 0 0 black;
    transition: 0.2s;
}

#download-button:hover {
    box-shadow: -5px 5px black;
    transform: translate(10px, 0px);
}

.button-blue {
    background-color: #37d0fe;
    transition: $transition;
}

.button-green {
    background-color: #37d0fe;
    transition: $transition;
}

.title {
    font-family: $roboto-font;
}

.social-media-inverted {
    filter: $full-filter-invert;
    transition: $transition;
}

.social-media:hover {
    opacity: 0.5;
    transition: 0.3s;
}

.pic {
    margin: 10px;
    box-shadow: 0 0 $pic-hover-color;
    transition: 0.5s;
    border: 2px solid black;
    border-radius: 7px;
}

.pic:hover {
    box-shadow: -5px 5px $pic-hover-color;
    transform: translate(5px,-5px);
}

.light-font-color {
    color: $white-color;
    transition: $font-color-transition;
}

.blackish-font-color {
    color: $dark-font-color;
    transition: $font-color-transition;
}

</style>
