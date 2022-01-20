<template>
  <v-container>
    <v-row>
      <v-col sm="6" md="3">
        <v-card class="mx-auto" max-width="344" color="cyan" dark>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">Today Sale</div>
              <v-list-item-title class="text-h5 mb-1">
               $ 500
              </v-list-item-title>
             </v-list-item-content>
             <v-avatar color="primary">
              <v-icon dark>
                mdi-currency-usd
              </v-icon>
            </v-avatar>
          </v-list-item>
        </v-card>
      </v-col>
      <v-col sm="6" md="3">
        <v-card class="mx-auto" max-width="344"  color="green darken-2" dark>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">Today Expense</div>
              <v-list-item-title class="text-h5 mb-1">
                $ 50
              </v-list-item-title>
             </v-list-item-content>
             <v-avatar color="warning">
              <v-icon dark>
                mdi-currency-usd
              </v-icon>
            </v-avatar>
          </v-list-item>
        </v-card>
      </v-col>
      <v-col sm="6" md="3">
        <v-card class="mx-auto" max-width="344"  color="cyan lighten-3" dark>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">Today User</div>
              <v-list-item-title class="text-h5 mb-1">
                 5
              </v-list-item-title>
             </v-list-item-content>
             <v-avatar color="indigo">
              <v-icon dark>
                mdi-account-circle
              </v-icon>
            </v-avatar>
          </v-list-item>
        </v-card>
      </v-col>
      <v-col sm="6" md="3">
        <v-card class="mx-auto" max-width="344"  color="red accent-3" dark>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">Today Due</div>
              <v-list-item-title class="text-h5 mb-1">
                $ 50
              </v-list-item-title>
             </v-list-item-content>
             <v-avatar color="red darken-1">
              <v-icon dark>
                mdi-currency-usd
              </v-icon>
            </v-avatar>
          </v-list-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Home",
  components: {},
};
</script>
