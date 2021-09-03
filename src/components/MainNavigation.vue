<template>        
    <v-app-bar            
        color="white"      
        flat
        fixed            
    >      
        <v-row 
            class="d-none d-md-flex"
            justify="center"
        >
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

        <div 
            class="d-flex flex-column d-md-none ml-auto"
            style="position:relative"
            
        >
            <v-app-bar-nav-icon

            @click="click"
            ></v-app-bar-nav-icon>
            <span 
                style="font-size:0.5rem; text-align:center; position:absolute; bottom:0; width:100%"
            >MENU</span>
        </div>  
    
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
        ],        
    }),

    methods: {
        drawer () {
            console.log('drawer clicked');
            this.$emit('drawer-click');
        }, 
        
        click () {
            console.log('click')
        }
    }
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