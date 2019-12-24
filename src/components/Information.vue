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
      <v-column v-for="quote in quotes" :key="quote">
        <a :href="quote.href">
          <v-img
            :alt="quote.text"
            height="400"
            width="400"
            :src="quote.image"
          />
        </a>
      </v-column>
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
  name: 'HelloWorld',

  data: () => ({
    quotes: [
      {
        text: 'Warcraft 3 Quotes',
        href: 'https://wc3.blizzardquotes.com',
        image: require('@/assets/blizzard/warcraft-iii.svg')
      },
      {
        text: 'Starcraft 2 Quotes',
        href: 'https://sc2.blizzardquotes.com',
        image: require('@/assets/blizzard/starcraft-ii.svg')
      },
      {
        text: 'Starcraft 1 Quotes',
        href: 'https://sc.blizzardquotes.com',
        image: require('@/assets/blizzard/starcraft-remastered.svg')
      }
    ]
  })
};
</script>
