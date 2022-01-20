<template>
  <v-app class="main_div">
    <admin-nav-bar></admin-nav-bar>
    <v-main class="mt-4">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import AdminNavBar from './components/AdminNavBar.vue';
export default {
  components: { AdminNavBar },
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style >
.main_div{
  background: #ECEFF1 !important;
}
</style>