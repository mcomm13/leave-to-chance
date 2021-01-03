<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">Leave To Chance</div>
      <v-spacer></v-spacer>
      <v-btn
        href="https://github.com/mcomm13/leave-to-chance"
        target="_blank"
        text
      >
        <span class="mr-2">View on GitHub</span>
        <v-icon>mdi-github-circle</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <LeaveToChance />
    </v-content>

    <v-footer>
      <div>&copy; 2020 Michael Commendatore</div>
    </v-footer>
  </v-app>
</template>

<script>
import LeaveToChance from './components/LeaveToChance';

export default {
  name: 'App',

  components: {
    LeaveToChance,
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss">
.v-application--wrap {
  min-height: 100vh;
}
.row {
  margin: auto;
}
</style>
