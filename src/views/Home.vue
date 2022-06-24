<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <SideBar />
    <SideBarRight />
    <Content />
  </v-app>
</template>

<script>
// @ is an alias to /src
import SideBar from '@/components/SideBar.vue'
import SideBarRight from '@/components/SideBarRight.vue'
import Content from '@/components/Content.vue'

export default {
  name: 'Home',
  components: {
    SideBar,
    SideBarRight,
    Content,
  }
}
</script>
