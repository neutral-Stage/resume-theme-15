<template>
  <v-app>
    <section>
      <v-row justify="center" align="center">
        <v-col md="6" cols="12">
          <v-row justify="center" align="center" no-gutters>
            <v-col md="3" cols="4" sm="4">
              <v-avatar class="profile ml-12 hidden-sm-and-down" size="150">
                <img src="/pic/avatar.jpg" alt="John" />
              </v-avatar>
              <v-avatar class="profile ml-n3 hidden-md-and-up" size="100">
                <img src="/pic/avatar.jpg" alt="John" />
              </v-avatar>
            </v-col>
            <v-col md="4" cols="6" sm="6" class="detail">
              <div class="headline white--text ">Jennifer lopez</div>
              <div class="subtitle-1 white--text">Web Designer</div>
              <v-row no-gutters class="hidden-sm-and-down">
                <v-icon
                  color="white"
                  class="pt-2 pr-3"
                  v-for="icon in icons"
                  :key="icon.name"
                  >{{ icon.name }}</v-icon
                >
              </v-row>
              <v-btn
                outlined
                fab
                small
                v-for="(icon, index) in media"
                :key="index"
                color="white"
                class="mr-3 hidden-md-and-up"
              >
                <v-icon small color="white">{{ icon }}</v-icon>
              </v-btn>
            </v-col>
            <v-row
              no-gutters
              class="hidden-md-and-up mt-12"
              align="center"
              justify="center"
            >
              <v-icon
                color="#104efb"
                class="pt-2 pr-3"

                v-for="icon in icons"
                :key="icon.name"
                >{{ icon.name }}</v-icon
              >
            </v-row>
            <v-col md="3" cols="6" class="hidden-sm-and-down">
              <v-btn
                outlined
                fab
                small
                v-for="(icon, index) in media"
                :key="index"
                color="white"
                class="mr-3"
              >
                <v-icon small color="white">{{ icon }}</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col md="6" class="hidden-sm-and-down">
          <v-row no-gutters justify="center">
            <v-col md="8" class="blade">
              <v-row no-gutters justify="center" class="mt-6 mr-3">
                <v-col md="4" class="index line">
                  <h2 class="subtitle-1 text-center font-weight-bold textcol">
                    10$
                  </h2>
                  <h2 class="caption text-center textcol">hourly rate</h2>
                </v-col>
                <v-col md="4" class="index">
                  <h2 class="subtitle-1 text-center font-weight-bold textcol">
                    35 HOURS
                  </h2>
                  <h2 class="caption text-center textcol">
                    weekly availability
                  </h2>
                </v-col>
                <v-col md="3" class="index">
                  <v-btn
                    color="#104EFB"
                    rounded
                    x-large
                    block
                    class="white--text"
                  >
                    HIRE ME
                  </v-btn>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>

        <v-col cols="12" sm="12" class="hidden-md-and-up">
          <v-row no-gutters justify="center">
            <v-col md="8" class="blademob">
              <v-row no-gutters justify="center" class="mt-6 mr-3">
                <v-col sm="6" cols="6" class="index linemob">
                  <h2 class="subtitle-1 text-center font-weight-bold white--text">
                    10$
                  </h2>
                  <h2 class="caption text-center white--text">hourly rate</h2>
                </v-col>
                <v-col sm="6" cols="6" class="index">
                  <h2 class="subtitle-1 text-center font-weight-bold white--text">
                    35 HOURS
                  </h2>
                  <h2 class="caption text-center white--text">
                    weekly availability
                  </h2>
                </v-col>
              </v-row>
              <v-col cols="12" sm="12" class="index mt-12 text-center">
                <v-btn
                        color="#104EFB"
                        rounded
                        x-large

                        class="white--text pb-10 pt-6 px-12"
                >
                  HIRE ME
                </v-btn>
              </v-col>
            </v-col>
          </v-row>
        </v-col>
        <v-col md="8" class="mt-10">
          <v-row>
            <v-col class="index" md="2" v-for="tab in tabs" :key="tab.name">
              <router-link
                :to="tab.link"
                active-class="title font-weight-bold textcol textunder"
                class="title textcol"
                >{{ tab.name }}</router-link
              >
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row no-gutters justify="center">
        <v-col md="12">
          <router-view></router-view>
        </v-col>
      </v-row>
    </section>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld
  },

  data() {
    return {
      icons: [
        { name: "mdi-behance" },
        { name: "mdi-dribbble" },
        { name: "mdi-pinterest" },
        { name: "mdi-instagram" },
        { name: "mdi-linkedin" }
      ],
      media: ["mdi-message-text", "mdi-volume-high", "mdi-video-vintage"],
      tabs: [
        {
          name: "Portfolio",
          link: "/portfolio"
        },
        {
          name: "Skills",
          link: "/skills"
        },
        {
          name: "Work",
          link: "/work"
        },
        {
          name: "Education",
          link: "/education"
        }
      ]
    };
  }
};
</script>

