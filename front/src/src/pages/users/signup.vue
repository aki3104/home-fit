<template>
  <UserSignup />
</template>
<script>
export default {
  components: {
    UserSignup: () => import('@/components/Organisms/UserSignup')
  }
}
</script>