<template>

    <v-dialog v-model="dialog"
              width="700"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-row class="mx-md-10"
               align="center"
               v-bind="attrs"
               v-on="on">
          <v-col cols="auto">
            <v-avatar rounded size="64">
              <v-img contain :src="require('~/assets/exp_awards_icons/'+ image + '.png')">
              </v-img>
            </v-avatar>
          </v-col>
          <v-col cols="auto">
            <slot></slot>
          </v-col>
        </v-row>
      </template>
      <v-card style="padding: 20px">
        <v-avatar style="display: inline" size="64">
          <v-img contain :src="require('~/assets/exp_awards_icons/'+ image + '.png')">
          </v-img>
        </v-avatar>
      </v-card>
    </v-dialog>
</template>

<script>
export default {
  name: "awards",
  props: {
    image: String,
    title: String,
    links: Object,

  },

  data () {
    return {
      dialog: false,

    }
  },

  mounted() {
    console.log(this.title)
  },

  methods: {
    htmlToElement(html) {
      let template = document.createElement('template');
      html = html.trim(); // Never return a text node of whitespace as the result
      template.innerHTML = html;
      return template.content.firstChild;
    }
  }
}
</script>

<style scoped>

</style>
