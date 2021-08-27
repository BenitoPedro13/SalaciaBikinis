<template>
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
</template>

<script>
export default {
    name: 'SocialLine'
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

</style>