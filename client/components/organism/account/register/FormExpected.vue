<template lang="pug">
v-container
  v-form
    v-row
      v-col(cols='3' md='4')
        label 職種（大分類）
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
    v-row
      v-col(cols='3' md='4')
        label 業界
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
    v-row
      v-col(cols='3' md='4')
        label 目的
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
    v-row
      v-col(cols='3' md='4')
        label フェーズ
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
    v-row
      v-col(cols='3' md='4')
        label 職種（中分類）
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
    v-row
      v-col(cols='3' md='4')
        label 職種（小分類）
      v-col(cols='9' md='8')
        v-radio-group(row)
          v-switch(label='A')
          v-switch(label='B')
          v-switch(label='C')
</template>

<script>
export default {
  methods: {
    validate () {
      return true
    }
  },
  created () {
    console.log('expected created')
  },
  mounted () {
    console.log('expected mounted')
  }
}
</script>
