<template>
  <v-navigation-drawer app color="#fff" right width="330">
    <v-list subheader two-line class="mt-5">
      <v-list-item>
        <v-list-item-content>
          <h3>Current Order</h3>
        </v-list-item-content>
        <v-list-item-action>
          <v-btn
            tile
            fab
            small
            depressed
            color="#f8f8f8"
            class="btn-ico"
          >
            <v-icon dark>
              mdi-cog-outline
            </v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
    </v-list>

    <v-list three-line>
      <v-list-item v-for="(item, i) in orders" :key="i">
        <v-list-item-avatar size="70" rounded color="grey lighten-4">
          <v-img :src="item.image"></v-img>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title>
            {{ item.title }}
          </v-list-item-title>
          <v-list-item-subtitle>
            <v-row class="mt-1">
              <v-col cols="12" md="5" class="mt-1"> 
                <h3 style="color: #f46801;">${{ item.pay }}</h3>
              </v-col>
              <v-col cols="12" md="7" >
                <v-row no-gutters align="center">
                  <v-btn
                    tile
                    fab
                    dark
                    x-small
                    depressed
                    color="#f46801"
                    class="btn-action"
                  >
                    <v-icon dark>
                      mdi-plus
                    </v-icon>
                  </v-btn>
                  <div class="mx-3">{{ item.count }}</div>
                  <v-btn
                    tile
                    fab
                    dark
                    x-small
                    depressed
                    color="#f46801"
                    class="btn-action"
                  >
                    <v-icon dark>
                      mdi-minus
                    </v-icon>
                  </v-btn>
                </v-row>
              </v-col>
            </v-row>
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <v-card color="#f8f8f8" flat class="mt-3 mx-3">
      <v-card-text>
        <v-list>
          <v-list-item class="px-0" style="min-height: 25px;">
            <v-list-item-title>
              Subtotal
            </v-list-item-title>
            <v-list-item-subtitle class="text-right">
              $37.61
            </v-list-item-subtitle>
          </v-list-item>
          <v-list-item class="px-0" style="min-height: 25px;">
            <v-list-item-title>
              Discount sales
            </v-list-item-title>
            <v-list-item-subtitle class="text-right">
              $5.00
            </v-list-item-subtitle>
          </v-list-item>
          <v-list-item class="px-0" style="min-height: 25px;">
            <v-list-item-title>
              Total sales tax
            </v-list-item-title>
            <v-list-item-subtitle class="text-right">
              $2.25
            </v-list-item-subtitle>
          </v-list-item>
        </v-list>
      </v-card-text>
    </v-card>
    <div class="rip"></div>
    <v-card color="#f8f8f8" flat class="mx-3">
      <v-card-text>
        <v-list>
          <v-list-item class="px-0" style="min-height: 0px;">
            <v-list-item-title>
              <h3>Total</h3>
            </v-list-item-title>
            <v-list-item-subtitle class="text-right">
              <h3>$34.86</h3>
            </v-list-item-subtitle>
          </v-list-item>
        </v-list>
      </v-card-text>
    </v-card>
    <div class="mx-3 mt-4">
      <v-btn color="#f46801" depressed block dark class="text-capitalize">
        Continue to Payment
      </v-btn>
    </div>
  </v-navigation-drawer>
</template>

<script>
  export default {
    data: () => ({
      orders: [
        {
          image:'5.jpg', 
          title: 'Croissant Tenderloin Slice', 
          pay: '10.01',
          count: '1'
        },
        {
          image:'2.jpg', 
          title: 'Croissants Chocolate Chocochips', 
          pay: '22.02',
          count: '2'
        },
        {
          image:'1.jpg',
          title: 'Croissants Granulated Sugar',
          pay: '5.58',
          count: '1'
        },
      ]
    })
  }
</script>

<style scoped>
.btn-ico {
  border-radius: 5px 5px 5px 5px;
}
.btn-action {
  border-radius: 5px 5px 5px 5px;
  width: 25px !important;
  height: 25px !important;
}
.rip {
  position: relative;
  height: 20px;
  margin: 0 10px;
  background-color: #f8f8f8;
  background-size: 4px 2px;
  background-repeat: repeat-x;
  background-position: center;
  position: relative;
  background-image: url('../../public/hr.png')
}
.rip::after {
  transform: translate(-50%, -50%) rotate(225deg);
  right: -26px;
  content: "";
  position: absolute;
  width: 25px;
  height: 25px;
  top: 50%;
  border: 12px solid transparent;
  border-top-color: #fff;
  border-right-color: #fff;
  border-radius: 100%;
  pointer-events: none;
}
.rip::before {
  content: "";
  left: 0px;
  position: absolute;
  width: 25px;
  height: 25px;
  top: 50%;
  transform: translate(-50%, -50%) rotate(45deg);
  border: 12px solid transparent;
  border-top-color: #fff;
  border-right-color: #fff;
  border-radius: 100%;
  pointer-events: none;
}
.v-card {
  border-radius: 8px 8px 8px 8px !important;
}
</style>