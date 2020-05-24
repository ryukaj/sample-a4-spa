<template lang="pug">
  div
    v-dialog(v-model='dialog' persistent scrollable)
      v-card
        v-toolbar(color='primary')
          v-btn(icon @click='close()')
            v-icon mdi-close
          v-toolbar-title TITLE
          v-spacer
          v-toolbar-items
            v-btn(text @click='save()') SAVE
        v-card-title
          span modal title
        v-card-text
          v-container(:is='currentComponent' ref='form')
</template>

<script>
import formAccount from '@/components/organism/account/register/FormAccount.vue'
import formExpected from '@/components/organism/account/register/FormExpected.vue'
export default {
  components: {
    formAccount
  },
  data: () => ({
    dialog: false,
    wizard: false,
    current: 0,
    formComponents: [formAccount, formExpected]
  }),
  computed: {
    currentComponent () {
      return this.formComponents[this.current]
    },
    isLastComponent () {
      return this.current === this.formComponents.length - 1
    }
  },
  methods: {
    open (aFromNumber, aIsWizard) {
      this.current = aFromNumber !== undefined && this.formComponents.length < aFromNumber ? aFromNumber : 0
      this.wizard = aIsWizard === true
      this.dialog = true
    },
    close () {
      this.dialog = false
    },
    save () {
      if (this.$refs.form.validate()) {
        // date store
        if (!this.wizard || this.isLastComponent) {
          this.dialog = false
        } else {
          this.current++
        }
      }
    }
  }
}
</script>
