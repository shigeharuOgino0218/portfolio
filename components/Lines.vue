<template lang="pug">
  .container
    .line.-vertical
      .line_item
      .line_item
      .line_item
      .line_item
    .line.-horizontal
      .line_block
        .line_item
        .line_item
        .line_item
      .line_block.-center
        .line_logo
          img(src="/img/logo-outline.svg", alt="")
          img(src="/img/logo-outline.svg", alt="")
          img(src="/img/logo-outline.svg", alt="")
      .line_block
        .line_item
        .line_item
        .line_item
</template>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  pointer-events: none;
}

.line {
  @at-root {
    & {
      position: absolute;
      &.-vertical {
        display: flex;
        justify-content: space-between;
        width: 100%;
        height: 100vh;
        top: 50%;
        transform: translate(0, -50%);
        .line_item {
          width: 1px;
          height: 100%;
          &:nth-child(odd) {
            transform-origin: top;
          }
          &:nth-child(even) {
            transform-origin: bottom;
          }
        }
      }
      &.-horizontal {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 100vw;
        height: 100%;
        left: 50%;
        transform: translate(-50%, 0);
        .line_block {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          height: 31.25%;
          &.-center {
            justify-content: center;
            width: auto;
            height: 37.5%;
            overflow: hidden;
          }
        }
        .line_item {
          width: 100%;
          height: 1px;
          &:nth-child(odd) {
            transform-origin: left;
          }
          &:nth-child(even) {
            transform-origin: right;
          }
        }
      }
    }
    .line_item {
      background: #fff;
      opacity: 0.05;
      backface-visibility: hidden;
    }
    .line_logo {
      display: flex;
      width: 1000%;
      height: 50%;
      img {
        display: block;
        height: 100%;
        opacity: 0.25;
        animation: logo 30s linear infinite;
        padding: 0 1.125vh;
      }
    }
  }
}

@keyframes logo {
  0% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(-100%, 0);
  }
}
</style>
