<template>
  <div class="">
    <section class="hero">
      <v-img
        src="/_nuxt/static/ana_deitada.jpeg"
        lazy-src="/_nuxt/static/ana_deitada-min.jpeg"
        class="hero-img"
      >
        <template #placeholder>
          <v-row class="fill-height ma-0" align="center" justify="center">
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
      <div class="content">
        <v-btn text class="seta">
          <svg
            width="105"
            height="14"
            viewBox="0 0 105 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M104.017 7.28317L1.01758 6.98248"
              stroke="white"
              stroke-width="1.5"
            />
            <path
              d="M1.01758 6.98248L7.00004 13"
              stroke="white"
              stroke-width="1.5"
            />
            <path
              d="M1.0174 6.98252L7.03489 1.00006"
              stroke="white"
              stroke-width="1.5"
            />
          </svg>
        </v-btn>

        <div class="cta">
          <p>coleçao carnaval 2022</p>
          <h2>vastidao, sol e mar</h2>
          <nuxt-link to="/bikinis" class="link">ver bikinis</nuxt-link>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
@import url('http://fonts.cdnfonts.com/css/nexa-bold');
@import url('http://fonts.cdnfonts.com/css/qaligo');

html {
  font-family: 'Nexa', 'Roboto';
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
.branco {
  color: white !important;
  mix-blend-mode: difference !important;
}
.preto {
  color: black !important;
  mix-blend-mode: exclusion !important;
}

.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}
.hero .content {
  position: absolute;
  display: flex;
  align-items: center;
}
.seta {
  position: relative;
  right: 300px;
}
.content .seta:hover {
  animation: 0.7s enviar infinite;
}
@keyframes enviar {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(-10px);
  }
  100% {
    transform: translateX(0);
  }
}
.hero .cta {
  height: 220px;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}
.cta p {
  margin: 0;
  font-family: 'Nexa';
  font-style: normal;
  font-weight: 300;
  font-size: 32px;
  line-height: 58px;
  display: flex;
  align-items: flex-end;
  text-align: center;
  color: white;
}
.cta h2 {
  font-family: Qaligo;
  font-style: normal;
  font-weight: normal;
  font-size: 32px;
  line-height: 70px;
  display: flex;
  align-items: center;
  text-align: center;
  color: white;
}
.cta .link {
  color: white;
  width: 280px;
  height: 56px;
  display: flex;
  align-content: center;
  align-items: center;
  text-align: center;
  justify-content: center;
  background: #72c6d5;
  font-family: Nexa;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
}
</style>
