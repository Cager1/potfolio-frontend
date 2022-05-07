<template>
<!--    <v-card>-->
<!--      <div class="container-iframe" data-widget="">-->
<!--        <iframe src="http://pzi022022.studenti.sumit.sum.ba" class="responsive-iframe"></iframe>-->
<!--      </div>-->
<!--    </v-card>-->

  <v-row>
    <v-col cols="12" md="10" offset-md="1">
      <v-hover class="d-none d-md-block" :value="focused">
        <template>
          <v-card
            @mouseover="focused = true"
            @mouseleave="focused = false"
          >
            <v-img
              class="d-md-block d-none"
              @focus="focused = true"
              @focusout="focused = false"
              tabindex="1"
              :src="require('~/assets/project_files/projekt1.png')">
            </v-img>
            <v-img
              class="d-md-none"
              tabindex="1"
              contain
              :src="require('~/assets/project_files/projekt1-mobile.png')">
            </v-img>

            <v-expand-transition>
              <v-card
                v-if="focused"
                class="transition-ease-in-out  v-card--reveal"
                style="height: 100%;"
                elevation="0"

              >
                <v-row justify="center" align="center">
                  <v-col cols="6">
                    <v-card-title>Ika Instalacije</v-card-title>
                  </v-col>
                  <v-col cols="6" class="d-md-flex d-none text-right">
                    <a tabindex="1"
                       @focusin="focused = true"
                       @focuout="focused = false"
                       target="_blank" class="zoom"
                       href="https://github.com/Cager1/pzi-api">
                      <v-icon class="zoom" large>mdi-github</v-icon>
                    </a>
                    <a tabindex="1"
                       @focusin="focused = true"
                       @focusout="focused = false"
                       target="_blank" class="zoom"
                       href="http://pzi022022.studenti.sumit.sum.ba">
                      <v-icon class="zoom" large>mdi-link</v-icon>
                    </a>
                  </v-col>
                  <v-col cols="6" class="d-md-none text-right">
                    <a tabindex="1"
                       target="_blank" class="zoom"
                       href="https://github.com/Cager1/pzi-api">
                      <v-icon class="zoom" large>mdi-github</v-icon>
                    </a>
                    <a tabindex="1"
                       target="_blank" class="zoom"
                       href="http://pzi022022.studenti.sumit.sum.ba">
                      <v-icon class="zoom" large>mdi-link</v-icon>
                    </a>
                  </v-col>
                </v-row>

                <v-divider></v-divider>
                <v-row>
                  <v-col cols="12" md="6">
                    <v-card elevation="0">
                      <v-card-title>Description</v-card-title>
                      <v-card-text>
                        Last project I made in collage. It served as practice and now as a showcase for my
                        knowledge in backend and frontend web technlogies.
                      </v-card-text>
                      <v-card-text>
                        Idea of this project is for it to be used by service technicians in various fields
                        where they offer their services while users should be able to see their availability
                        and appoint them.
                      </v-card-text>

                      <v-card-text>
                        You should use following credentials in order to acces admin panel to check out all of
                        implemented features:
                        <ul>
                          <li>
                            E-mail: admin@admin.com
                          </li>
                          <li>
                            Password: admin123
                          </li>
                        </ul>
                      </v-card-text>

                    </v-card>
                  </v-col>
                  <v-col cols="12" md="6">
                    <v-card elevation="0">
                      <v-card-title>Used Technologies</v-card-title>
                      <v-card-text>
                        <ul>
                         <li>
                           Vue
                           <ul>
                             <li>Vuetify</li>
                             <li>VeeValidate</li>
                             <li>Nuxt</li>
                           </ul>
                         </li>
                          <li>Laravel</li>

                        </ul>
                      </v-card-text>

                    </v-card>

                    <v-card elevation="0">
                      <v-card-title>Features</v-card-title>
                      <v-card-text>
                        Authentication and Authorization (Bearer token) <br>
                        Admin Control Panel <br>
                        CRUD model for viewing deleting and updating jobs

                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </v-card>
            </v-expand-transition>
          </v-card>
        </template>
      </v-hover>
      <v-hover class="d-md-none" :value="focused">
        <template>
          <v-card
            @mouseover="focused = true"
            @mouseleave="focused = false"
            elevation="0"
            width="80%"
            class="mx-auto"
          >
            <v-img
              class="d-md-none"
              tabindex="1"
              contain
              :src="require('~/assets/project_files/projekt1-mobile.png')">
            </v-img>

            <v-expand-transition>
              <v-card
                v-if="focused"
                class="transition-ease-in-out  v-card--reveal"
                style="height: 100%;"
                elevation="12"

              >
                <v-row justify="center" align="center">
                  <v-col cols="7">
                    <v-card-title>Ika Instalacije</v-card-title>
                  </v-col>
                  <v-col cols="5" class="d-md-none text-right">
                    <a tabindex="1"
                       target="_blank" class="zoom"
                       href="https://github.com/Cager1/pzi-api">
                      <v-icon class="zoom" large>mdi-github</v-icon>
                    </a>
                    <a tabindex="1"
                       target="_blank" class="zoom"
                       href="http://pzi022022.studenti.sumit.sum.ba">
                      <v-icon class="zoom" large>mdi-link</v-icon>
                    </a>
                  </v-col>
                </v-row>

                <v-divider></v-divider>
                <v-row>
                  <v-col cols="12" md="6">
                    <v-card elevation="0">
                      <v-card-title>Description</v-card-title>
                      <v-card-text>
                        Last project I made in collage. It served as practice and now as a showcase for my
                        knowledge in backend and frontend web technlogies.
                      </v-card-text>
                      <v-card-text>
                        Idea of this project is for it to be used by service technicians in various fields
                        where they offer their services while users should be able to see their availability
                        and appoint them.
                      </v-card-text>

                      <v-card-text>
                        You should use following credentials in order to acces admin panel to check out all of
                        implemented features:
                        <ul>
                          <li>
                            E-mail: admin@admin.com
                          </li>
                          <li>
                            Password: admin123
                          </li>
                        </ul>
                      </v-card-text>

                    </v-card>
                  </v-col>
                  <v-col cols="12" md="6">
                    <v-card elevation="0">
                      <v-card-title>Used Technologies</v-card-title>
                      <v-card-text>
                        <ul>
                          <li>
                            Vue
                            <ul>
                              <li>Vuetify</li>
                              <li>VeeValidate</li>
                              <li>Nuxt</li>
                            </ul>
                          </li>
                          <li>Laravel</li>

                        </ul>
                      </v-card-text>

                    </v-card>

                    <v-card elevation="0">
                      <v-card-title>Features</v-card-title>
                      <v-card-text>
                        Authentication and Authorization (Bearer token) <br>
                        Admin Control Panel <br>
                        CRUD model for viewing deleting and updating jobs

                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </v-card>
            </v-expand-transition>
          </v-card>
        </template>
      </v-hover>
    </v-col>
  </v-row>



</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      focused: false,
    }
  },

  methods: {

  }
}
</script>

<style scoped>

.zoom {
  transition: transform .5s;
  text-decoration: none;
  transform: scale(1);
}

.zoom:hover {
  transition: transform .5s;
  transform: scale(1.15);
  z-index: 5;
}

.v-card--reveal {
  bottom: 0;
  position: absolute;
  width: 100%;
  padding: 10px;
  color: black;
  border-bottom-left-radius: unset !important;
  border-bottom-right-radius: unset !important;

  font-family: 'Oswald', sans-serif;
  font-weight: 200;
  overflow-y: scroll;
}

.v-card--reveal::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.v-card--reveal {
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
}

.container-iframe {
  position: relative;
  width: 100%;
  overflow: hidden;
  padding-top: 56.25%; /* 16:9 Aspect Ratio */
}
.responsive-iframe {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  border: none;
}
</style>
