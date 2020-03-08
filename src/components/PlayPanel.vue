<template>
  <div class="songs">
    <v-card max-width="500" tile flat>
      <v-img class="white--text align-end" height="200px" src="https://www.kenyon.edu/files/pages/music-2.jpg">
        <v-card-title class="timer">
          Song Name <v-spacer></v-spacer>00:00 / 03:10
        </v-card-title>
      </v-img>
      <v-divider></v-divider>

      <v-slider v-model="value" class="slide" min="0" max="100"></v-slider>

      <v-card-actions class="pa-0 px-2 py-1">
        <v-btn color="primary" icon @click="liked">
          <v-icon>{{ liked1 ? 'mdi-heart' : 'mdi-heart-outline' }}</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn color="primary" icon outlined>
          <v-icon>mdi-skip-previous</v-icon>
        </v-btn>
        <v-btn color="primary" icon @click="play" fab outlined>
          <v-icon>{{ play1 ? 'mdi-play-outline' : 'mdi-stop' }}</v-icon>
        </v-btn>
        <v-btn color="primary" icon outlined>
          <v-icon>mdi-skip-next</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn color="primary" icon @click="repeat">
          <v-icon>{{ repeat1 ? 'mdi-repeat' : 'mdi-repeat-once' }}</v-icon>
        </v-btn>
        <v-btn color="primary" icon @click="suffle">
          <v-icon>{{ suffle1 ? 'mdi-shuffle' : 'mdi-shuffle-disabled' }}</v-icon>
        </v-btn>
      </v-card-actions>
 
    </v-card>
  </div>
</template>


<script>
export default {
  name: 'songs',
  components: {
  },

  data: () => ({
    value: 30,
    play1: false,
    repeat1: false,
    suffle1: false,
    liked1: false,
  }),
  methods: {
    play() {
      this.play1 = !this.play1
    },
    repeat() {
      this.repeat1 = !this.repeat1
    },
    suffle() {
      this.suffle1 = !this.suffle1
    },
    liked() {
      this.liked1 = !this.liked1
    }
  }
};
</script>

<style scoped>
.timer {
font-size: 15px;
padding: 5px 10px;
}
.slide {
margin: 10px auto;
height: 35px;
padding: auto 5px;
}
</style>