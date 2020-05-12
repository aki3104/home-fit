<template>
  <v-text-field
    prepend-icon='fa-key'
    label='password'
    @input="inputText($event)"
    @click:append="showPass = !showPass"
    value=""
    :append-icon="showPass ? 'mdi-eye' : 'mdi-eye-off'"
    :rules="[rules.required, rules.min]"
    :type="showPass ? 'text' : 'password'"
    hint="8文字以上"
  />
</template>

<script>
export default {
  data () {
    return {
      showPass: false,
      rules: {
        required: value => !!value || 'パスワードを入力してください',
        min: value => value.length >= 8 || 'パスワードが８文字以下です。',
        emailMatch: () => ('The email and password you entered don\'t match'),
      }
    }
  },
  methods: {
    inputText(event) {
      //text-fieldの内容と名前を親要素に渡す
      this.$emit('inputEve', { value: event, name: 'password'})
    }
  }
}
</script>