<template lang="pug">
  div
    v-dialog(v-model='dialog' persistent :scrollable='!isMobile' :fullscreen='isMobile')
      v-card
        v-toolbar(color='primary')
          v-btn(icon @click='close()')
            v-icon mdi-close
          v-toolbar-title TITLE
          v-spacer
          v-toolbar-items(v-if='isLastComponent')
            v-btn(text @click='save()') SAVE
        v-stepper.l-stepper(v-model='current' alt-labels)
          v-stepper-header
            template(v-for='(step, idx) in steps')
              v-stepper-step(
                :step='step.key'
              ) {{ step.name }}
              v-divider(v-if='idx < steps.length -1')
          v-stepper-items
            v-stepper-content(v-for='(step, idx) in steps' :step='step.key')
              v-container.l-stepper__form(:is='step.component' :ref='step.refname')
          v-container
            v-btn(@click='nextContent()') continue
</template>

<script>
import formAccount from '@/components/organism/account/register/FormAccount.vue'
import formExpected from '@/components/organism/account/register/FormExpected.vue'
export default {
  data: () => ({
    dialog: false,
    wizard: false,
    current: 1,
    steps: [
      { key: 1, name: 'ユーザ情報', component: formAccount, refname: 'formAccount' },
      { key: 2, name: '希望', component: formExpected, refname: 'formExpected' }
    ]
  }),
  computed: {
    isMobile () {
      return (this.$mq === 'mobile')
    },
    isLastComponent () {
      return this.current === this.steps.length
    },
    currentStep () {
      return this.steps[this.current - 1]
    }
  },
  methods: {
    open (aFromNumber, aIsWizard) {
      this.current = aFromNumber !== undefined && this.steps.length < aFromNumber ? aFromNumber : 1
      this.wizard = aIsWizard === true
      this.dialog = true
    },
    close () {
      this.dialog = false
    },
    save () {
      alert('saveボタン押下')
    },
    nextContent () {
      this.$refs[this.currentStep.refname][0].validate()
      if (this.isLastComponent) {
        this.close()
      } else {
        this.current++
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.l-stepper {
  &__form {
    max-height: 400px;
    overflow-y: scroll;
  }
}
</style>
