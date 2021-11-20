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
    </v-container>
  </div>
</template>

<script>
import mainbgimage from '@/static/bgmainpage.jpeg'

export default {
  name: 'Index',
  data () {
    return {
      mainBgImage: mainbgimage
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
