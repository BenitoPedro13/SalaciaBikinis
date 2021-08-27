<template>
    <v-app-bar
      flat
      hide-on-scroll
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      color="transparent"
      height="80"
      app
    >
      <nuxt-link to="/">
        <v-toolbar-title v-text="title" />
      </nuxt-link>
      <v-spacer />
      <v-btn-toggle v-model="toggle_exclusive" mandatory group class="nav">
        <nuxt-link to="/">
          <v-btn text class="nav-menu">home</v-btn>
        </nuxt-link>
        <nuxt-link to="/inspire">
          <v-btn text class="nav-menu">bikinis</v-btn>
        </nuxt-link>
        <nuxt-link to="/contato">
          <v-btn text class="nav-menu">contato</v-btn>
        </nuxt-link>
        <nuxt-link to="/blog">
          <v-btn text class="nav-menu">blog</v-btn>
        </nuxt-link>
      </v-btn-toggle>
    </v-app-bar>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            toggle_exclusive: undefined,
            collapseOnScroll: true,
            title: 'salacia'
        }
    }
}
</script>

<style lang="scss" scoped>
$background-color-footer: #72c6d5;

$font-color-primary: white !important;
$font-color-secondary: black !important;

$font-stack-primary: 'Nexa', 'Roboto';
$font-stack-secondary: 'Qaligo';

$font-size-header-logo: 28px;
$font-size-line: 24px;
$font-size-footer-big: 32px;
$font-size-footer-small: 16px;
$font-size-footer-cta-header: 20px;
$font-size-footer-cta-subheader: 28px;
$font-size-copyright: 18px;

header {
  width: calc(100vw - 120px);
}

.v-toolbar__title {
  font-family: $font-stack-primary;
  font-weight: bold;
  color: $font-color-primary;
  font-size: $font-size-header-logo;
}

.nav {
  width: 35%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}

.theme--light.v-btn--active:hover::before,
.theme--light.v-btn--active::before {
  opacity: 0 !important;
}

.nav-menu {
  font-family: $font-stack-primary;
  margin: 0 auto;
  text-transform: lowercase !important;
  font-weight: thin;
  display: flex;
  position: relative;
  flex-direction: column;
  color: $font-color-primary;

  ::after {
    content: '';
    display: none;
    position: absolute;
    width: 5px;
    height: 5px;
    background: currentColor;
    border-radius: 50%;
    top: 85%;
  }
}
.nuxt-link-exact-active {
  .nav-menu {
    font-weight: bold;

    ::after {
      display: block;
    }
  }
}

</style>