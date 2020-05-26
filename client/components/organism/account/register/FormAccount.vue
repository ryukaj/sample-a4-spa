<template lang="pug">
v-container
  v-form
    v-row
      v-col(cols='12')
        v-text-field(label='ニックネーム' v-model='ui.name' required)
    v-row
      v-col(cols='12')
        v-text-field(label='パスワード' type="password" v-model='ui.password' required)
</template>

<script>
export default {
  data: () => ({
    ui: {
      name: '',
      password: ''
    }
  }),
  methods: {
    validate () {
      return true
    }
  },
  created () {
    console.log('account created')
  },
  mounted () {
    console.log('account mounted')
  }
}
</script>
