<template>
  <div :style="{'background-image': 'url(' + background + ')'}" style="background-repeat: repeat">
    <v-container>
      <v-row>
        <v-col cols="12" align="center">
          <nuxt-link to="/">
            <v-img :src="mainLogo" width="642" alt="The Fortuna logo" />
          </nuxt-link>
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
              <nuxt-link :to="button.link">
                <v-img :src="button.source" :alt="button.name" width="92" />
              </nuxt-link>
            </v-col>
          </v-row>
        </v-col>
        <v-spacer />
      </v-row>
    </v-container>
  </div>
</template>

<script>
import backgroundImage from 'static/th1.jpg'
import banner from 'static/Fortuna.jpg'
import schoolButton from 'static/chkola2.gif'
import clubButton from 'static/klub2.gif'
import dosugButton from 'static/Dosug2.gif'
import avtorButton from 'static/avtor2.gif'

export default {
  name: 'FortunaHeader',
  data () {
    return {
      background: backgroundImage,
      mainLogo: banner,
      buttons: [
        { source: schoolButton, name: 'Link to school page', link: { name: 'school' } },
        { source: clubButton, name: 'Link to Club page', link: { name: 'club' } },
        { source: dosugButton, name: 'Link to Entertainment page', link: { name: 'еntertainment' } },
        { source: avtorButton, name: 'Link to author', link: { name: 'about' } }
      ]
    }
  }
}
</script>
