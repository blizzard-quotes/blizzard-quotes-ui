<template>
  <v-container>
    <v-row justify="center" class="mx-2">
      <h1 class="text-center">{{ h1 }}</h1>
    </v-row>
    <v-row justify="center" class="mx-2">
      <p class="text-justify mt-2 mb-0">
        This domain contains quotes from classic Blizzard Entertainment games.
        Each game under this domain leads has a UI and an API for accessing and
        retrieving quotes. For more information, click on the icon for the game
        you are interested in.
      </p>
    </v-row>
    <v-row dense justify="center">
      <v-col cols="12" sm="4" md="4" v-for="(image, i) in images" :key="i">
        <a :href="image.href">
          <v-img
            :alt="image.alt"
            :src="image.src"
            aspect-ratio="1"
            class="game-icon"
          />
        </a>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Konami from 'konami';

const H1_DEFAULT = 'STAY AWHILE AND LISTEN';
const H1_KONAMI = 'BY THE LIGHT OF THE MOON';

export default {
  name: 'Information',

  data: () => ({
    h1: H1_DEFAULT,
    images: [
      {
        id: 'warcraft-3-quotes',
        alt: 'Warcraft 3 Quotes',
        href: 'https://wc3.blizzardquotes.com',
        src: require('@/assets/blizzard/warcraft-iii.svg'),
      },
      {
        id: 'starcraft-2-quotes',
        alt: 'Starcraft 2 Quotes',
        href: 'https://sc2.blizzardquotes.com',
        src: require('@/assets/blizzard/starcraft-ii.svg'),
      },
      {
        id: 'starcraft-1-quotes',
        alt: 'Starcraft 1 Quotes',
        href: 'https://sc.blizzardquotes.com',
        src: require('@/assets/blizzard/starcraft-remastered.svg'),
      },
    ],
  }),
  created() {
    new Konami(() => {
      this.h1 = H1_KONAMI;
    });
  },
};
</script>

<style>
.game-icon {
  opacity: 0.8;
  transition: opacity 0.2s;
}
.game-icon:hover {
  opacity: 1;
}
</style>
