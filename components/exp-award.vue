<template>
  <v-container style="margin-bottom: 75px">
    <v-row class="d-none d-md-flex" align="center">
      <v-col cols="auto">
        <v-avatar size="64" rounded>
          <v-img :src="require('~/assets/exp_awards_icons/'+ image[0] + '.png')">
          </v-img>
        </v-avatar>
      </v-col>
      <v-col cols="auto">
        <h2>{{ title }}</h2>
      </v-col>
      <v-col cols="12">
        <v-dialog v-model="dialog"
                  width="800"
        >
          <template v-slot:activator="{ on, attrs }">
            <div v-bind="attrs"
                 v-on="on"
            >
              <slot></slot>
            </div>
          </template>
          <v-card style="padding: 20px">
            <slot></slot>
            <slot name="Content">
            </slot>

          </v-card>
        </v-dialog>
      </v-col>
    </v-row>
    <v-row class="d-md-none" align="center">
      <v-col cols="auto">
        <v-avatar size="48" rounded>
          <v-img :src="require('~/assets/exp_awards_icons/'+ image[0] + '.png')">
          </v-img>
        </v-avatar>
      </v-col>
      <v-col cols="auto">
        <h2>{{ title }}</h2>
      </v-col>
      <v-col cols="12">
        <v-dialog v-model="dialog"
                  width="800"

        >
          <template v-slot:activator="{ on, attrs }">
            <div v-bind="attrs"
                 v-on="on">
              <slot></slot>
            </div>

          </template>
          <v-card style="padding: 20px">
            <slot></slot>
            <v-divider class="mt-3 mb-6"></v-divider>
            <slot name="Content">
            </slot>

          </v-card>
        </v-dialog>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "exp-award",
  props: {
    title: String,
    image: Array,
  },

  data () {
    return {
      dialog: false,
    }
  }
}
</script>

<style scoped>

h2 {
  font-family: 'Playfair Display', serif;
  font-size: 45px;
}

#enlarge {
  position: fixed;

}
</style>
