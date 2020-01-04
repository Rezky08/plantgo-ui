<template>
  <v-app>
    <top-bar v-if="topBarHide"></top-bar>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import TopBar from "./components/AppTopBar.vue";

export default {
  name: "App",
  components: { TopBar },
  created() {
    this.hidingTopBar();
  },
  beforeUpdate() {
    this.hidingTopBar();
  },
  methods: {
    hidingTopBar: function() {
      return (this.topBarHide = this.hideRoute.includes(this.$route.path)
        ? false
        : true);
    }
  },
  data: () => ({
    topBarHide: true,
    hideRoute: ["/login", "/register"]
  })
};
</script>
