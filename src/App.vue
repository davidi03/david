<template>
  <v-app id="inspire">
    <router-view></router-view>
    <div class="navigation">
      <navigation />
    </div>
  </v-app>
</template>

<script>
import Navigation from "./components/Navigation.vue";

export default {
  components: {
    Navigation,
  },
  data() {
    return {};
  },
};
</script>
