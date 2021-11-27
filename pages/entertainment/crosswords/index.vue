<template>
  <v-container>
    <v-row>
      <v-col>
        <div class="text-h4" style="color: #FF00FF">
          Существует много типов вербальных игр !!! Вам представлена лишь малая доля !!!
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-spacer v-if="$vuetify.breakpoint.smAndUp" />
      <v-col cols="4">
        <div class="text-body-1 mt-5" style="text-align: center;">
          <ul>
            <nuxt-link to="/entertainment/crosswords/fun?tab=0">
              <li class="ft-large-text">
                Метаграммы
              </li>
            </nuxt-link>
            <nuxt-link to="/entertainment/crosswords/fun?tab=1">
              <li class="ft-large-text">
                Анаграммы
              </li>
            </nuxt-link>
            <nuxt-link to="/entertainment/crosswords/fun?tab=2">
              <li class="ft-large-text">
                Шарады
              </li>
            </nuxt-link>
            <nuxt-link to="/entertainment/crosswords/fun?tab=3">
              <li class="ft-large-text">
                Логогрифы
              </li>
            </nuxt-link>
          </ul>
        </div>
      </v-col>
      <v-spacer />
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Crosswords'
}
</script>

<style scoped>
.ft-large-text {
  font-size: x-large;
  margin-top: 10px;
}
</style>
