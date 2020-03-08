<template>
  <v-app>
    <Nav1 />
    <PlayPanel />
    <Songs />

    <!--<v-content class="ma-4">
      <router-view></router-view>
    </v-content>-->

  </v-app>
</template>

<script>
import Nav1 from './components/Nav1'
import PlayPanel from './components/PlayPanel'
import Songs from './components/Songs'

export default {
  name: 'App',

  components: {
    Nav1, PlayPanel, Songs
  },

  data: () => ({
    //
  }),
};
</script>

<style>
* {
font-family: Verdana, Geneva, Tahoma, sans-serif;
}
</style>