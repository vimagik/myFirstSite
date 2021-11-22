<template>
  <div :style="{'background-image': 'url(' + bgEnterImage + ')'}" class="FtMainBody">
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
import bgEnterImage from '@/static/restBG.jpeg'

export default {
  name: 'Entertainment',
  data () {
    return {
      bgEnterImage,
      buttons:
        [
          { id: 0, name: 'Развлекаловка', page: '/entertainment' },
          { id: 1, name: 'Анекдоты', page: '/entertainment/anecdotes' },
          { id: 2, name: 'Кроссворды', page: '/entertainment/crosswords' }
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
