<template>
    <v-container fluid class="grey lighten-5">
        <v-row>
            <v-col
                cols="12"
                sm="4"
                v-for="(card,i) in cards"
                :key="i" 
            >
                <v-card
                     width="350"
                     height="400"                                
                >
                   
                    <v-img
                        :src="card.src"
                        height="200"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"                        
                    >
                        <v-card-title v-text="card.text"></v-card-title>
                    </v-img>
                    <v-card-text>
                        {{ card.details }}
                    </v-card-text>
                     <v-list-item>
                        <v-list-item-content>                            
                            <v-list-item-subtitle>{{ card.date }}</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                    <v-card-actions>
                        <v-btn
                            text
                            color="deep-purple accent-4"
                        >
                            Read More
                        </v-btn>
                        <v-spacer></v-spacer>
                        <v-btn icon>
                            <v-icon>mdi-share-variant</v-icon>
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'NewsSection',
    data(){
        return {
            cards: [
                {
                    title: 'LATEST NEWS',
                    date: '28 September 2020',
                    text: 'CSEC & CAPE Registration',
                    details: "Registration for 2021 Exams begin",
                    src: 'img/news/cxc.png'
                },
                {
                    title: 'BOOK LIST COLLECTION',
                    date: '08 August 2020',
                    text: 'BOOK LIST COLLECTION',
                    details: 'Book lists can be collected at office between 8:00am - 12:00pm',
                    src: 'img/news/students.png'
                },
                 {
                    title: 'FORM 6 APPLICATIONS',
                    date: '15 September 2020',
                    text: 'Form 6 Applications',
                    details: 'Applications Open between 22-30th September 2020',
                    src: 'img/news/students.png'
                }
            ]
        }
    }
}
</script>