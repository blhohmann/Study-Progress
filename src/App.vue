<template>
  <VApp class="rounded rounded-md">
    <!-- Sidebar -->

    <!-- Cards -->
    <v-app-bar>
      <v-spacer></v-spacer>
      <v-toolbar-title class="text-center">What, like it's hard?</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer>
      <v-list>
        <v-list-item title="Navigation drawer"></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
      <div id="app">
        <ChartComponent />
      </div>
      <!-- this is only for personal use cannot use commercially, generated via https://designer.microsoft.com/image-creator -->
      <v-img src="@/assets/happy.jpeg" aspect-ratio="2.75"></v-img>
    </v-main>
  </VApp>
</template>

<script>
import ChartComponent from './components/CaseProgChart.vue';

export default {
  name: 'App',
  components: {
    ChartComponent
  }
}
</script>
