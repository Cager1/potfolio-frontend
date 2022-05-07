<template>
  <v-container id="exp-awards">

    <div id="tip" class="d-none text-center d-md-block">
      <v-img  height="32px" contain :src="require('~/assets/lightbulb.png')"></v-img>
      <p style="display: inline">Click on items to expand them</p>
    </div>
    <div id="tip1" class="d-md-none text-center">
      <v-img height="32px" contain :src="require('~/assets/lightbulb.png')"></v-img>
      <p style="display: inline">Click on items to expand them</p>
    </div>

    <div class="d-none d-md-block">
      <exp-award title="Awards" :image="images.awards" style="background: transparent">
        <button tabindex="3">
          <v-row class="mx-md-10 zoom1"
                 align="center">

            <v-col cols="auto" class="mx-auto mx-md-0 text-center">
              <v-avatar rounded size="64">
                <v-img contain :src="require('~/assets/exp_awards_icons/'+ images.awards[1] + '.png')">
                </v-img>
              </v-avatar>
            </v-col>
            <v-col cols="auto">
              <p> <strong style="font-size: 20px">{{ title[0] }}</strong> - Sveučilište u Mostaru - University of Mostar <br>
                <span class="mx-md-5">Hackathon Winner for competition in Leo Rover Smart Kampus</span></p>
            </v-col>

          </v-row>
        </button>

        <template v-slot:Content>
          <v-row align="center" justify="center">
            <a tabindex="3" class="zoom" target="_blank" v-for="n in 4" :key="n" :href="links[n-1]">
              <v-img style="display: inline-block" width="300" :src="require('~/assets/award-articles/article' + n + '.png')">
              </v-img>
              <div class="overlay"><v-img :src="require('~/assets/award-articles/website_logos/' + website[n-1] + '.png')">
              </v-img></div>
            </a>
          </v-row>
          <v-row class="mt-10 mb-10" align="center" justify="center">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/wJ531QFMNIk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </v-row>
        </template>
      </exp-award>
      <exp-award title="Experience" :image="images.experience" style="background: transparent">
        <button tabindex="3">
            <v-row class="mx-md-10 zoom1"
                   align="center">
              <v-col cols="auto" class="text-center">
                <v-avatar rounded size="64">
                  <v-img contain :src="require('~/assets/exp_awards_icons/'+ images.experience[1] + '.png')">
                  </v-img>
                </v-avatar>
              </v-col>
              <v-col class="text-left" cols="auto">
                <p> <strong style="font-size: 20px">{{ title[1] }} </strong> <br>
                  <span class="text-left mx-md-5">Upwork</span>
                </p>
              </v-col>
            </v-row>
        </button>

        <template v-slot:Content>
          <v-row style="padding-left: 10px; margin-bottom: 20px">
            <a tabindex="3" target="_blank" href="https://www.upwork.com/freelancers/~01cf52923eef60a719?viewMode=1"><h2>My Upwork Page</h2></a>
          </v-row>
          <v-row>
            <v-img class="d-none d-md-block" contain :src="require('~/assets/experience_photos/my_upwork_page.png')"></v-img>
            <v-img class="d-none d-sm-block d-md-none" contain :src="require('~/assets/experience_photos/ipad_my_upwork_page.png')"></v-img>
            <v-img class="d-block d-sm-none" contain :src="require('~/assets/experience_photos/phone_my_upwork_page.png')"></v-img>
          </v-row>
        </template>
      </exp-award>
    </div>

    <div class="d-md-none">
      <exp-award title="Awards" :image="images.awards" style="background: transparent">
        <v-row class="mx-md-10">
          <v-col cols="2" class="text-center">
            <v-avatar rounded size="48">
              <v-img contain :src="require('~/assets/exp_awards_icons/'+ images.awards[1] + '.png')">
              </v-img>
            </v-avatar>
          </v-col>
          <v-col cols="10">
            <p> <strong style="font-size: 20px">{{ title[0] }}</strong> - Sveučilište u Mostaru - University of Mostar <br>
              <span class="mx-md-5">Hackathon Winner for competition in Leo Rover Smart Kampus</span></p>
          </v-col>
        </v-row>
        <template v-slot:Content>
          <v-row align="center" justify="center">
            <a class="zoom" target="_blank" v-for="n in 4" :key="n" :href="links[n]">
              <v-img style="display: inline-block" width="300" :src="require('~/assets/award-articles/article' + n + '.png')">
              </v-img>
              <div class="overlay"><v-img :src="require('~/assets/award-articles/website_logos/' + website[n-1] + '.png')">
              </v-img></div>
            </a>
          </v-row>

          <v-row class="mt-10 mb-10" align="center" justify="center">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/wJ531QFMNIk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </v-row>
        </template>
      </exp-award>
      <exp-award title="Experience" :image="images.experience" style="background: transparent">
        <v-row class="mx-md-10">
          <v-col cols="2" class="text-center">
            <v-avatar rounded size="48">
              <v-img contain :src="require('~/assets/exp_awards_icons/'+ images.experience[1] + '.png')">
              </v-img>
            </v-avatar>
          </v-col>
          <v-col cols="10">
            <p> <strong style="font-size: 20px">{{ title[1] }} </strong> <br>
              <span class="mx-md-5">Upwork</span>
            </p>
          </v-col>
        </v-row>
        <template v-slot:Content>
          <v-row style="padding-left: 10px; margin-bottom: 20px">
            <a target="_blank" href="https://www.upwork.com/freelancers/~01cf52923eef60a719?viewMode=1"><h2>My Upwork Page</h2></a>
          </v-row>
          <v-row>
            <v-img class="d-none d-md-block" contain :src="require('~/assets/experience_photos/my_upwork_page.png')"></v-img>
            <v-img class="d-none d-sm-block d-md-none" contain :src="require('~/assets/experience_photos/ipad_my_upwork_page.png')"></v-img>
            <v-img class="d-block d-sm-none" contain :src="require('~/assets/experience_photos/phone_my_upwork_page.png')"></v-img>
          </v-row>
        </template>
      </exp-award>
    </div>


  </v-container>
