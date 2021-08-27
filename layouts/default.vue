<template>
  <v-app dark>
    <Navbar/>
    <SocialLine/>
    <v-main>
      <Nuxt />
    </v-main>
    <FooterBottom/>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import SocialLine from '@/components/SocialLine.vue'
import FooterBottom from '@/components/FooterBottom.vue'

export default {
  components: {
    Navbar,
    SocialLine,
    FooterBottom
  }
}
</script>

<style lang="scss">

$font-stack-primary: 'Nexa', 'Roboto';

html {
  font-family: $font-stack-primary;
}
main {
  padding: 0px !important;
}
img {
  display: block;
  max-width: 100%;
}
a {
  text-decoration: none !important;
}
</style>