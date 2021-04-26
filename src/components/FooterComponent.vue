<template>
<!--
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon.id"
          class="mx-4 white--text"
          icon
          :href="icon[1]"
          target="_blank"
        >
          <v-icon size="24px">
            {{ icon[0] }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
         <v-spacer></v-spacer>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>-->
  <v-footer
    dark
    padless
  >
    <v-card
      class="cyan darken-2 white--text text-center flex pb-0"
      flat
      tile
    >
      <v-card-title class="pb-0 cyan darken-2">
        <p class="overline subheading my-0 py-0">Get connected with us on social networks!</p>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon.id"
          :href=icon[1]
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">
            {{ icon[0] }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="pb-2 pt-0 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        ['mdi-web',"http://www.z4ck.tk/"],
        ['mdi-twitter',"https://twitter.com/z4ckz4ckz4ck"],
        ['mdi-github', "https://github.com/0z4ck"],
      ],
    }),
  }
</script>


