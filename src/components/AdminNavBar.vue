<template>
  <nav>
    <v-app-bar app flat class="blue-grey lighten-5">
       <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase">Dashboard</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
        <v-btn
          v-bind="attrs"
          v-on="on"
          small
          class="mr-1"
        >
           Menu <v-icon>mdi-chevron-down</v-icon>
        </v-btn>
      </template>

        <v-list dense class="py-0">

       <v-divider></v-divider>
        <v-list-item-group
        color="primary"
      >
        <v-list-item
          v-for="(link, i) in links"
          :key="i" router :to="link.route"
        >
          <v-list-item-icon class="mr-0">
            <v-icon small v-text="link.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title> {{link.text}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
          <v-divider></v-divider>
      </v-list-item-group>
    </v-list>        

      </v-menu>
      
      <v-btn small class="text-capitalize">
        <span>Sign Out</span>
        <v-icon right>mdi-logout</v-icon>
      </v-btn>
    </v-app-bar>

     <v-navigation-drawer
      v-model="drawer"
      app
      class="leftbar"
    >

    <v-list dense class="py-0">
    <p  class="text-center mb-0 py-2 grey lighten-1 white--text text--bold">
        MarnSteel
       <span class="off_leftbar"> <v-icon fab outlined color="white" class="hidden-md-and-up red--text font-weight-bold" large @click="drawer = false">mdi-alpha-x</v-icon></span>
    </p>
      
     <v-divider></v-divider>
      <v-list-item-group
        color="primary"
      >
        <v-list-item
          v-for="(link, i) in links"
          :key="i" router :to="link.route"
          class="white--text"
        >
          <v-list-item-icon class="mr-0">
            <v-icon small v-text="link.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="link.text"> {{i}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
          <v-divider></v-divider>
      </v-list-item-group>
    </v-list>

    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
    data() {
        return {
            drawer:true,
             links: [
                    { text: 'Dashboard', icon: 'mdi-view-dashboard',route:'/' },
                    { text: 'Local Purches', icon: 'mdi-briefcase' ,route:'localpurches'},
                    { text: 'Import Purches', icon: 'mdi-briefcase' ,route:'importpurches'},
                ],
        }
    }
};
</script>

<style scoped>
.leftbar{
    background: #9652ff !important;
}
.off_leftbar {
    position: fixed;
    top: 1px;
    right: 0%;
    cursor: pointer;
    font-size: 14px;
}
</style>