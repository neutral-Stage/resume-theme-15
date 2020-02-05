<template>
  <v-app>

    <v-content>
      <v-container>
        <v-row justify="center" align="center">
          <v-col md="5">
            <v-img src="/pic/port1.png">

            </v-img></v-col>
          <v-col md="5">
            <v-img src="/pic/port2.png">

            </v-img></v-col>
        </v-row>

      </v-container>
      <v-row no-gutters justify="end"  align="center">
        <v-col md="2" class="navblade py-6" style="text-align: center;">
          <v-btn  dark fab outlined color="#fff" disabled small class="ma-3 ">
            <v-icon small >mdi-arrow-left</v-icon>
          </v-btn>
          <v-btn  dark fab outlined color="#fff" small class="ma-3">
            <v-icon small >mdi-arrow-right</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-content>

  </v-app>

</template>

<script>
  export default {
    name: "home"
  }
</script>

<style scoped>
  .theme--light.v-application {
    background: transparent;
    color: rgba(0,0,0,.87);
  }
  .navblade {
    position: relative;
    background-color: #104EFB;
    border-top-left-radius: 300px;
    border-bottom-left-radius: 0;
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
  }
  .navblade:before{

  }

</style>
