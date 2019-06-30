<template>
  <v-app id="inspire">
    <v-layout row>
      <v-flex xs12 sm6 offset-sm3>
        <v-card
          v-for="work in works"
          :key="work.id"
          >
          <v-img
            class="card_img"
            :src=work.img_src
            height="100%"
          >
          </v-img>
          <v-card-title primary-title>
            <div>
              <div class="headline">{{ work.title }}</div>
              <span class="grey--text">{{ work.summary }}</span>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn flat>
              <a class="ex_link" v-bind:href="work.app_link">app</a>
            </v-btn>
            <v-btn flat>
              <a class="ex_link" v-bind:href="work.src_link">src</a></v-btn>
            <v-spacer></v-spacer>
            <v-btn icon @click="work.show = !work.show">
              <v-icon>{{ work.show ? 'keyboard_arrow_down' : 'keyboard_arrow_up' }}</v-icon>
            </v-btn>
          </v-card-actions>
          <v-slide-y-transition>
            <v-card-text v-show="work.show">
              {{ work.desc }}
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
    works: [
      {
        id: 1,
        img_src: require('~/assets/ep_hub.png'),
        title: 'EPHub',
        summary: 'アイデア共有アプリ',
        desc: '新しいサービスのアイデアをエレベータピッチの手法でまとめ、共有出来るRailsアプリ。プロダクトのCRUDとそのプロダクトの公開ステータスと閲覧権限ユーザー保持まで実装。デモです。',
        app_link: 'https://ep-hub.herokuapp.com/',
        src_link: 'https://github.com/Y-KURI/ep_hub',
        show: false
      },
      {
        id: 2,
        img_src: require('~/assets/todo_app.png'),
        title: 'TODO',
        summary: 'TODOアプリ',
        desc: '任意のフォルダごとにTODOを登録できるLaravelアプリ。着手ステータス、期限、ユーザー認証機能。',
        app_link: 'https://todo-laravelapp.herokuapp.com/',
        src_link: 'https://github.com/Y-KURI/todo_laravel',
        show: false
      }
    ]
  })
}
</script>

<style>
.v-card {
  margin: 10px;
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
