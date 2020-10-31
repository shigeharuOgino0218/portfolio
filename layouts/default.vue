<template lang="pug">
  #app
    img(src="/img/logo.svg", alt="").logo
    Nuxt
    p.copyright &copy; 2020 Shigeharu Ogino
</template>

<style lang="scss">
#app {
  background: rgba(#000, 0.85);
  width: 100%;
  height: 100vh;
  position: relative;
}

.logo {
  width: 220px;
  position: fixed;
  left: 40px;
  top: 30px;
  mix-blend-mode: exclusion;
}

.copyright {
  font-family: $font-en;
  font-size: 12px;
  color: #fff;
  position: absolute;
  right: 20px;
  bottom: 20px;
}
</style>
