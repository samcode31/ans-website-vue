<template>
    <div class="carousel-container">
        <v-row
            justify="center"
            align-content="center"
            class="logo--row"
        >
            <v-btn
                fab
                dark
                width="100"
                height="100"
                color="white"
                elevation="0"                
            >
                <v-img
                    src="img/icon/logo.png"
                    max-width="80"
                ></v-img>
            </v-btn>
        </v-row>    
        <v-carousel
            continuous
            cycle
        >
            <v-carousel-item
                v-for="(slide,i) in slides"
                :key="i"
                :src="slide.src"
            >
                
            </v-carousel-item>
        </v-carousel>
    </div>
</template>

<script>
export default {
    name: 'CarouselSection',
    data () {
        return {
            slides: [
                {src: 'img/wallpaper/outside-wall.jpg'},
                {src: 'img/wallpaper/5k-students.jpg'},
                {src: 'img/wallpaper/ans-poui.jpg'},
                {src: 'img/wallpaper/block-e-night.JPG'},
            ]
        }
    }
}
</script>

<style scoped>
    .carousel-container{
        position: relative;
        margin-top: 64px;
    }
    .logo--row{
        position: fixed;
        z-index: 10;
        width: 100vw;
        top: 0;
    }
    
</style>