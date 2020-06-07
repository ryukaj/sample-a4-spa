<template lang="pug">
  main.l-main
    .l-main__content
      .l-main__content__gradation
        .type1
        .type2
        .type3
        .type4
        .type5
        .type6
        .type7
        .type8
        .type9
        .type10
      .l-main__content__message
        div エンジニアのことは
        div エンジニアに聞け
        div.stress Ask the engineer about the engineer
      .l-main__content__gradation
        .type10
        .type9
        .type8
        .type7
        .type6
        .type5
        .type4
        .type3
        .type2
        .type1
</template>

<script>
export default {
  layout: 'guest',
  created: () => {}
}
</script>

<style lang="scss" scoped>
.l-main {
  position: relative;
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  background-image: url('/images/layout/pcandcoffee.jpg');
  background-size: cover;
  &__content {
    position: relative;
    left: 2rem;
    background-color: #000;
    opacity: .5;
    &__message {
      padding: 1rem 2rem;
      color: #fff;
      font-size: xxx  -large;
      > div {
        margin-bottom: 0.5rem
      }
      .stress {
        color: #f39800;
        font-size: xx-large;
      }
    }
    &__gradation {
      display: flex;
      width: 100%;
      height: 3rem;
      > div {
        width: 10%;
      }
      .type1 {
        background-color: #000;
      }
      .type2 {
        background-color: #191919;
      }
      .type3 {
        background-color: #323232;
      }
      .type4 {
        background-color: #4c4c4c;
      }
      .type5 {
        background-color: #666;
      }
      .type6 {
        background-color: #7f7f7f;
      }
      .type7 {
        background-color: #999;
      }
      .type8 {
        background-color: #b2b2b2;
      }
      .type9 {
        background-color: #ccc;
      }
      .type10 {
        background-color: #fff;
      }
    }
  }

}
</style>

<style>
.page-enter {
  opacity: 0;
}
.page-enter-active {
  transition: opacity 2s;
}
</style>
