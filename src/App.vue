<template>
  <v-app>
    <Header></Header>
    <v-main>
      <Information></Information>
    </v-main>
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
    Footer,
  },

  data: () => ({}),

  created() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
