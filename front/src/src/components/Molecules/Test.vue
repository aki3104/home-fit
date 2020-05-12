<template>
  <div>
    <Button class="info">
      <template v-slot>
        test
      </template>
    </Button>

    <template>
      <Button :context="context" :styles="styles">
      </Button>
    </template>

      <v-form>
        <UserEmail @inputEve="updateParams"/>
      </v-form>

  </div>
</template>

<script>
  export default {
    components: {
      Button: () => import('@/components/Atoms/Button'),
      UserEmail: () => import('@/components/Molecules/TextField/UserEmail')
    },
    data() {
      return {
        styles: 'info',
        context: 'test2'
      }
    },
    methods: {
      updateParams(event) {
        console.log(event)
      }
    },
    
  }

</script>
