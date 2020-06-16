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
        <strong>Sound-Cast</strong> A Podcast App
        </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon x-large color="red">mdi-music</v-icon>
      </v-btn>

      <v-spacer></v-spacer>
        <v-text-field
            
            
          ></v-text-field>
      <v-btn icon>
        <v-icon color="yellow">mdi-magnify</v-icon>
      </v-btn>

    </v-app-bar>

    <v-navigation-drawer color="dark teal accent-4" dark app v-model="isDrawerOpen">
     <v-list-item>
        <v-list-item-content>
          <v-list-item-title text-dark class="title">
           Eximia SoundCast
          </v-list-item-title>
          <v-list-item-subtitle text-dark class="subtitle">
            <strong>Podcasts-App</strong>
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-list>


  

        <v-list-item-title v-on:click="navigate('/')">
          <v-list-item-action>
            <v-list-item-icon>
           <v-icon color="pink darken-2">mdi-home</v-icon>
           </v-list-item-icon>


          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title >Home</v-list-item-title >
          </v-list-item-content>
        </v-list-item-title>

           <v-list-item-title v-on:click="navigate('about')">
          <v-list-item-action>
             <v-list-item-icon>
           <v-icon color="yellow lighten-2">mdi-domain</v-icon>
             </v-list-item-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title >About</v-list-item-title >
          </v-list-item-content>
        </v-list-item-title>

             <v-list-item-title v-on:click="navigate('support')">
          <v-list-item-action>
            <v-list-item-icon>
           <v-icon color="orange darken-2">mdi-arrow-up-bold-box-outline</v-icon>
           </v-list-item-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title >Contact</v-list-item-title >
          </v-list-item-content>
        </v-list-item-title>

             <v-list-item-title v-on:click="navigate('social')">
          <v-list-item-action>
            <v-list-item-icon>
           <v-icon color="red darken-2">mdi-heart</v-icon>
           </v-list-item-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title dark ><a href="www.eximia.fi" target="blank">ShowUs Love</a></v-list-item-title >
          </v-list-item-content>
        </v-list-item-title>

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
  },
  methods:{
    navigate: function(route){
      this.$router.push(route);
    }
  }
}
</script>

<style scoped>
a{
  color: hotpink;
  text-decoration:none;
  }
</style>