</template>

<script>
export default {
  name: "experience-awards",
  data () {
    return {
      title: ['Hackathon Winner', 'Freelance Graphic Designer'],
      images: {
        awards: ['award_icon', 'sum-logo'],
        experience: ['experience_icon', 'upwork-logo']
      },

      website: ['novasloboda', 'ericsson', 'tockanai', 'sum'],

      links: [
        'https://novasloboda.ba/2021/12/09/robot-leo-rover-novi-dio-projekta-smart-campusa/',
        'https://www.ericsson.hr/en/-/20211209-smart-campus-project',
        'https://tockanai.hr/tehnologija/na-sveucilistu-u-mostaru-predstavljen-robot-leo-rover-53845/',
        'https://www.sum.ba/objave/novosti/robot-leo-rover-novi-dio-projekta-smart-campusa',
      ]
    }
  }
}
</script>

<style scoped>

#exp-awards {
  padding-top: 100px;
}

button {
  background: transparent;
  box-shadow: 0 0 0 transparent;
  border: 0 solid transparent;
  text-shadow: 0 0 0 transparent;
}

button:hover {
  display: block;
  width: 100%;
  padding: 0;
  margin: 0;
  background: transparent;
  box-shadow: 0 0 0 transparent;
  border: 0 solid transparent;
  text-shadow: 0 0 0 transparent;
}

button:active {
  outline: none;
  border: none;
}


/*#exp-awards {*/
/*  background-image: url("~/assets/background-computer.png");*/
/*  background-position: bottom;*/
/*  background-repeat: no-repeat;*/
/*  background-size: contain;*/
/*}*/

.zoom {
  transition: transform .5s;

  transform: scale(1);
}

.zoom:hover {
  transition: transform .5s;
  transform: scale(1.15);
  z-index: 5;
}




#tip {

  position: absolute;
  top: 5%;
  right: 5%;

}

#tip1 {

  position: absolute;
  top: 5%;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;

}

.overlay {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgb(255, 255, 255);
  width: 100%;
  transition: .5s ease;
  opacity:0;
  color: white;
  font-size: 20px;
  padding: 20px;
  text-align: center;
}

/* When you mouse over the container, fade in the overlay title */
.zoom:hover .overlay {
  opacity: 1;
}
</style>
