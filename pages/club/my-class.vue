<template>
  <v-container>
    <v-col>
      <v-row justify="center">
        <div class="text-h4" style="text-align: center; color: #FFFF00">
          <p>З н а к о м ь т е с ь</p>
          <p>мой класс !!!</p>
        </div>
      </v-row>
      <v-row>
        <v-img :src="classPhoto">
          <nuxt-link tag="a" to="/about">
            <a style="position:absolute; top: 33%; right: 90%; height:5%; width: 5%;" />
          </nuxt-link>
        </v-img>
      </v-row>
    </v-col>
  </v-container>
</template>

<script>
import classPhoto from '@/static/klass.jpg'

export default {
  name: 'MyClass',
  data () {
    return {
      classPhoto
    }
  }
}
</script>

<style scoped>

</style>
