<template>
    <v-container fluid class="pa-0">
        <v-row align-content="center" justify="center">SCHOOL GALLERY</v-row>
        <v-row align-content="center" justify="center">
            <v-btn
                text
                color="deep-purple accent-4"
            >
                Students
            </v-btn>
            <v-btn
                text
                color="deep-purple accent-4"
            >
                Achievements
            </v-btn>
            <v-btn
                text
                color="deep-purple accent-4"
            >
                Environment
            </v-btn>
        </v-row>
        <v-row no-gutters class="pa-0" fluid>
            <v-col
                v-for="(image,i) in images"
                :key="i"                
            >
                <v-hover v-slot:default="{ hover }">
                    <v-card
                        flat
                        tile
                        class="d-flex"
                    >
                        <v-img
                            :src="image.src"
                            aspect-ratio="1"
                        >
                            <v-expand-transition>
                                <div
                                    v-if="hover"
                                    class="d-flex transition-fast-in-fast-out cyan darken-2 v-card--reveal display-3 white--text"
                                    style="height:100%;"
                                >
                                    {{ image.caption }}
                                </div>
                            </v-expand-transition>
                        </v-img>

                    </v-card>
                </v-hover>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'GallerySection',
    data(){
        return{
            images: [
                {
                    src: 'img/gallery/student/old-mas.jpg',
                    caption: 'Old Mas Competition 2017'
                },
                {
                    src: 'img/gallery/student/sports-day.jpg',
                    caption: 'Sports Day',
                },
                {
                    src: 'img/gallery/student/female-football-team-2017-2018.jpg',
                    caption: '2017-2018 Female Football Team'
                },
            ]
        }
    }
}
</script>

<style scoped>
    .v-card--reveal{
        align-items: center;
        bottom: 0;
        justify-content: center;
        opacity: .9;
        position: absolute;
        width: 100%;
    }
</style>