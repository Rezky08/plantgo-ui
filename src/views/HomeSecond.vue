<template>
  <v-container>
    <v-row>
      <v-col v-bind:cols="searchBoxCol">
        <v-text-field
          name="searchBox"
          label="searchBox"
          placeholder="find what you want to buy or plant . . ."
          solo
          rounded
          prepend-inner-icon="fa-search"
        ></v-text-field>
      </v-col>
      <v-col v-bind:cols="promoCol">
        <v-btn class="white" :elevation="2" rounded>
          <v-icon left>fa-percentage</v-icon>promo
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>
<style scoped>
.v-text-field {
  font-size: 9pt;
}
.v-text-field .prepend-inner-icon {
  font-size: 2pt;
}
</style>

<script>
export default {
  data: () => ({
    searchBoxCol: 8,
    promoCol: 3
  })
};
</script>
