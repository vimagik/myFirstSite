<template>
  <v-container>
    <v-col>
      <v-row justify="center">
        <v-img :src="entNBanner" max-width="507">
          <nuxt-link tag="a" to="/entertainment/anecdotes">
            <a style="position:absolute; top: 33%; right: 70%; height:30%; width: 30%;" />
          </nuxt-link>
          <nuxt-link tag="a" to="/entertainment/crosswords">
            <a style="position:absolute; top: 33%; right: 5%; height:30%; width: 30%;" />
          </nuxt-link>
        </v-img>
      </v-row>
      <v-row>
        <div class="text-body-1 mt-5" style="color: #800080">
          <p>Вербальные забавы.</p>
          <p>
            Вербальные игры, пожалуй, один из самых любимых видов развлечения. Они не требуют сложных атрибутов,
            громоздкой амуниции. Их можно совместить, например, с чисткой картошки или починкой табурета. Зато
            польза от них колоссальная! И удовольствие огромное!
          </p>
          <p>Было время, когда игры со словом являлись непременным атрибутом домашнего досуга.</p>
          <p>Ну а без анекдотов наша жизнь была бы слишком сера!!!</p>
        </div>
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
import entNBanner from '@/static/UMOR.gif'

export default {
  name: 'Entertainment',
  data () {
    return {
      entNBanner
    }
  }
}
</script>

<style scoped>

</style>
