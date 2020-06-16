<template>
  <v-container fluid grid-list-lg>
      <v-layout wrap>
          <v-flex xs4 v-for="(sound,index) in sounds" :key="index">
              <v-card dark color="" v-on:click="play(sound.sound)">
                  <v-card-text>
                               <v-icon x-large color="yellow darken-2">mdi-play</v-icon>
                               <p light>{{sound.title}}</p>
                  </v-card-text>
              </v-card>

          </v-flex>
      </v-layout>
  </v-container>
</template>

<script>
export default {

    name:'Sounds',
    data(){
        return {
            sounds:[
                {
                    title:"What is Biology?",
                    sound:"What is Biology.mp3"
                },
                   {
                    title:"A song i wrote about twitter",
                    sound:"a song i wrote about twitter.mp3"
                },
                  {
                    title:"Kanye West - POWER",
                    sound:"Kanye West - POWER.mp3"
                },
                  {
                    title:"What is Coding",
                    sound:"What is Coding.mp3"
                },
                  {
                    title:"Growth in the Digital Era Is about More Than Technology",
                    sound:"Growth in the Digital Era Is about More Than Technology.mp3"
                },
                  {
                    title:"Enter the Digital era, with Thales",
                    sound:"Enter the Digital era, with Thales.mp3"
                },
                  {
                    title:"Are you ready for the digital era _ Deloitte Nederland",
                    sound:"Are you ready for the digital era _ Deloitte Nederland.mp3"
                },
                  {
                    title:"How podcasts became so popular",
                    sound:"How podcasts became so popular.mp3"
                },
                  {
                    title:"CastBox CEO on the AI-driven Future of Podcasts",
                    sound:"CastBox CEO on the AI-driven Future of Podcasts.mp3"
                },
                  {
                    title:"Borrowed Future – The Podcast On the Student Loan Crisis and the Way Out",
                    sound:"Borrowed Future – The Podcast On the Student Loan Crisis and the Way Out.mp3"
                }
            ]
        }
    },
    methods:{
        play: function(name){
            let audio = new Audio(require('@/assets/sounds/'+name));


            audio.play();
            //audio.pause();
        }
    }
}

</script>

