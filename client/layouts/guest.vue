<template lang="pug">
  v-app.l-guest
    v-app-bar.l-header(app)
      v-row.l-header__row
        .l-header__row__left
          .l-header__row__left__search
            v-toolbar-title.l-header__row__left__logo
            v-text-field(solo-inverted flat hide-details label="Search.." prepend-inner-icon="mdi-magnify" v-if='!isMobile')
          .l-header__row__left__gradation(v-if='!isMobile')
            .gradation.type1
            .gradation.type2
            .gradation.type3
        .l-header__row__right
          btn-two-stage(upper='Log in' lower='会員の方はこちら')
          btn-two-stage(upper='New Entry' lower='新規登録はこちら' linkto='/account/register')
          btn-two-stage(upper='Try' lower='登録せずに見たい方はこちら')
    v-content
      v-container
        transition(name='page')
          nuxt
    v-footer(app color='primary')
      span A4 Footer
</template>

<script>
import btnTwoStage from '@/components/atoms/buttons/BtnTwoStage.vue'
export default {
  components: {
    btnTwoStage
  },
  data: () => ({
    drawer: null
  }),
  computed: {
    isMobile () {
      return (this.$mq === 'mobile')
    }
  },
  created: () => {}
}
</script>

<style lang="scss" scoped>
.l-header {
  &__row {
    background-color: #f39800 !important;
    justify-content: space-between;
    height: 100%;
    margin: 0;
    &__left {
      height: 100%;
      flex-grow: 2;
      display: flex;
      justify-content: space-between;
      background-image: url('/images/layout/handshake.jpg');
      background-position: left;
      background-size: cover;
        &__logo {
          width: 64px;
          height: 100%;
          background-image: url('/images/layout/header_logo.png');
          background-size: cover;
          background-position: center;
          margin: 0 0.5rem;
        }
        &__search {
          display: flex;
          align-items: center;
          flex-grow: 2;
        }
        &__gradation {
        display: flex;
        .gradation {
          width: 3rem;
          height: 100%;
          background: #f39800;
        }
        .type1 {
          opacity: 0.3;
        }
        .type2 {
          opacity: 0.6;
        }
        .type3 {
          opacity: 0.9;
        }
      }
    }
    &__right {
      display: flex;
    }
  }
}
</style>

<style>
.l-guest .v-toolbar__content {
  padding: 0;
}
</style>
