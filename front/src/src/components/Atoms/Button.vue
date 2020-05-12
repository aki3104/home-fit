<template>
  <v-btn @click="onClick">
    <slot />
  </v-btn>
</template>

<script>
export default {
  methods: {
    onClick() {
      this.$emit("click")
    }
  }
}
</script>