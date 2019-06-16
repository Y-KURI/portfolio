<template>
  <v-app id="inspire">
    <v-layout row>
      <v-flex xs12 sm6 offset-sm3>
        <v-card>
          <v-img
            class="card_img"
            :src="img_src"
            height="100%"
          >
          </v-img>
          <v-card-title primary-title>
            <div>
              <div class="headline">{{ title }}</div>
              <span class="grey--text">{{ summary }}</span>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn flat>
              <a class="ex_link" href="https://ep-hub.herokuapp.com/">app</a>
            </v-btn>
            <v-btn flat>
              <a class="ex_link" href="https://github.com/Y-KURI/ep_hub">src</a></v-btn>
            <v-spacer></v-spacer>
            <v-btn icon @click="show = !show">
              <v-icon>{{ show ? 'keyboard_arrow_down' : 'keyboard_arrow_up' }}</v-icon>
            </v-btn>
          </v-card-actions>
          <v-slide-y-transition>
            <v-card-text v-show="show">
              {{ desc }}
            </v-card-text>
          </v-slide-y-transition>
        </v-card>
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  el: '#app',
  data: () => ({
    show: false,
    img_src: require('~/assets/ep_hub.png'),
    title: 'EPHub',
    summary: 'アイデア共有アプリ',
    desc: '新しいサービスのアイデアをエレベータピッチの手法でまとめ、共有出来るアプリ。プロダクトのCRUDとそのプロダクトの公開ステータスと閲覧権限ユーザー保持まで実装。デモです。'
  })
}
</script>

<style>
#inspire {
  margin: 50px;
}
.card_img {
  filter: drop-shadow(1px 2px 1px rgba(0,0,0,0.4))
}
.work-card {
  background-color: #35495e;
}
.ex_link {
  color: black;
}
</style>
