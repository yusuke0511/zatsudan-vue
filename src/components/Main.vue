<template>
  <v-app>
    <v-app-bar 
      color="#014c86"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title color="#FFFFFF">Menu</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item href="/">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
<!--
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
-->

          <v-list-item href="/howto">
            <v-list-item-icon>
              <v-icon>mdi-magnify</v-icon>
            </v-list-item-icon>
            <v-list-item-title>使い方</v-list-item-title>
          </v-list-item>

          <v-list-item href="/policy">
            <v-list-item-icon>
              <v-icon>mdi-file</v-icon>
            </v-list-item-icon>
            <v-list-item-title>利用規約</v-list-item-title>
          </v-list-item>

          <v-list-item href="https://forms.gle/ZX19uJTTFCrz8GVJ7" target="_blank">
           <v-list-item-icon>
              <v-icon>mdi-email</v-icon>
            </v-list-item-icon>
            <v-list-item-title>雑談ネタを投稿する</v-list-item-title> 
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <!-- Theme表示部分-->
    <router-view :itemList="items"/>
  </v-app>
</template>

<script>
import 'material-design-icons-iconfont/dist/material-design-icons.css';

export default {
  name: 'App',
  data: () => ({
    drawer: false,
    items:[],
  }),
  components: {
  },
};
</script>
