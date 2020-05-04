<template>
  <div>
    <v-app
      id="inspire"
      class="bg"
    >
      <v-content>
        <v-container
          fluid
          fill-height
        >
          <v-layout
            align-center
            justify-center
            class="login-form"
          >
            <v-flex
              xs12
              sm8
              md4
            >
              <v-card class="elevation-12">
                <v-toolbar
                  color="primary"
                  dark
                  flat
                >
                  <v-toolbar-title>Login form</v-toolbar-title>
                  <v-spacer></v-spacer>
                  <v-tooltip bottom>
                    <template v-slot:activator="{ on }">
                      <v-btn
                        :href="source"
                        icon
                        large
                        target="_blank"
                        v-on="on"
                      >
                        <v-icon>mdi-code-tags</v-icon>
                      </v-btn>
                    </template>
                    <span>Source</span>
                  </v-tooltip>
                  <v-tooltip right>

                  </v-tooltip>
                </v-toolbar>
                <v-card-text>
                  <v-form>
                    <v-text-field
                      label="Login"
                      name="login"
                      type="text"
                    ></v-text-field>

                    <v-text-field
                      id="password"
                      label="Password"
                      name="password"
                      type="password"
                    ></v-text-field>
                  </v-form>
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <router-link to="/">
                    <v-btn color="primary">Login</v-btn>
                  </router-link>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-content>
    </v-app>
    <div class="mengban"></div>
  </div>
</template>

<script>
export default {
  name: "Login",
  data: () => ({
    drawer: null
  })
};
</script>

<style scoped lang="scss">
.bg {
  background: url("../assets/img/bg.jpg");
}
.mengban {
  position: absolute;
  background: linear-gradient(to right, #ecdfb2 34%, #7d7ce0 100%);
  opacity: 0.7;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.login-form {
  z-index: 44;
}
</style>
