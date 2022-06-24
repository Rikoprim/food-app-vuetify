<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" md="2">
        <v-btn color="white" large depressed>
          <v-icon left dark>mdi-star-settings-outline</v-icon>
            Signature
        </v-btn>
      </v-col>
      <v-col cols="12" md="2" class="text-center">
        <v-btn color="orange" dark large depressed>
          <v-icon left dark>mdi-food-croissant</v-icon>
            Bakery
        </v-btn>
      </v-col>
      <v-col cols="12" md="2" class="text-center">
        <v-btn color="white" large depressed>
          <v-icon left dark>mdi-dharmachakra</v-icon>
            Waffle
        </v-btn>
      </v-col>
      <v-col cols="12" md="2" class="text-center">
        <v-btn color="white" large depressed>
          <v-icon left dark>mdi-coffee-outline</v-icon>
            Coffee
        </v-btn>
      </v-col>
      <v-col cols="12" md="2">
        <v-btn color="white" large depressed>
          <v-icon left dark>mdi-rice</v-icon>
            Ice Cream
        </v-btn>
      </v-col>
      <v-col cols="12" md="2" class="text-right">
        <v-btn color="white" large depressed>
          <v-icon left dark>mdi-receipt-outline</v-icon>
            Snack
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
      
  }
</script>

<style scoped>
.actives {
  background-color: orange;
}
</style>