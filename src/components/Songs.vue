<template>
  <div class="songs">
    <p class="ma-0 mx-2 py-2 primary--text">Songs</p>
    <v-card max-width="500" class="card-style" tile v-for="a in 10" :key="a">
      <v-list-item class="ma-0 pa-0">
        <v-list-item-avatar color="grey" class="mx-2"></v-list-item-avatar>
        <v-list-item-content class="ma-0 pa-0 primary--text">
          <v-list-item-title class="subheadline">Our Changing Planet</v-list-item-title>
          <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle>
      </v-list-item-content>
      </v-list-item>
    </v-card>
  </div>
</template>

<style scoped>
.card-style {
margin-bottom: 5px;
}
.card-style:last-child {
margin-bottom: 0px;
}
</style>>