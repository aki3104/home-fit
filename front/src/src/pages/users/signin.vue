<template>
  <UserSignin />
</template>
<script>
export default {
  components: {
    UserSignin: () => import('@/components/Organisms/UserSignin')
  }
}
</script>