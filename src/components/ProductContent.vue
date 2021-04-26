<template>
  <v-container>
    <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
      <v-col cols="12">
       
        <p style="font-size: 60pt;" class="blue-grey--text darken1"> <v-icon size="60" class="mr-2">mdi-sword-cross</v-icon>Product</p>
      </v-col>
      <v-col cols="12" sm="6" md="6" lg="6" xl="6"
        v-for="skill in skills" :key="skill.id" >
        <v-card class="pa-6 {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}"
          elevation="1" >
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
            <v-icon size=24pt>
              {{skill.icon}}
            </v-icon>
            <p class="headline ma-1 pa-6">
              {{skill.title}}
            </p>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}">
            <v-card-text class="ma-1">
              {{skill.description}}
              <div v-if="skill.url=='shogi.jpg'">
                <a href="https://github.com/0z4ck/Reiou" target="_blank">将棋アプリ令王</a>
              </div>
            </v-card-text>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}">
            <v-img :src="skill.url" max-height="450">
            </v-img>
          </v-row>
        </v-card> 
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'MainContent',
    computed: {
      size () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 10
          case 'sm': return 16
          case 'md': return 20
          case 'lg': return 30
          case 'xl': return 30
        }
      },
    },
    data: () => ({
      skills: 
        [   
            {   url: "order.jpg",
                icon: 'mdi-web',
                title: '注文管理システム',
                description: '複数のフードデリバリーサービスを利用している飲食店で全サービスからの注文を一つのページに統合するwebアプリ。各サービスのAPIを利用し取得した情報をデータベースに挿入し、webアプリからの要求に応じてphpでデータを整形して返しています。またシングルボードコンピューターを店内に置き、レシート印刷用プリンターとbluetoothで接続しレシートの印刷を自動化しました。主にデータの収集にpythonを使いプリンターとシリアル通信する部分はnodejsを使いました。',
            },
            {   url: "marker.jpg",
                icon: 'mdi-desktop-tower',
                title: 'Google Map APIを使ったデータの可視化',
                description: 'ゲーム内で取得できる距離情報からそのオブジェクトの座標を算出しGoogleMapAPIで可視化したもの。データ取得の部分、大遠距離・二つの円の交点の計算はpythonで書き、データベースに挿入。javascriptのMapAPIでどの範囲が画面内に表示されてるのか取得・計算し、phpでその範囲のデータを出力する。躓いた点はSQLのクエリ時間が長く、画面を動かすたびにイベントが発生し再取得が行われるので差分の計算が必要だったことです。緯度・経度のカラムにインデックスを作成するとクエリ時間が大幅に短くなりUXが良くなりました。',
            },
            {   url: "bench.jpg",
                icon: 'mdi-cellphone',
                title: 'Androidのベンチマークアプリ',
                description: 'Androidアプリで、色々なアルゴリズムで計算量の多い処理を行い、実行時間で割ることでスコアを算出。CPU内には加法用の演算装置と乗法用の演算装置があり,CPUによって得意不得意が違うので気になって実験するために作りました。',
            },
            {   url: "batmon.jpg",
                icon: 'mdi-cellphone',
                title: 'アプリの上で表示されるAndroidアプリ',
                description: '「オーバーレイ」と言ったり「フローティングビュー」と言ったりするのですが、アプリの上でアプリを表示し、画面のどこにでもスライドさせることができるアプリを作りました。バッテリーの出力電圧と電流をリアルタイムで取得し表示するアプリでした。この「フローティングビュー」ですが私が作った当初は文献も少なく実装が大変でした。',
            },
            {   url: "shogi.jpg",
                icon: 'mdi-remote-desktop',
                title: '将棋のゲーム(作りかけ)',
                description: '将棋のゲームをUnityで作り始めました。C#は初めてだったのですが他の言語と記法は似ていたので特に躓きポイントはなかったです。普段はプライベートリポジトリなのですがしばらくパブリックに致します。',
            },
        ],
    }),
  }
</script>
