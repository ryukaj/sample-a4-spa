<template lang="pug">
  v-app
    v-navigation-drawer(app v-model='drawer')
      v-list
        v-list-item
          v-avatar
            v-img(src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg")
          v-list-item-title 〇〇〇〇さん
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title アドバイスする
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title キャリア登録・更新
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title 受取一覧
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title 実施一覧
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title 登録情報更新
    v-app-bar(app)
      v-app-bar-nav-icon(@click.stop="drawer = !drawer")
      v-toolbar-title A4 Mypage
    v-content
      v-container
        transition(name='page')
          nuxt
    v-footer(app)
      span A4 Footer
</template>

<script>
export default {
  data: () => ({
    drawer: null
  }),
  created: () => {}
}
</script>
