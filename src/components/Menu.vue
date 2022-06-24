<template>
  <v-row>
    <v-col cols="12" md="4" v-for="(item, i) in menus" :key="i">
      <v-card class="rounded-lg px-4 pt-4">
        <v-img
          height="200"
          :src="item.image"
        >
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
            <v-spacer></v-spacer>
              <v-btn
                tile
                fab
                small
                depressed
                color="white"
                class="btn-ico ml-3"
              >
                <v-icon dark color="orange">
                  mdi-cart-minus
                </v-icon>
              </v-btn>
          </v-app-bar>
        </v-img>

        <v-card-title class="px-0 text-h6">{{ item.title }}</v-card-title>
        <v-card-text class="px-0">
          <div>{{ item.desc }}</div>
          <h2 class="mt-3 orange--text">${{item.pay}} <span class="grey--text text-subtitle-2"> / {{ item.pcs }} pcs</span></h2>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      menus: [
        {
          image:'4.jpg', 
          title: 'Almond Brown Sugar Croissant', 
          desc: 'Sweet Croissant with topping almonds and brown sugar',
          pay: '12.98',
          pcs: '3'
        },
        {
          image:'5.jpg', 
          title: 'Smoke Tenderloin Slice Croissant', 
          desc: 'Plain croissant with smoke tenderloin beef sliced and vegetable',
          pay: '10.01',
          pcs: '2'
        },
        {
          image:'6.jpg',
          title: 'Berry Whipped Cream Croissant',
          desc: 'Sweet croissant with blueberries and starwberries inside',
          pay: '8.92',
          pcs: '3'
        },
                {
          image:'1.jpg', 
          title: 'Sweet Granulated Sugar Croissant', 
          desc: 'Sweet Croissant with topping almonds and brown sugar',
          pay: '14.02',
          pcs: '3'
        },
        {
          image:'2.jpg', 
          title: 'Smoke Chocolate Chocochips Croissant', 
          desc: 'Plain croissant with smoke tenderloin beef sliced and vegetable',
          pay: '15.01',
          pcs: '2'
        },
        {
          image:'3.jpg',
          title: 'Basic Croissant La Ta Dhore',
          desc: 'Sweet croissant with blueberries and starwberries inside',
          pay: '9.92',
          pcs: '3'
        },
      ]
    }) 
  }
</script>

<style scoped>
.btn-ico {
  border-radius: 5px 5px 5px 5px;
}
.v-card > *:first-child:not(.v-btn):not(.v-chip):not(.v-avatar), .v-card > .v-card__progress + *:not(.v-btn):not(.v-chip):not(.v-avatar) {
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}
</style>