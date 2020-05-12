<template>
  <v-container text-xs-conter>
    <v-row justify="center">
      <v-col>
        <v-card
          max-width="344"
          min-height="450"
          class="mx-auto"
        >
          <v-card-text>
            <v-form>
              <UserEmail @inputEve="updateParams"/>
              <UserPass @inputEve="updateParams"/>
            </v-form>

            <div class="text-center my-10">
              <Button class="info">
                <template v-slot>
                  ログイン
                </template>
              </Button>
            </div>

          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  components: {
    Button: () => import('@/components/Atoms/Button'),
    UserEmail: () => import('@/components/Molecules/TextField/UserEmail'),
    UserPass: () => import('@/components/Molecules/TextField/UserPass')
    },
  methods: {
    updateParams(event) {
      console.log(event)
    }
  },
}
</script>