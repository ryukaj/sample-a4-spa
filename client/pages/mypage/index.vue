<template lang="pug">
main.l-main
  v-container
    v-row
      v-col(cols='12' sm='2')
        v-row
          v-col アドバイス受取数
            div ●●件
        v-row
          v-col アドバイス実施数
            div ●●件
        v-row
          v-col ●●さんと同じ職種登録数
            div ●●人
        v-row
          v-col エンジニア総登録数
            div ●●人
      v-col(cols='12' sm='6')
        v-row
          v-col(cols='12' sm='6') スペシャリストランク
            div S6
          v-col(cols='12' sm='6') マネジメントランク
            div M4
        v-row
          v-col(cols='12') アドバイス実施エンジニアからの返信
            div aaaaaa
            div bbbbbb
            div ccccc
        v-row
          v-col(cols='12') 事務局からのご連絡
            div aaaaaa
            div bbbbbb
            div ccccc
        v-row
          v-col(cols='12') レーダーチャート配置
      v-col(cols='12' sm='4')
        v-row
          v-col(cols='12') これまでの経験
            v-timeline
              v-timeline-item
                v-card sample1
              v-timeline-item
                v-card sample2
              v-timeline-item
                v-card sample3
        v-row
          v-col(cols='12') これからのキャリア
           v-timeline
            v-timeline-item
              v-card sample1
            v-timeline-item
              v-card sample2
            v-timeline-item
              v-card sample3

</template>

<script>
import { Radar } from 'vue-chartjs'

export default {
  extends: Radar,
  layout: 'prototype',
  created: () => {},
  mounted () {
  }
}
</script>

<style lang="scss" scoped>
.l-main {
    position: relative;
}
</style>
