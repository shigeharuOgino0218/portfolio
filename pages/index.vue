<template lang="pug">
  .container
    h2.name 
      span HINA ADACHI PORTFOIO
    .center
      .center_inner
        IndexItem
        Lines
</template>

<script>
import IndexItem from "~/components/IndexItem.vue";
import Lines from "~/components/Lines.vue";

export default {
  data() {
    return {
      DOM: {}
    };
  },
  components: {
    IndexItem,
    Lines
  },
  mounted() {
    const DOM = this.DOM;
    DOM.center = document.querySelector(".center");
    DOM.inner = document.querySelector(".center_inner");
    const height = DOM.center.clientHeight;
    DOM.inner.style.width = height + "px";
    // DOM.name.style.width = (window.innerWidth - height) / 2 + "px";
    // DOM.name.style.fontSize = ((height * 0.3125) / 2) * 0.5625 + "px";
  }
};
</script>

<style lang="scss">
.name {
  width: 100%;
  height: calc((100vh - #{$center-height}) / 2);
  text-align: center;
  position: absolute;
  left: 0;
  bottom: 0;
  padding: 20px;
  span {
    display: block;
    font-family: $font-en;
    font-size: 20px;
    font-weight: 900;
    color: #fff;
    letter-spacing: 0.05em;
    line-height: 1.15;
    position: relative;
    z-index: 100;
  }
}

.center {
  @at-root {
    & {
      width: 100%;
      height: $center-height;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
    .center_inner {
      width: 0;
      height: 100%;
      margin: 0 auto;
      position: relative;
    }
  }
}
</style>
