<template>
  <div>
    <v-app-bar
      color="teal darken-1"
      dense
      dark
    >
      <v-app-bar-nav-icon v-on:click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <span class="font-weight-black">
        Eximia
        </span>
        <strong>Sound-Cast</strong> A Podcast based App for students
        </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon color="red">mdi-heart</v-icon>
      </v-btn>
        <v-text-field
            
            
          ></v-text-field>
      <v-btn icon>
        <v-icon color="yellow">mdi-magnify</v-icon>
      </v-btn>

    </v-app-bar>
    <v-navigation-drawer color="teal darken-4" dark app v-model="isDrawerOpen">
      <v-list>
        <v-list-title>
          <v-list-title-action>
           <v-icon x-large>mdi-home</v-icon>
          </v-list-title-action>
          <v-list-title-content></v-list-title-content>
        </v-list-title>
      </v-list>

    </v-navigation-drawer>
  </div>
</template>


<script>
export default {
  name:'Navbar',
  data(){
    return {
      isDrawerOpen:false
    }
  }
}
</script>

<style>

</style>