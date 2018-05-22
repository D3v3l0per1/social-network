<template>
  <v-app dark>

    <v-toolbar>
      <v-toolbar-side-icon class="hidden-sm-and-up"></v-toolbar-side-icon>
      <v-toolbar-title>Social_Network</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat v-for="item in menuItems" :key="item.title">{{ item.title }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <router-view></router-view>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      menuItems: [
        { title: 'Test1', link: '' },
        { title: 'Test2', link: '' },
        { title: 'Test3', link: '' }
      ]
    }
  },
  name: 'App'
}
</script>
