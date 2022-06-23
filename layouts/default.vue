<template>
    <v-main>
      <v-container class="ma-0 pa-0"> 
        <Nuxt />
      </v-container>
    </v-main>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
