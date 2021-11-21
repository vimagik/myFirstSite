<template>
  <div :style="{'background-image': 'url(' + bgImage + ')'}" class="FtMainBody">
    <v-container>
      <v-row>
        <v-col cols="12" sm="5" md="3">
          <div class="mt-5">
            <v-btn
              v-for="button of buttons"
              :key="button.id"
              text
              block
              :to="button.page"
              nuxt
            >
              {{ button.name }}
            </v-btn>
          </div>
        </v-col>
        <v-col cols="12" sm="7" md="9">
          <nuxt-child />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import bgImage from '@/static/bgclub.jpeg'

export default {
  name: 'Club',
  data () {
    return {
      bgImage,
      buttons: [
        { id: 0, name: 'Как вступить в клуб', page: '/club/how-to-join' },
        { id: 1, name: 'Мой класс', page: '/club/my-class' },
        { id: 2, name: 'Друзья', page: '/club/friends' }
      ]
    }
  }
}
</script>

<style scoped>
.FtMainBody {
  background-repeat: repeat;
  height: 100%;
}
</style>
