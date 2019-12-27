<template>
  <v-container fluid class="mx-0">
    <v-row align="center" justify="center" class="mx-2">
      <h1 class="text-center">YOU MUST CONSTRUCT ADDITIONAL PYLONS</h1>
    </v-row>
    <v-row align="center" justify="center" class="mx-2">
      <p class="text-center mt-2 mb-0">
        This domain contains quotes from classic blizzard entertainment games.
        Each game below leads to a user interface along with an API for said
        game.
      </p>
    </v-row>
    <v-row align="center" justify="center">
      <section
        v-for="(image, i) in images"
        :key="i"
        align="center"
        justify="center"
      >
        <a :href="image.href">
          <v-img :alt="image.alt" :src="image.src" class="game-icon" />
          <p>{{ image.mouseOver }}</p>
        </a>
      </section>
    </v-row>
    <v-row align="center" justify="center" class="mx-2">
      <p class="text-center mt-2 mb-0">
        For questions or assistance, e-mail blizzardquotes@gmail.com
      </p>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Information',

  data: () => ({
    dimensions: '400',
    images: [
      {
        id: 'warcraft-3-quotes',
        alt: 'Warcraft 3 Quotes',
        href: 'https://wc3.blizzardquotes.com',
        src: require('@/assets/blizzard/warcraft-iii.svg')
      },
      {
        id: 'starcraft-2-quotes',
        alt: 'Starcraft 2 Quotes',
        href: 'https://sc2.blizzardquotes.com',
        src: require('@/assets/blizzard/starcraft-ii.svg')
      },
      {
        id: 'starcraft-1-quotes',
        alt: 'Starcraft 1 Quotes',
        href: 'https://sc.blizzardquotes.com',
        src: require('@/assets/blizzard/starcraft-remastered.svg')
      }
    ]
  })
};
</script>

<style>
div.game-icon {
  opacity: 0.85;
  height: 400px;
  width: 400px;
  transition: opacity 0.15s;
}
div.game-icon:hover {
  opacity: 1;
}
</style>
