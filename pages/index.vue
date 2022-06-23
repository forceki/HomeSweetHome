<template>
<v-app>
  <navbar />
  <Home />
</v-app>
</template>

<script>
import Home from '~/components/Home.vue'
export default {
  components: { Home },
  name: 'IndexPage',
}
</script>
