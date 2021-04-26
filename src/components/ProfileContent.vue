
<template>
  <v-container>
    <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
      <v-col cols="12">
       
        <p style="font-size: 60pt;" class="blue-grey--text darken1"> <v-icon size="60" class="mr-2">mdi-account</v-icon>PROFILE</p>
      </v-col>
      <v-col cols="12">
        <v-card class="pa-6 {'ma-1': $vuetify.breakpoint.smAndDown, 'ma-6': $vuetify.breakpoint.mdAndUp}" >
          <p class="headline pa-6 ma-1 {'ma-1': $vuetify.breakpoint.smAndDown, 'ma-6': $vuetify.breakpoint.mdAndUp}"> 
            スマホ・パソコン・電子機器が大好きな理系学生。
            <br/>
            高校３年生の春、pythonと出会い恋に落ちる。
            <br/>
            大学１年生の秋、暗号通貨と出会い単位を落とす。
          </p>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'ProfileContent',
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
}
