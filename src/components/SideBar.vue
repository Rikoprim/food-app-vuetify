<template>
  <v-navigation-drawer
    app
    color="#fff"
    mini-variant
    mini-variant-width="90"
  >
  <v-avatar class="d-block text-center mx-auto mt-4">
    <v-icon color="#f46801" x-large>shopify</v-icon>
  </v-avatar>
  <v-divider class="mx-5 mt-3"></v-divider>
  <v-list flat class="mt-4">
    <v-list-item-group v-model="selectedItem" active-class="border">
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :ripple="false"
        v-slot="{ active }"
      >
      <v-list-item-content>
        <v-icon v-text="active ? item.icon : item.icon+'-outline'" :color="active ? '#f46801' : '#bebebe'"></v-icon>
      </v-list-item-content>
      </v-list-item>
    </v-list-item-group>
  </v-list>
    <template v-slot:append>
      <div class="pa-2">
        <v-list flat class="mt-4">
          <v-list-item-group>
            <v-list-item
              v-for="(item, i) in items1"
              :key="i"
              :ripple="false"
            >
            <v-list-item-content>
              <v-icon v-text="item.icon" color="#bebebe"></v-icon>
            </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </div>
    </template>
  </v-navigation-drawer>
</template>

<script>
  export default {
    data: () => ({
      selectedItem: 0,
      drawer: true,
      items: [
        { icon: "mdi-home" },
        { icon: "mdi-room-service" },
        { icon: "mdi-receipt" },
        { icon: "mdi-bookmark" },
        { icon: "mdi-wallet" },
      ],
      items1: [
        { icon: "mdi-cog-outline" },
        { icon: "mdi-logout" },
      ],
    })
  }
</script>

<style scoped>
.border {
  border-right: 2px solid #f46801;
}
</style>