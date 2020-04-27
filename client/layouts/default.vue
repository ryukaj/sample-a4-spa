<template lang="pug">
  v-app
    v-navigation-drawer(app v-model='drawer')
      v-list
        v-list-item
          v-list-item-action
            v-icon mdi-home
          v-list-item-content
            v-list-item-title Home
    v-app-bar(app)
      v-app-bar-nav-icon(@click.stop="drawer = !drawer")
      v-toolbar-title A4 Header
    v-content
      v-container
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
