<template>
  <v-app id="leave-to-chance">
    <!-- <v-content> -->
    <v-container>
      <h1>Use this app to help you leave a decision up to chance</h1>
      <v-row align="center" justify="center">
        <v-col cols="12" sm="8" md="6">
          <v-card class="elevation-12">
            <v-card-text>
              <v-row>
                <v-col>
                  <strong>How many options are you choosing from?</strong>
                </v-col>
                <v-col>
                  <v-text-field v-model="numOfOptions" label="Number of options" />
                </v-col>
              </v-row>
            </v-card-text>
            <v-row v-if="randomPick">
              <v-col class="result">
                <div class="result__header">Your randomly selected option is:</div>
                <div class="result__value">{{randomPick}}</div>
              </v-col>
            </v-row>
            <v-card-actions>
              <v-row align="center" justify="center">
                <v-btn v-on:click="makeRandomPick" color="primary">Make Random Pick</v-btn>
              </v-row>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <!-- </v-content> -->
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      randomPick: 0,
      numOfOptions: 2
    };
  },
  methods: {
    makeRandomPick: function() {
      this.numOfOptions = parseInt(this.numOfOptions);
      this.randomPick = Math.floor(Math.random() * this.numOfOptions) + 1;
    }
  }
};
</script>

<style lang="scss">
h1 {
  text-align: center;
  font-size: 24px;
  margin-top: 12px;
  margin-bottom: 12px;
}
.result {
  text-align: center;
  &__header {
    font-size: 24px;
  }
  &__value {
    font-size: 32px;
    font-weight: bold;
  }
}
</style>