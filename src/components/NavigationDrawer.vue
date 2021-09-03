<template>
    <v-navigation-drawer
        v-if="drawer"
        v-model="drawer"
        absolute
        bottom
        temporary
    ></v-navigation-drawer>
</template>

<script>
export default {
    props: {
        drawer: Boolean,
    }
}
</script>