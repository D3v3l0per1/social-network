<template>
  <v-app dark>

    <v-toolbar dense fixed>
      <v-toolbar-side-icon class="hidden-sm-and-up"></v-toolbar-side-icon>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat v-for="item in leftMenuItems" :key="item.title">{{ item.title }}</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-icon v-for="item in rightMenuItems" :key="item.title">{{item.icon}}</v-icon>
      </v-toolbar-items>
    </v-toolbar>

    <v-container>
      <router-view></router-view>
    </v-container>

  </v-app>
</template>

<script>
export default {
  data () {
    return {
      leftMenuItems: [
        { title: 'Home' },
        { title: 'Wassup' },
        { title: 'Groups' }
      ],
      rightMenuItems: [
        { icon: 'supervisor' },
        { icon: '' },
        { icon: '' }
      ]
    }
  },
  name: 'App'
}
</script>
