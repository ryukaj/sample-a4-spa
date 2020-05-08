<template lang="pug">
  main
    v-app-bar(app v-if='parallax.subHeight < position')
      v-toolbar-title forAdvice
      v-spacer
      div.dummylink Log In
      div.dummylink New Entry
      div.dummylink Try
    v-parallax.l-parallax(:height='parallax.mainHeight' src='images/parallax/main.png')
      .l-parallax__content.l-parallax__msg
        div エンジニアのことはエンジニアに聞け
        div Ask the engineer about the engineer
      .l-parallax__content.l-parallax__nav
        v-row
          v-col(cols=12 align='center') forAdvice
        v-row.l-parallax__nav__links(align='center' justify='center')
          v-col(cols=3 align='center') Log In
          v-col(cols=3 align='center') New Entry
          v-col(cols=3 align='center') Try
        v-row(align='center' justify='center')
          v-col(cols=3 align='center') 会員の方はこちら
          v-col(cols=3 align='center') 新規登録はこちら
          v-col(cols=3 align='center') 登録せずに見たい方はこちら
    v-parallax.l-parallax(:height='parallax.subHeight' src='images/parallax/sub1.png' style='margin-top:100px;')
</template>

<script>
export default {
  layout: 'guest',
  data: () => ({
    parallax: {
      mainHeight: 600,
      subHeight: 500
    },
    position: 0
  }),
  created() {},
  mounted() {
    this.$set(this.parallax, 'mainHeight', window.innerHeight)
    this.$set(this.parallax, 'subHeight', window.innerHeight - 100)
    document.onscroll = (e) => {
      this.position = document.documentElement.scrollTop
    }
  }
}
</script>

/* lang="scss" scoped */
<style>
.dummylink {
  padding-right: 1rem;
  margin-right: 1rem;
  border-right: 1px solid #000;
}
.l-parallax {
  position: relative;
  background-color: #000;
}
.l-parallax__content {
  width: 960px;
  margin: auto;
}
.l-parallax__msg {
  font-size: xx-large;
}
.l-parallax__nav {
  color: #1631a3;
}
.l-parallax__nav__links {
  border-top: 2px solid #1631a3;
  border-bottom: 2px solid #1631a3;
}
</style>
