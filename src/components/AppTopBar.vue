<template>
  <div>
    <v-app-bar class="green lighten-1 d-flex">
      <v-img
        :src="require('../assets/plantgo-icon.svg')"
        height="50px"
        contain
      ></v-img>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "top-bar"
};
</script>
