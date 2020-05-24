<template lang="pug">
  article
    v-row
      v-col(cols=12 md=6)
        <!-- Carousel TODO: 切り出し -->
        v-carousel(height='360')
          v-carousel-item
            v-sheet(height='100%')
              v-row.fill-height(align='center' justify='center')
                div.display-1 登録・運用ルール
          v-carousel-item
            v-sheet(height='100%')
              v-row.fill-height(align='center' justify='center')
                div.display-1 A4への想い
          v-carousel-item
            v-sheet(height='100%')
              v-row.fill-height(align='center' justify='center')
                div.display-1 ４つのコンセプトによるアドバイス
          v-carousel-item
            v-sheet(height='100%')
              v-row.fill-height(align='center' justify='center')
                div.display-1 ４つのこだわり
      v-col(cols=12 md=6) セクション＃アカウント作成
    v-row(justify='center')
      v-col(cols=12 md=2 align='center')
        v-card
          .font-weight-light 開発
          .text-center.font-weight-black 100人
      v-col(cols=12 md=2 align='center')
        v-card
          .font-weight-light インフラ
          .text-center.font-weight-black 100人
      v-col(cols=12 md=3 align='center')
        v-card
          .font-weight-light 登録エンジニア
          .text-center.font-weight-black 100人
      v-col(cols=12 md=2 align='center')
        v-card
          .font-weight-light テクサポ
          .text-center.font-weight-black 100人
      v-col(cols=12 md=2 align='center')
        v-card
          .font-weight-light その他
          .text-center.font-weight-black 100人
</template>

<script>
export default {
  created: () => {}
}
</script>

/* lang="scss" scoped */
<style>
.page-enter {
  opacity: 0;
}
.page-enter-active {
  transition: opacity 2s;
}
</style>
