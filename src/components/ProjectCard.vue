<template>
  <v-card style="min-height: 200px" outlined>
    <v-card-title>
      <v-btn :href="project.link" text>
        <v-icon>mdi-github</v-icon>
        <span> {{ project.title }} </span>
      </v-btn>
    </v-card-title>
    <v-card-subtitle>
      <li>Category: {{ project.category }}</li>
      <li>Stack: {{ project.stack }}</li>
    </v-card-subtitle>
    <v-card-text> {{ project.text }} </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: ['project'],
}
</script>
