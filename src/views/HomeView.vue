<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="19" md="19">
            <v-card class="evaluation-12">
              <v-window v-model="step">              
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1 class="text-center display-2 teal--text text--accent-3">Sign in</h1>
                        <div class="text-center" mt-4>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mlt-4">Assurer votre Email pour l'enregistrement</h4>
                        <v-form>
                          <v-text-field
                                    label="Email"
                                    name="Email"
                                    prepend-icon="email"
                                    type="text"
                                    color="teal accent-3"
                          />
                          <v-text-field
                                    id="password"
                                    label="Password"
                                    name="Password"
                                    prepend-icon="lock"
                                    type="password"
                                    color="teal accent-3"
                          />
                        </v-form>
                        <h3 class="text-center mt-3">Mot de passe oublié ?</h3>
                      </v-card-text>
                      <div class="text-center" mt-3>
                        <v-btn rounded color="teal accent-3" dark>SIGN IN</v-btn>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Coucou!!!!</h1>
                        <h5 class="text-center">Entrer detail personnel</h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined="" dark @click="step++">SIGN UP</v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>              
                <v-window-item :value="2">
                  <v-row class="fill-height">
                      <v-col cols="12" md="4" class="teal accent">
                        <v-card-text class="white--text mt-12">
                          <h1 class="text-center display-1">Bienvenu!!</h1>
                          <h5 class="text-center">To keep connected with us</h5>
                        </v-card-text>
                        <div class="text-center">
                          <v-btn rounded outlined dark @click="step--">SIGN IN</v-btn>
                        </div>
                      </v-col>
                      <v-col cols="12" md="8">
                        <v-card-text class="mt-12">
                          <h1 class="text-center display-2 teal--text text--accent-3">Creer un compte</h1>
                          <div class="text-center mt-4">
                            <v-btn class="mx-2" fab color="Black" outlined>
                              <v-icon>fab fa-facebook-f</v-icon>
                            </v-btn>
                            <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                            </v-btn>
                            <v-btn class="mx-2" fab color="black" outlined>
                              <v-icon>fab fa-linkedin-in</v-icon>
                            </v-btn>
                          </div>
                          <h4 class="text-center mt-4">Assuer votre Email</h4>
                          <v-form>
                            <v-text-field
                                      label="Full name"
                                      name="Name"
                                      prepend-icon="person"
                                      type="text"
                                      color="teal accent-3"
                            />
                            <v-text-field
                                      label="Email"
                                      name="Email"
                                      prepend-icon="email"
                                      type="text"
                                      color="teal accent-3"
                            />
                            <v-text-field
                                      id="password"
                                      label="Password"
                                      name="Password"
                                      prepend-icon="lock"
                                      type="password"
                                      color="teal accent-3"
                            />
                          </v-form>
                        </v-card-text>
                        <div class="text-center mt-n5">
                          <v-btn rounded color="teal accent-3">SIGN UP</v-btn>
                        </div>
                      </v-col>
                  </v-row>
                </v-window-item>             
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
  export default{
    data: () => ({
      step: 1
    }),
    props: {
      source : String
    }
  };
</script>
