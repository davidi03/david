<template>
  <v-app id="inspire">
    <!-- <v-app-bar app color="orange">
      
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-filter</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-navigation-drawer v-model="drawer" app fixed absolute left temporary>
        <v-list nav dense>
          <v-list-item-group active-class="orange--text text--accent-4">
            <v-list-item
              v-for="item in items"
              :key="item.title"
              dense
              router
              :to="item.route"
            >
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-title>{{ item.title }}</v-list-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-app-bar> -->
    <div>
      <navigation />
    </div>
    <!-- <router-view></router-view> -->
  </v-app>
</template>

<script>
import Navigation from "@/components/Navigation.vue";

export default {
  data() {
    return {
      name: "App",
    };
  },
  components: {
    Navigation,
  },
};
</script>
