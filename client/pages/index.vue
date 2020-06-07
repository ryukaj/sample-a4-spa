<template lang="pug">
  main
    div hoge
</template>

<script>
export default {
  layout: 'guest',
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
