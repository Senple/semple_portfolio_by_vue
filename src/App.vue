<template>
  <v-app id="inspire">
    <v-app-bar app color="white" flat>
      <v-avatar
        :color="$vuetify.breakpoint.smAndDown ? 'grey darken-1' : 'transparent'"
        size="32"
      ></v-avatar>

      <v-tabs centered class="ml-n9" color="grey darken-1">
        <v-tab v-for="link in links" :key="link">{{ link }}</v-tab>
      </v-tabs>

      <!-- https://qiita.com/sudo5in5k/items/92e759bb024abab5f328 -->
      <v-btn v-for="website in websites" :key="website" class="mx-4" fab icon>
        <a v-bind:href="website.link">
          <v-avatar size="45">
            <img v-bind:src="website.icon" alt="avatar" />
          </v-avatar>
        </a>
      </v-btn>
    </v-app-bar>

    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
          <v-col cols="12" sm="2">
            <v-sheet rounded="lg" min-height="268">
              <!--  -->
            </v-sheet>
          </v-col>

          <v-col cols="12" sm="8">
            <v-sheet min-height="70vh" rounded="lg">
              <!--  -->
            </v-sheet>
          </v-col>

          <v-col cols="12" sm="2">
            <v-sheet rounded="lg" min-height="268">
              <!--  -->
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    links: ["About", "Skill", "Travel", "Contact"],
    websites: [
      // {
      //   text: "Twitter",
      //   link: "https://twitter.com/your_account",
      //   icon: require("@/assets/twitter-logo.png")
      // },
      // {
      //   text: "Facebook",
      //   link: "https://www.facebook.com/people/your_account",
      //   icon: require("@/assets/facebook-logo.png")
      // },
      {
        text: "Github",
        link: "https://github.com/Senple",
        icon: require("@/assets/GitHub-Mark-64px.png")
      }
    ]
  })
};
</script>
