<template>
  <div class="">
    <section class="hero">
      <img src="~/static/ana_deitada.jpeg" class="hero-img" />
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

<style lang="scss" scoped>
@import url('http://fonts.cdnfonts.com/css/nexa-bold');
@import url('http://fonts.cdnfonts.com/css/qaligo');

.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-img {
  width: 100vw !important;
}

.content {
  position: absolute;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.seta {
  position: relative;
  right: 300px;

  :hover {
    animation: 0.7s enviar infinite;
  }
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

%generic-base-cta {
  display: flex;
  align-items: center;
}

%base-cta {
  @extend %generic-base-cta;
  font-style: normal;
  text-align: center;
  color: white;
}

.cta {
  @extend %generic-base-cta;
  height: 220px;
  right: 68.5px;
  position: relative;
  flex-direction: column;
  justify-content: space-evenly;

  p {
    @extend %base-cta;
    margin: 0;
    font-family: 'Nexa';
    font-weight: 300;
    font-size: 32px;
    line-height: 58px;
    align-items: flex-end;
  }

  h2 {
    @extend %base-cta;
    font-family: 'Qaligo';
    font-weight: normal;
    font-size: 32px;
    line-height: 70px;
    align-items: center;
  }

  .link {
    @extend %base-cta;
    width: 280px;
    height: 56px;
    align-content: center;
    align-items: center;
    justify-content: center;
    background: #72c6d5;
    font-family: 'Nexa';
    font-weight: bold;
    font-size: 20px;
    line-height: 24px;
  }
}
</style>
