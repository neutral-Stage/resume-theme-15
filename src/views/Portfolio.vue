<template>
  <v-app>

    <v-container>
      <v-row
        justify="center"
        align="center"
        class="mt-12"
      >
        <v-col
          md="5"
          cols="12"
          sm="6"
          class="px-6"
        >
          <v-img src="/pic/port1.png">

          </v-img>
        </v-col>
        <v-col
          md="5"
          cols="12"
          sm="6"
          class="px-6"
        >
          <v-img src="/pic/port2.png">

          </v-img>
        </v-col>
      </v-row>

    </v-container>
    <v-row
      no-gutters
      justify="end"
      align="center"
      class="hidden-xs-only"
    >
      <v-col
        md="2"
        class="navblade py-6"
        style="text-align: center;"
      >
        <v-btn
          dark
          fab
          outlined
          color="#fff"
          disabled
          small
          class="ma-3 "
        >
          <v-icon small>mdi-arrow-left</v-icon>
        </v-btn>
        <v-btn
          dark
          fab
          outlined
          color="#fff"
          small
          class="ma-3"
        >
          <v-icon small>mdi-arrow-right</v-icon>
        </v-btn>
      </v-col>
    </v-row>

  </v-app>

</template>

<script>
export default {
  name: "portfolio"
};
</script>

<style >
.theme--light.v-application {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
}
.navblade {
  position: relative;
  background-color: #104efb;
  border-top-left-radius: 300px;
  border-bottom-left-radius: 0;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
</style>
