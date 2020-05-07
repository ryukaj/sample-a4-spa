<template lang="pug">
  article
    div#parallax_container
      v-row.container_btn
        div.title A4 タイトル
        div.btnarea
          v-card
            .font-weight-light Log in
            .text-center.font-weight-black 会員の方はこちら
          v-card
            .font-weight-light New Entry
            .text-center.font-weight-black 新規登録
          v-card
            .font-weight-light TRY
            .text-center.font-weight-black 登録なし
      v-parallax.content_parallax(height='550' src='https://cdn.vuetifyjs.com/images/parallax/material.jpg')
        v-col 
          p エンジニアのことはエンジニアに聞け！
          p Ask the engineer about the engineer
      v-parallax.content_parallax(height='550' src='https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg')
        v-col 
          p エンジニアの成長は人類の成長である
          p Engineer growth is human growth
      v-parallax.content_parallax(height='550' src='https://cdn.vuetifyjs.com/images/parallax/material2.jpg ')
        v-col 
          p ４つのコンセプトによるアドバイス
</template>

<script>
export default {
  created: () => {}
}
</script>

/* lang="scss" scoped */
<style>
#parallax_container {
  position: relative;
  padding-bottom: 100px;
}
.container_btn {
  border: 1px solid red;
  top: 550px;
  left: 320px;
  width: 1162px;
  height: 150px;
  padding-bottom: 1rem;
  position: fixed;
  background-color: #fff;
  z-index: 1000;
}
.title {
  width: 100%;
  text-align: center;
}
.btnarea {
  display: flex;
  width: 100%;
  padding: 0 40px;
  justify-content: space-between;
}
.btnarea .v-card {
  width: 150px;
}
</style>
