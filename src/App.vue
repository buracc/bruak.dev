<template>
  <v-app>
    <v-app-bar app color="tertiary" dark>
      <div class="d-flex align-center">Projects</div>

      <v-spacer></v-spacer>

      <v-btn href="https://github.com/buracc" text>
        <span class="mr-2">github.com/buracc</span>
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-row style="padding: 1%">
        <v-col md="3" v-for="(p, i) in projects" :key="i">
          <ProjectCard :project="p"></ProjectCard>
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import ProjectCard from '@/components/ProjectCard'

export default {
  name: 'App',
  components: { ProjectCard },
  data: () => ({
    projects: [
      {
        title: 'ov-app',
        stack: 'Android, Kotlin, Gradle',
        category: 'Travel',
        text: 'A public transport trip planner Android app using the Dutch NS public transport API. Inspired by 9292-OV.',
        link: 'https://github.com/buracc/ov-app',
      },
      {
        title: 'botlin',
        stack: 'Java 11, Kotlin, Gradle',
        category: 'Games, Runescape',
        text: 'A customized, lightweight RuneScape (OpenOSRS) client, with a scripting API written in Kotlin.',
        link: 'https://github.com/buracc/botlin',
      },
      {
        title: 'botlin-scripts',
        stack: 'Kotlin, Gradle',
        category: 'Games, Runescape',
        text: 'Automation scripts to use with the Botlin client.',
        link: 'https://github.com/buracc/botlin-scripts',
      },
      {
        title: 'MeteorLite',
        stack: 'Java 16, Gradle, JavaFX',
        category: 'Games, Runescape',
        text: 'Another open source RuneScape client, using JavaFX.',
        link: 'https://github.com/MeteorLite/MeteorLite',
      },
      {
        title: 'SimpleCL',
        stack: '.NET, C#',
        category: 'Games, Silkroad Online',
        text: 'A lightweight client(less) packet framework for Silkroad Online.',
        link: 'https://github.com/buracc/SimpleCL',
      },
      {
        title: 'Hexagon',
        stack: 'Java EE, Maven, Javascript, TypeScript Angular, Ionic Framework, Socket.IO',
        category: 'Entertainment',
        text:
          'A prototype project created for the Amsterdam Arena during my internship at MediaLAB Amsterdam. ' +
          'Hexagon is an e-sports match predicting game (similar to sports betting/predicting), but without the' +
          ' gambling aspects.',
        link: 'https://github.com/buracc/Hexagon',
      },
    ],
  }),
}
</script>
