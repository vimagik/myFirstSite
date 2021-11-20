<template>
  <div :style="{'background-image': 'url(' + mainBgImage + ')'}" class="FtMainBody">
    <v-container>
      <v-row>
        <v-col>
          <div class="text--primary">
            <p class="ft-main-text">
              Приветствую вас! В данный момент вы находитесь на страничке &quot;Фортуна&quot;. Здесь вы можете узнать
              много об
              Экспериментальной школе-комплекс N 18 города Йошкар-Ола. Так же вы можете расширить не только круг друзей,
              но и собственный кругозор.От души посмеяться!!!
            </p>
            <p class="ft-main-text">
              Рекомендую для лучшего просмотра использовать <span class="black--text">Netscape Communicator.</span>
            </p>
            <p>
              Последнее обновление 20.02.2000
            </p>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn outlined color="indigo" @click="dialog = true">
            Реставрация сайта 20.11.2021
          </v-btn>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-dialog v-model="dialog" max-width="490" persistent>
          <v-card>
            <v-img :src="nuxtLogo" max-width="490" />
            <v-card-text class="mt-6">
              <p>
                Мой первый сайт я создал и разместил более 20 лет назад. Много воды утекло, а он до сих пор доступен по
                адресу: <a href="http://georgemr.chat.ru/" target="_blank">http://georgemr.chat.ru/</a>
              </p>
              <p>
                Правда часть функционала уже утрачена, поэтому пришла идея отреставрировать сайт с применением
                современных технологиях: SPA, VUE, NUXT.
              </p>
              <p>Дизайн и наполнение восстановлены без изменений.</p>
            </v-card-text>
            <v-card-actions>
              <v-spacer />
              <v-btn @click="dialog = false">
                Принято
              </v-btn>
              <v-spacer />
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import mainbgimage from '@/static/bgmainpage.jpeg'
import nuxtLogo from '@/static/nuxt.png'

export default {
  name: 'Index',
  data () {
    return {
      mainBgImage: mainbgimage,
      dialog: false,
      nuxtLogo
    }
  }
}
</script>

<style>
.ft-main-text {
  color: blue;
}

.FtMainBody {
  background-repeat: repeat;
  height: 100%;
}
</style>
