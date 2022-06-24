<template>
  <v-container class="mt-4">
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <v-toolbar-title class="mt-n3">Welcome, Gorry</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-text-field
        label="Search product..."
        class="mt-6"
        color="brown"
        filled
        prepend-inner-icon="mdi-magnify"
        dense
        solo
        flat
        background-color="white"
      ></v-text-field>
      <v-btn
        tile
        fab
        small
        depressed
        color="#fff"
        class="btn-ico ml-3"
      >
        <v-icon dark>
          mdi-filter-outline
        </v-icon>
      </v-btn>
    </v-toolbar>
    <p class="caption px-4 mt-n6 grey--text">Discover whatever you need easily</p>
    <Category />
    <v-container>
      <Menu />
    </v-container>
  </v-container>
</template>

<script>
import Category from '@/components/Category.vue';
import Menu from '@/components/Menu.vue';

  export default {
    components: {
      Category,
      Menu
    }
  }
</script>

<style scoped>
.btn-ico {
  border-radius: 5px 5px 5px 5px;
}
</style>