<template lang="pug">
v-container
  v-form
    v-row
      v-col(cols='12')
        v-text-field(label='ニックネーム' required)
    v-row
      v-col(cols='12')
        v-text-field(label='パスワード' type="password" required)
</template>

<script>
export default {
  methods: {
    validate () {
      return true
    }
  },
  created () {
    alert('account created')
  },
  mounted () {
    alert('account mounted')
  }
}
</script>
