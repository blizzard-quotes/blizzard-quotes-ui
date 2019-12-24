<template>
  <v-app>
    <Header></Header>
    <v-content>
      <Information></Information>
    </v-content>
    <Footer></Footer>
  </v-app>
</template>

<script>
import Header from './components/Header';
import Information from './components/Information';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Header,
    Information,
    Footer
  },

  data: () => ({}),

  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>
