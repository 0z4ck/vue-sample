<template>
    <v-app-bar
      app
      color="cyan darken-2"
      dark
      fade-img-on-scroll
      shrink-on-scroll
      height="256px"
      src="board.jpg"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-row justify="center" class="text-center {'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}">
        <v-col cols="12">
       
        </v-col>
      </v-row> 
    </v-app-bar>
</template>
