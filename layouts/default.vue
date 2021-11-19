<template>
  <v-app>
    <div :style="{'background-image': 'url(' + background + ')'}" style="background-repeat: repeat">
      <v-container>
        <v-row>
          <v-col cols="12" align="center">
            <v-img :src="mainLogo" width="642" alt="The Fortuna logo" />
          </v-col>
        </v-row>
        <v-row>
          <v-spacer />
          <v-col
            cols="12"
            sm="10"
            md="8"
            lg="6"
            xl="4"
            align="center"
          >
            <v-row>
              <v-col v-for="button of buttons" :key="button.name">
                <v-img :src="button.source" :alt="button.name" width="92" />
              </v-col>
            </v-row>
          </v-col>
          <v-spacer />
        </v-row>
      </v-container>
    </div>
    <div>
      <nuxt />
    </div>
  </v-app>
</template>

<script>
import banner from '@/static/Fortuna.jpg'
import avtorButton from '@/static/avtor2.gif'
import schoolButton from '@/static/chkola2.gif'
import dosugButton from '@/static/Dosug2.gif'
import clubButton from '@/static/klub2.gif'
import backgroundImage from '@/static/th1.jpg'

export default {
  data () {
    return {
      background: backgroundImage,
      mainLogo: banner,
      buttons: [
        { source: schoolButton, name: 'Link to school page', link: '2' },
        { source: clubButton, name: 'Link to Club page', link: '2' },
        { source: dosugButton, name: 'Link to Entertainment page', link: '2' },
        { source: avtorButton, name: 'Link to author', link: '1' }
      ]
    }
  }
}
</script>

<style>
.main-body {
  background-color: aqua;
}
</style>
