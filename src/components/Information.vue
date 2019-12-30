<template>
  <v-container fluid>
    <v-row justify="center" class="mx-2">
      <h1>BY THE LIGHT OF THE MOON</h1>
    </v-row>
    <v-row justify="center" class="mx-2">
      <p class="text-justify mt-2 mb-0">
        This domain contains quotes from classic Blizzard Entertainment games.
        Each game below leads to a user interface along with an API for said
        game containing memorable quotes. Click one of the games below for more
        information.
      </p>
    </v-row>
    <v-row justify="center">
      <section v-for="(image, i) in images" :key="i">
        <a :href="image.href">
          <v-img :alt="image.alt" :src="image.src" class="game-icon" />
        </a>
      </section>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Information",

  data: () => ({
    images: [
      {
        id: "warcraft-3-quotes",
        alt: "Warcraft 3 Quotes",
        href: "https://wc3.blizzardquotes.com",
        src: require("@/assets/blizzard/warcraft-iii.svg")
      },
      {
        id: "starcraft-2-quotes",
        alt: "Starcraft 2 Quotes",
        href: "https://sc2.blizzardquotes.com",
        src: require("@/assets/blizzard/starcraft-ii.svg")
      },
      {
        id: "starcraft-1-quotes",
        alt: "Starcraft 1 Quotes",
        href: "https://sc.blizzardquotes.com",
        src: require("@/assets/blizzard/starcraft-remastered.svg")
      }
    ]
  })
};
</script>

<style>
.game-icon {
  opacity: 0.8;
  height: 300px;
  width: 300px;
  transition: opacity 0.2s;
}
.game-icon:hover {
  opacity: 1;
}
</style>
