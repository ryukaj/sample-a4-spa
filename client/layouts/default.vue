<template lang="pug">
  v-app
    v-navigation-drawer(app v-model='drawer')
      v-list
        v-list-item(to='/' nuxt)
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title Home
        v-list-item(to='/inspire' nuxt)
          v-list-item-action
            v-icon mdi-charity
          v-list-item-content
            v-list-item-title sample
        v-list-item(to='/parallax' nuxt)
          v-list-item-action
            v-icon mdi-charity
          v-list-item-content
            v-list-item-title Parallax
        v-list-item(to='/account/register' nuxt)
          v-list-item-action
            v-icon mdi-charity
          v-list-item-content
            v-list-item-title landing
    v-app-bar(app)
      v-app-bar-nav-icon(@click.stop="drawer = !drawer")
      v-toolbar-title A4 Header
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
