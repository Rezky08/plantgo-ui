<template>
  <v-container class="fill-height" fluid>
    <v-row align="center" justify="center" class="mx-auto">
      <v-col>
        <!-- plantGo Icon Dark -->
        <v-row align="center" justify="center">
          <v-col cols="6" sm="8" md="3">
            <router-link to="/">
              <v-img :src="require('../assets/plantgo-iconDark.svg')" contain></v-img>
            </router-link>
          </v-col>
        </v-row>
        <!--  -->

        <!-- login Field -->
        <v-row align="center" justify="center">
          <v-col cols="12" md="8">
            <v-text-field
              solo
              label="username"
              v-model="usernameField"
              rounded
              prepend-inner-icon="fa-user"
            ></v-text-field>
            <v-text-field
              :type="show?'text':'password'"
              solo
              label="password"
              v-model="passwordField"
              rounded
              prepend-inner-icon="fa-key"
              :append-icon="show?'fa-eye-slash':'fa-eye'"
              @click:append="show = !show"
            ></v-text-field>
            <v-btn class="my-2" block color="primary" rounded>Login</v-btn>
            <v-btn class="my-2" block rounded text color="primary" to="/register">Create account?</v-btn>
          </v-col>
        </v-row>
        <!--  -->

        <v-divider class="my-5"></v-divider>

        <!-- login with Social Media -->
        <v-row align="center" justify="center">
          <v-col cols="12" md="8">
            <div class="my-2">
              <v-btn color="white" rounded block>
                <v-icon left>fab fa-google</v-icon>Login with Google
              </v-btn>
            </div>

            <div class="my-2">
              <v-btn color="white" rounded block>
                <v-icon left>fab fa-facebook</v-icon>Login with Facebook
              </v-btn>
            </div>

            <div class="my-2">
              <v-btn color="white" rounded block>
                <v-icon left>fab fa-twitter</v-icon>Login with Twitter
              </v-btn>
            </div>
          </v-col>
        </v-row>
        <!--  -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    usernameField: "",
    passwordField: "",
    show: false
  })
};
</script>