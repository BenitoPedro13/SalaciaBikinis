<template>
  <v-app dark>
    <v-app-bar flat absolute color="transparent" height="80" app hide-on-scroll>
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
    <div class="social-line">
      <button class="shop">
        <svg width="51" height="36" viewBox="0 0 51 48" fill="none">
          <path
            d="M38.9848 41.1522L37.4151 14.8696C37.3497 13.5 36.1724 12.3913 34.799 12.3913H28.8473V9.58696C28.8473 4.30435 24.5307 0 19.233 0C13.9353 0 9.61874 4.30435 9.61874 9.58696V12.3913H3.66705C2.22818 12.3913 1.11633 13.5 1.05092 14.8696L0.00447167 41.2174C-0.0609315 42.9783 0.5931 44.6739 1.83576 45.9783C3.07842 47.2826 4.7789 48 6.54479 48H32.379C34.2103 48 35.9108 47.2826 37.1535 45.9783C38.3961 44.6739 39.1156 42.9783 38.9848 41.1522ZM12.3003 9.58696C12.3003 5.73913 15.4396 2.6087 19.2984 2.6087C23.1572 2.6087 26.2965 5.73913 26.2965 9.58696V12.3913H12.3003V9.58696ZM35.3222 44.2174C34.6027 45 33.5563 45.4565 32.4444 45.4565H6.61019C5.56374 45.4565 4.51729 45 3.79785 44.2826C3.07842 43.5 2.686 42.5217 2.686 41.413L3.73245 15.0652H9.68414V26.3478H12.3003V15.0652H26.2311V26.3478H28.8473V15.0652H34.799L36.3686 41.3478C36.434 42.3913 36.107 43.4348 35.3222 44.2174Z"
            fill="white"
          />
          <circle cx="40.5" cy="10.5" r="10.5" fill="white" />
          <path
            d="M38.5046 14H42.8126V12.884H41.3486V5.6L38.5766 6.476V7.652L40.0166 7.244V12.884H38.5046V14Z"
            fill="black"
          />
        </svg>
      </button>
      <v-btn class="line"></v-btn>
      <a target="_blank" href="https://www.instagram.com" class="social"
        >instagram</a
      >
      <a target="_blank" href="https://wa.me/5521991672783" class="social"
        >whatsapp</a
      >
    </div>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer :absolute="!fixed" app>
      <div class="somos-salacia">
        <p>nos somos</p>
        <h1>salacia</h1>
      </div>
      <div class="conte">
        <h1>
          conte qualquer <br />
          coisa pra gente.
        </h1>
      </div>
      <div class="journal">fique atualizado sobre nossos produtos.</div>
      <form action="">
        <input
          id="nome"
          v-model="name"
          type="text"
          name="nome"
          placeholder="nome"
          :class="isNameEmpty"
        />
        <input
          id="email"
          v-model="email"
          type="email"
          name="email"
          placeholder="email"
          :class="isEmailEmpty"
        />
        <v-btn text class="enviar"
          >enviar
          <svg
            width="80"
            height="16"
            viewBox="0 0 106 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0.999948 7.7169L104 8.01758"
              stroke="white"
              stroke-width="3"
            />
            <path
              d="M104 8.01758L98.0171 2.00009"
              stroke="white"
              stroke-width="3"
            />
            <path
              d="M104 8.01736L97.9822 13.9998"
              stroke="white"
              stroke-width="3"
            />
          </svg>
        </v-btn>
      </form>
      <div class="policies">
        <div class="copy">
          © Salacia 2021. Todos os Direitos <br />
          Reservados
        </div>
        <div class="copyright">
          <nuxt-link to="/servicos">
            <v-btn text class="copyright">serviços</v-btn>
          </nuxt-link>
          <nuxt-link to="/institucional">
            <v-btn text class="copyright">institucional</v-btn>
          </nuxt-link>
          <nuxt-link to="/cookies">
            <v-btn text class="copyright">cookies</v-btn>
          </nuxt-link>
        </div>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      toggle_exclusive: undefined,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      title: 'salacia'
    }
  },
  computed: {
    isEmailEmpty() {
      if (this.email.length > 0 && this.email !== undefined) {
        return 'active'
      }
      return ''
    },
    isNameEmpty() {
      if (this.name.length > 0 && this.name !== undefined) {
        return 'active'
      }
      return ''
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
  text-decoration: none;
}

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

@keyframes shop {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}

.shop:hover {
  animation: 1.3s shop infinite;
}

.social-line {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 120px;
  height: 776px;
  left: 91.1%;
  top: 22px;
  z-index: 2;

  .social {
    font-family: $font-stack-primary;
    font-weight: thin;
    font-size: $font-size-line;
    line-height: 29px;
    display: flex;
    align-items: center;
    text-align: center;
    color: $font-color-primary;
    transform: rotate(90deg);
    margin: 100px 5px 0 0;
  }
  .line {
    content: '' !important;
    display: block !important;
    height: 362px !important;
    min-width: 2px;
    max-width: 2px !important;
    width: 2px !important;
    background: $font-color-primary;
    padding: 0 !important;
    margin: 30px 5px 0 0;
  }
}

.v-footer {
  height: 600px;
  background: $background-color-footer;
  position: relative;
  padding: 0 100px;
  justify-content: space-evenly;
  align-items: flex-start;
  flex-direction: column;
}

.somos-salacia {
  > * {
    font-family: $font-stack-primary;
    margin-top: 0;
    margin-bottom: 0;
    display: flex;
    align-items: center;
    color: $font-color-primary;
  }
  p {
    font-weight: thin;
    font-size: $font-size-footer-small;
    line-height: 20px;
  }
  h1 {
    font-weight: bold;
    font-size: $font-size-footer-big;
    line-height: 32px;
  }
}

%base-footer-cta {
  display: flex;
  align-items: flex-end;
  color: $font-color-primary;
}

.conte {
  @extend %base-footer-cta;
  font-family: $font-stack-secondary;
  font-weight: normal;
  font-size: $font-size-footer-cta-header;
  line-height: 80px;
}
.journal {
  @extend %base-footer-cta;
  font-family: $font-stack-primary;
  font-weight: bold;
  font-size: $font-size-footer-cta-subheader;
  line-height: 36px;
}
form {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
input {
  margin-right: 30px;
  font-weight: bold;
  font-size: $font-size-footer-big;
  line-height: 48px;
  color: $font-color-primary;
  outline: none;
  opacity: 0.5;
  border-bottom: 1px solid $font-color-primary;
}

input:hover {
  opacity: 1;
  transition: 0.3s;
}

input.active {
  opacity: 1;
  transition: 0.3s;
}

@keyframes enviar {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(10px);
  }
  100% {
    transform: translateX(0);
  }
}

.enviar {
  font-weight: bold;
  font-size: $font-size-footer-big;
  line-height: 48px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-transform: lowercase;
  width: 250px !important;
  color: $font-color-primary;

  :hover svg {
    animation: 0.7s enviar infinite;
  }
}

%base-footer-policies {
  align-items: flex-end;
  color: $font-color-primary;
  display: flex;
  font-family: $font-stack-primary;
  font-weight: thin;
  font-size: $font-size-copyright;
  line-height: 22px;
  text-transform: uppercase;
}

.policies {
  @extend %base-footer-policies;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.copyright {
  @extend %base-footer-policies;
}
</style>
