<template lang="pug">
  .item
    .item_block.-left
    .item_block.-center
    .item_block.-right
</template>

<style lang="scss">
.item {
  @at-root {
    & {
      display: flex;
      justify-content: space-between;
      width: 100%;
      height: 100%;
      cursor: pointer;
      position: relative;
      z-index: 10;
      &:hover {
        .item_block {
          top: 15.625%;
        }
      }
    }
    .item_block {
      width: calc(33.333% - 1px);
      height: 68.75%;
      background: #ccc;
      position: relative;
      transition: top 0.4s $ease-out-cubic;
      &.-left {
        top: 31.25%;
      }
      &.-center {
        top: 15.625%;
      }
      &.-right {
        top: 0;
      }
    }
  }
}
</style>
