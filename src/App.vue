<template>
  <v-app>
    <HeaderComponent/>
    <v-main class="light-blue lighten-5">
      <ProfileContent/>
      <MainContent/>
      <ProductContent/>
    </v-main>
    <FooterComponent/>
  </v-app>
</template>

<script>
import HeaderComponent from './components/HeaderComponent';
import ProfileContent from './components/ProfileContent';
import MainContent from './components/MainContent';
import ProductContent from './components/ProductContent';
import FooterComponent from './components/FooterComponent';

export default {
  name: 'App',

  components: {
    HeaderComponent,
    ProfileContent,
    MainContent,
    ProductContent,
    FooterComponent,
  },

  data: () => ({
    //
  }),
};
</script>
