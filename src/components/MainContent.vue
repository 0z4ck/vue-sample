<template>
  <v-container>
    <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
      <v-col cols="12" sm="6" md="6" lg="6" xl="6"
        v-for="skill in skills" :key="skill" >
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
            <p class="overline ma-1">
              {{skill.description}}
            </p>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}">
            <v-col cols=4
              v-for="colname in colsname" :key="colname">
              <p>{{colname}}</p>
            </v-col>
          </v-row>
          <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-1': $vuetify.breakpoint.mdAndUp}"
            v-for="tech in skill.techs" :key="tech">
            <v-col cols=4
              v-for="cell in tech" :key="cell">
              <p>{{cell}}</p>
            </v-col>
            <v-col cols=4
              v-for="cell in tech" :key="cell">
              <div v-if="isNaN(cell)">
                <p>{{cell}}</p>
              </div>
              <!-- -->
              <div v-else>
                <v-rating half-increments background-color="gray" color="gray" readonly v-bind:value="cell">
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

    data: () => ({
      colsname: ["技術","経験年数","スキル"],
      skills: 
        [   
            {
                icon: 'mdi-web',
                title: 'Webフロントエンド',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-desktop-tower',
                title: 'バックエンド',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-server',
                title: 'インフラ・サーバー',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-database',
                title: 'DB',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-remote-desktop',
                title: 'DevOps',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-google-controller',
                title: 'ゲーム',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
            {
                icon: 'mdi-cellphone',
                title: 'モバイル',
                description: 'このページではVuetifyを使いました。',
                techs: [
                           ["JavaScript", "3年", "2"],
                           ["JavaScript", "3年", "2"],
                       ]
            },
        ],
    }),
  }
</script>
