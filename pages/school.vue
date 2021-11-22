<template>
  <div :style="{'background-image': 'url(' + bgSchool + ')'}" class="FtMainBody">
    <v-container>
      <v-row>
        <v-col cols="12" sm="5" md="3">
          <div class="mt-5">
            <v-btn
              v-for="button of buttons"
              :key="button.id"
              text
              block
              color="primary"
              :to="button.page"
              nuxt
              exact
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
import bgSchool from '@/static/schoolBG.jpeg'

export default {
  name: 'School',
  data () {
    return {
      bgSchool,
      buttons: [
        { id: 0, name: 'О школе', page: '/school/' },
        { id: 1, name: 'Школа искусств', page: '/school/art' },
        { id: 2, name: 'Спортивная школа', page: '/school/sport' },
        { id: 3, name: 'Оздоровительный центр', page: '/school/wellness-center' },
        { id: 4, name: 'Производственный комплекс', page: '/school/production-complex' }
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
