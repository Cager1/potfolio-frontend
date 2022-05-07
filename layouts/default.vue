<template>
  <v-app>
    <v-app-bar height="70px" app elevation="0" class="d-md-none">
      <v-btn text height="50px" active-class="link-active" class="text-center" width="50%" nuxt :to="links[n-1].to" v-for="n in 2" :key="n">
        <v-avatar size="40">
          <v-img class="link-image" :src="require('~/assets/mobile_icons/' + mobile_icons[n-1] + '.png')">
          </v-img>
        </v-avatar>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer class="d-none d-md-flex"
                         mobile-breakpoint="960"
                         id="drawer" app width="30%"
                         floating
                         fixed
    >
      <v-list style="padding-top: 100px">
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title id="myName">

              FILIP CRNOGORAC
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-list style="padding-top: 100px">
          <nuxt-link v-for="n in links.length - 1" :key="n"
                     :to="links[n-1].to"
                     style="text-decoration: none"
                     exact-active-class="nav_link"
                     tabindex="1"
          >
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title class="navItems">
                  {{ links[n-1].name }}
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </nuxt-link>

      </v-list>

      <v-bottom-navigation app style="box-shadow: none">
        <v-tooltip
          top
          allow-overflow
          nudge-right="10px"
        >
          <template v-slot:activator="{ on, attrs }">
            <a href="tel:+387 63 233 565">
              <button
                v-bind="attrs"
                v-on="on"
                class="contact-buttons">
                <v-avatar size="50">
                  <v-img :src="require('~/assets/contact_icons/phone-icon.png')">
                  </v-img>
                </v-avatar>
              </button>
            </a>

          </template>
          <div v-html="contact_links[0].content"></div>

        </v-tooltip>
        <v-tooltip v-for="n in contact_icons.length - 1" :key="n"
                   top
                   allow-overflow
                   nudge-right="10px"
        >
          <template v-slot:activator="{ on, attrs }">
            <a :href="contact_links[n].data" target="_blank">
              <button
                v-bind="attrs"
                v-on="on"
                class="contact-buttons">
                <v-avatar size="50">
                  <v-img :src="require('~/assets/contact_icons/' +  contact_icons[n].name + '.png')">
                  </v-img>
                </v-avatar>
              </button>
            </a>

          </template>
          <div v-html="contact_links[n].content"></div>

        </v-tooltip>

      </v-bottom-navigation>

    </v-navigation-drawer>

    <v-main>
      <v-container style="height: 100%">
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer class="d-md-none" app>
      <v-bottom-navigation app style="box-shadow: none">
        <v-menu v-for="n in contact_icons.length" :key="n"
                offset-overflow
                offset-y
                open-on-hover
                tile
                style="margin-top: 200px;"
        >
          <template v-slot:activator="{ on, attrs }">
            <a :href="contact_links[n-1].data" target="_blank">
              <button
                v-bind="attrs"
                v-on="on"
                class="contact-buttons">
                <v-avatar size="50">
                  <v-img :src="require('~/assets/contact_icons/' +  contact_icons[n-1].name + '.png')">
                  </v-img>
                </v-avatar>
              </button>
            </a>

          </template>
          <div v-html="contact_links[n-1].content"></div>

        </v-menu>

      </v-bottom-navigation>
    </v-footer>


  </v-app>


</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      activePage: 0,
      contact_icons: [
        {name: 'phone-icon'},
        {name: 'mail-icon'},
        {name: 'linkedin-icon'},
        {name: 'github-icon'}
      ],

      contact_links: [
        {
          data: 'tel: +387 63 233 565',
          content: '<div>+387 63 233 565</div>',
        },{
          data: 'mailto:filip.crnogorac@outlook.com',
          content: '<div>filip.crnogorac@outlook.com</div>',
        }, {
          data: 'https://www.linkedin.com/in/filip-crnogorac/',
          content: '<div>Visit my Linked In page',
        }, {
          data: 'https://github.com/Cager1',
          content: '<div>Visit my GitHub page',
        }
    ],


      tooltipContent: ['+387 63 233 565', 'filip.crnogorac@outlook.com', 'www.linkedin.com/in/filip-crnogorac', 'https://github.com/Cager1'],

      mobile_icons: ['projects_mobile_icon','experience_mobile_icon','contact_mobile_icon'],
      links: [
        {to: '/', name: 'Projects'},
        {to: '/experience-awards', name: 'Experience and Awards'},
        {to: '/contact', name: 'Contact'},
      ]
    }
  },
  methods: {
  }
}
</script>

<style scoped>

  #myName {
    font-family: 'Oswald', sans-serif;
    font-weight: 400;
    font-size: 40px;
  }

  #drawer {
    display: flex;
    align-items: center;
  }

  .nav-bar-active-class {

  }

  .navItems {
    margin-top: 10px;
    font-family: 'Oswald', sans-serif;
    font-size: 25px;
    font-weight: 200;


    position: relative;
  }

  .nav_link .navItems:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(1);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #0087ca;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }


  .navItems:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #0087ca;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }

  .navItems:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }

  .contact-buttons {
    opacity: 0.7;
    margin-left: 20px;
  }

  .contact-buttons:hover {
    opacity: 1.0;
  }
</style>
