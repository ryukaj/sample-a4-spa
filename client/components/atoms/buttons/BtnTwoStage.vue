<template lang="pug">
  div.l-btnTwoStage(v-ripple @click.prevent='onClick')
    .l-btnTwoStage__upper {{ upper }}
    .l-btnTwoStage__lower(v-if='!isMobile') {{ lower }}
</template>

<script>
export default {
  props: {
    upper: {
      type: String,
      required: true
    },
    lower: {
      type: String,
      required: true
    },
    linkto: {
      type: String,
      default: '',
      required: false
    }
  },
  computed: {
    isMobile () {
      return (this.$mq === 'mobile')
    },
    isInternalLink (path) {
      return !/^https?:\/\//.test(path)
    }
  },
  methods: {
    onClick () {
      if (this.linkto === '') { return }
      if (this.isInternalLink) {
        this.$router.push(this.linkto)
      } else {
        location.href = this.linkto
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.l-btnTwoStage {
  display: flex;
  flex-direction: column;
  padding: 0 0.5rem;
  justify-content: center;
  align-items: center;
  color: #fff;
  &__upper {
    text-align: center;
    padding-bottom: 2px;
  }
  &__lower {
    font-size: x-small;
    text-align: center;
    padding: 2px 1rem 0;
    text-transform: none;
    border-top: 1px solid #fff;
  }
}
</style>
