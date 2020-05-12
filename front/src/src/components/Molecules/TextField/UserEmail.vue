<template>
  <v-text-field
    prepend-icon='fa-envelope'
    label='メールアドレス'
    @input="inputText($event)"
  />
</template>

<script>
export default {
  methods: {
    inputText(event) {
      //text-fieldの内容と名前を親要素に渡す
      this.$emit('inputEve', { value: event, name: 'email'})
    }
  }
}
</script>