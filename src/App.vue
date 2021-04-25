<template>
  <v-app>
    <HeaderComponent/>
    <v-main>
      <MainContent/>
      <FooterComponent/>
    </v-main>
  </v-app>
</template>

<script>
import HeaderComponent from './components/HeaderComponent';
import MainContent from './components/MainContent';
import FooterComponent from './components/FooterComponent';

export default {
  name: 'App',

  components: {
    HeaderComponent,
    MainContent,
    FooterComponent,
  },

  data: () => ({
    //
  }),
};
</script>
