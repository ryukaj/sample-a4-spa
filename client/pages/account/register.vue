<template lang="pug">
  main
    div hoge
    modal-account-register-form(ref='modal')
</template>

<script>
import modalAccountRegisterForm from '@/components/templates/account/register/Modal.vue'
export default {
  layout: 'guest',
  components: {
    modalAccountRegisterForm
  },
  data: () => ({}),
  created () {},
  mounted () {
    this.$refs.modal.open(0, true)
  }
}
</script>
