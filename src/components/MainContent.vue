<template>
  <v-container>
    <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
      <v-col cols="12">
       
        <p style="font-size: 60pt;" class="blue-grey--text darken1"> <v-icon size="60" class="mr-2">mdi-sword-cross</v-icon>SKILL</p>
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
            </v-card-text>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}">
            <v-col cols=4
              v-for="colname in colsname" :key="colname.id">
              <p>{{colname}}</p>
            </v-col>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}"
            v-for="tech in skill.techs" :key="tech.id">
            <v-col cols=4
              v-for="cell in tech" :key="cell.id">
              <div v-if='isNaN(cell)||cell==""'>
                <p>{{cell}}</p>
              </div>
              <!-- -->
              <div v-else>
                <v-rating half-increments background-color="gray" color="gray" readonly :value="cell" 
                  :dense=true :size="size" >
                </v-rating>
              </div>
              <!-- -->
            </v-col>
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
        return 10;
      }
    },
    data: () => ({
      colsname: ["技術","経験年数","スキル"],
      skills: 
        [   
            {
                icon: 'mdi-web',
                title: 'Webフロントエンド',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["HTML", "3年", 2],
                           ["CSS", "3年", 2],
                           ["JavaScript", "3年", 2.5],
                           ["jQuery", "3年", 1.5],
                           ["Vue.js", "半年", 1.5],
                           ["-", "-", "-"],
                       ]
            },
            {
                icon: 'mdi-desktop-tower',
                title: 'バックエンド',
                description: '直近ではnodeやphpを書くことがありました。',
                techs: [
                           ["Python(2,3)", "6年", 5],
                           ["PHP", "2年", 2.5],
                           ["Nodejs", "1年", 2.5],
                           ["Shell", "7年", 2],
                           ["C", "4年", 3.5],
                           ["C++", "2年", 3],
                       ]
            },
            {
                icon: 'mdi-server',
                title: 'インフラ・サーバー',
                description: '国内のVPSやレンタルサーバーも借りなれています。',
                techs: [
                           ["Linux", "7年", 5],
                           ["Nginx", "3年", 3],
                           ["Apache", "2年", 2],
                           ["GCP,Azure", "3年", 4],
                       ]
            },
            {
                icon: 'mdi-database',
                title: 'DB',
                description: '直近では慣れないphpでSQLiを塞ぐ実装に頭を捻らせていました。',
                techs: [
                           ["MySQL", "3年", 4],
                           ["PostgreSQL", "1年", 3.5],
                           ["SQLite", "3年", 2],
                           ["-", "-", "-"],
                       ]
            },
            {
                icon: 'mdi-remote-desktop',
                title: 'DevOps',
                description: '最近はDockerでAlpineをベースに開発環境を作る事が増えました。',
                techs: [
                           ["Docker", "1年", 4],
                           ["Ansible", "1年", 1],
                           ["Git", "3年", 2],
                       ]
            },
            {
                icon: 'mdi-google-controller',
                title: 'ゲーム',
                description: '最近少しUnityとC#を始めましたがまだよく分かっていないです。',
                techs: [
                           ["Unity", "半年", 1],
                           ["C# (Unity)", "半年", 2],
                           ["-", "-", "-"],
                       ]
            },
            {
                icon: 'mdi-cellphone',
                title: 'モバイル',
                description: 'Androidシステム関連の機能を重視していてUIは手抜きな物が多いです。',
                techs: [
                           ["AndroidStudio", "3年", 3],
                           ["Java", "3年", 3],
                           ["Smali(dalvik assembly)", "3年", 2],
                       ]
            },
            {
                icon: 'mdi-developer-board',
                title: 'その他',
                description: 'Arduinoでデータベースに自動挿入される測りを作りました。',
                techs: [
                           ["Scheme", "半年", 3],
                           ["Arduino", "2年", 3.5],
                           ["LabView", "1年", 2.5],
                       ]
            },
        ],
    }),
  }
</script>
