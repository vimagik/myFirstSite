<template>
  <div :style="{'background-image': 'url(' + backgroundImage + ')'}" class="FtMainBody">
    <v-container>
      <v-row>
        <v-spacer />
        <v-col align="center">
          <v-img :src="authorLogo" max-width="332" @mouseenter="changeToNew" @mouseleave="changeToOld" />
        </v-col>
        <v-spacer />
      </v-row>
      <v-row>
        <v-col align="center">
          <div class="text-body-1 ft-main-text">
            <p>Привет!</p>
            <p>Хотите побольше обо мне узнать? Ладно!</p>
            <p>Зовут меня Ржавин Георгий или просто Жора. Мне 15 лет. Родился 1 августа 1984 года.</p>
            <p>
              Учусь в школе N 18
              города Йошкар-Ола, в 10 &quot;А&quot; классе. My hobby is мой
              компьютер. Люблю вкусно поесть.
            </p>
            <p>Ну и все пожалуй.</p>
          </div>

          <v-img
            :src="backButton"
            max-width="113"
            class="ft-button"
            @click="$router.go(-1)"
          />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import backgroundImage from '@/static/dob.jpg'
import authorImage from '@/static/georgemr.jpg'
import backButton from '@/static/backButton.gif'
import authorImageNew from '@/static/georgemr_new.jpg'

export default {
  name: 'About',
  data () {
    return {
      backgroundImage,
      authorLogo: authorImage,
      backButton
    }
  },
  methods: {
    changeToNew () {
      this.authorLogo = authorImageNew
    },
    changeToOld () {
      this.authorLogo = authorImage
    }
  }
}
</script>

<style scoped>
.FtMainBody {
  background-repeat: repeat;
  height: 100%;
}

.ft-button {
  cursor: pointer;
}

.ft-main-text {
  color: blue;
}
</style>