<style>
 .cls-1{fill:#104efb;}
.textcol {
  color: #104efb !important;
}
section {
  position: relative;
  margin: 0;
  padding: 0;
  background: url("/pic/curved.svg");
  background-repeat: no-repeat;
  background-size: contain;
}
@media only screen and (max-width: 600px) {
  section {
    position: relative;
    margin: 0;
    padding: 0;
    background: url("/pic/curvedmob.svg");
    background-repeat: no-repeat;
    background-size: contain;
  }
  .detail{
    margin-left: 24px !important;
  }
}
 @media only screen and (max-width: 1000px ) and (min-width: 650px ) {
   section {
     position: relative;
     margin: 0;
     padding: 0;
     background: url("/pic/curvedtab.svg");
     background-repeat: no-repeat;
     background-size: contain;
   }
 }
#curve {
  position: absolute;
  bottom: 0;
  width: 100%;
}
#curve path {
  fill: #fff;
}
#curvemob{
  position: absolute;
  top: 0;
  width: 100%;
}
#curvemob path {
  fill: #fff;
}
a {
  text-decoration: none;
}
.textunder {
  text-decoration: underline;
  text-underline-position: under;
}
.blade {
   position: relative;
   margin-top: 30px;
   z-index: 1;
 }
 .blade:before {
   content: "";
   background-color: #fff;
   position: absolute;
   width: 100%;
   top: 0;
   height: 100px;
   border-top-left-radius: 300px;
   border-bottom-left-radius: 0;
   border-top-right-radius: 0;
   border-bottom-right-radius: 300px;
   z-index: 1;
 }
 .blademob {
   position: relative;
   margin-top: 30px;
   z-index: 1;
 }
 .blademob:before {
   content: "";
   background-color: #104efb;
   position: absolute;
   width: 100%;
   top: 0;
   height: 100px;
   border-top-left-radius: 300px;
   border-bottom-left-radius: 0;
   border-top-right-radius: 0;
   border-bottom-right-radius: 300px;
   z-index: 1;
 }
.index {
  z-index: 10;
}
.line {
  position: relative;
  z-index: 10;
}
.line:after {
  content: "";
  background-color: #104efb;
  position: absolute;
  opacity: 0.44;
  width: 1px;
  bottom: 0;
  right: 0;
  z-index: 100;
  height: 50px;
  border: 1px solid rgba(16, 78, 251, 0.2);
  transform: rotate(180deg);
}
 .linemob {
   position: relative;
   z-index: 10;
 }
 .linemob:after {
   content: "";
   background-color: #fff;
   position: absolute;
   opacity: 0.44;
   width: 1px;
   bottom: 0;
   right: 0;
   z-index: 100;
   height: 50px;
   border: 1px solid white;
   transform: rotate(180deg);
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
