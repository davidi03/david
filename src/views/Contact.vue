<template>
  <v-app>
    <div class="header">
      <router-view></router-view>
    </div>
    <v-row v-for="n in 1" :key="n" :class="n === 1 ? 'mb-6' : ''" no-gutters>
      <v-card>
        <v-card-title primary-title> This is the Contact Form. </v-card-title>
        <contact />
      </v-card>
    </v-row>
  </v-app>
</template>

<script>
import Contact from "@/components/contactForm.vue";

export default {
  data() {
    return {
      name: "App",
    };
  },
  components: {
    Contact,
  },
};
</script>
