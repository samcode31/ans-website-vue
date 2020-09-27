<template>
    
        <v-app-bar            
            color="white"      
            flat
            fixed            
        >      
             <v-row justify="center">
                <a
                    v-for="(link, i) in links"
                    :key="i"
                    :href="link.href"
                    class="subheading mx-3"
                    target="_blank"
                >
                    {{ link.text }}
                </a>
            </v-row>
        
        </v-app-bar>
   
</template>

<script>
export default {
    name: 'MainNavigation',
    data: () => ({
        links:[
            {
                text: 'About Us',
                href: '#'
            },
            {
                text: 'News / Announcements',
                href: '#'
            },
            {
                text: 'Library',
                href: '#'
            },
            {
                text: 'Students',
                href: '#'
            },
            {
                text: 'Teachers',
                href: '#'
            },
            {
                text: 'Contact Us',
                href: '#'
            },
        ]
    })
}
</script>

<style scoped>
    a{
        text-decoration: none;
        color: rgb(28,85,102) !important;
        font-weight: 600;
        font-family: Montserrat;
        text-transform: uppercase;
    }
</style>