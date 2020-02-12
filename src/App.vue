<template>
  <v-app>
    <section>
      <v-row
        justify="center"
        align="center"
        class="backdesign"
      >
        <v-col
          md="6"
          lg="=6"
          cols="12"
        >
          <v-row
            justify="center"
            align="center"
            no-gutters
          >
            <v-col
              md="2"
              lg="2"
              cols="3"
              sm="3"
              class="d-flex flex-column align-center"
            >
              <v-avatar
                class="profile  hidden-sm-and-down"
                size="100"
              >
                <img
                  src="/pic/avatar.svg"
                  alt="John"
                />
              </v-avatar>
              <v-avatar
                class="profile ma-auto hidden-md-and-up"
                size="100"
              >
                <img
                  src="/pic/avatar.svg"
                  alt="John"
                />
              </v-avatar>
            </v-col>
            <v-col
              md="4"
              lg="4"
              cols="6"
              sm="9"
              class="detail"
            >

              <div class="headline white--text ">Jennifer lopez</div>
              <div class="subtitle-1 white--text">Web Designer</div>
              <v-row
                class="hidden-sm-and-down mt-2"
                no-gutters
              >
                <v-col
                  lg="2"
                  md="2"
                  v-for="icon in icons"
                  :key="icon.name"
                >

                  <v-img
                    color="white"
                    :src="icon.name"
                    :width="icon.size"
                    :height="icon.size"
                    contain
                  ></v-img>
                </v-col>
              </v-row>
              <v-btn
                outlined
                fab
                x-small
                v-for="(icon, index) in media"
                :key="index"
                color="white"
                class="mr-3 hidden-md-and-up"
              >
                <v-img
                  :src="icon"
                  width="16"
                  height="16"
                  contain
                ></v-img>
              </v-btn>
            </v-col>
            <v-row
              no-gutters
              class="hidden-md-and-up mt-12 pl-10"
              align="end"
              justify="end"
            >
              <v-img
                v-for="icon in iconsmob"
                :key="icon.name"
                :src="icon.name"
                :width="icon.size"
                :height="icon.size"
                contain
              ></v-img>
            </v-row>
            <v-col
              md="3"
              cols="6"
              class="hidden-sm-and-down"
            >
              <v-btn
                outlined
                fab
                small
                v-for="(icon, index) in media"
                :key="index"
                color="white"
                class="mr-3"
              >
                <v-img
                  :src="icon"
                  width="16"
                  height="16"
                  contain
                ></v-img>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col
          md="6"
          lg="6"
          class="hidden-sm-and-down"
        >
          <v-row
            no-gutters
            justify="center"
            align="center"
          >
            <v-col
              md="8"
              class="blade"
            >
              <v-row
                no-gutters
                justify="center"
                align="center"
                class="mt-4 mr-8"
              >
                <v-col
                  md="3"
                  class="index line mt-3"
                >
                  <h2 class="point text-center font-weight-bold textcol">
                    $10
                  </h2>
                  <h2 class="subpoint text-center textcol">hourly rate</h2>
                </v-col>
                <v-col
                  md="3"
                  class="index mx-2 mt-3"
                >
                  <h2 class="point text-center font-weight-bold textcol ">
                    35 HOURS
                  </h2>
                  <h2 class="subpoint text-center textcol">
                    weekly availability
                  </h2>
                </v-col>
                <v-col
                  md="4"
                  class="index text-center pl-4"
                >
                  <v-btn
                    color="#104EFB"
                    width="180"
                    height="60"
                    style="border-radius:300px"
                    class="white--text but"
                    elevation="4"
                  >
                    HIRE ME
                  </v-btn>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>

        <v-col
          cols="12"
          sm="12"
          class="hidden-md-and-up"
        >
          <v-row
            no-gutters
            justify="center"
          >
            <v-col
              md="8"
              class="blademob"
            >
              <v-row
                no-gutters
                justify="center"
                class="mt-6 mr-3"
              >
                <v-col
                  sm="6"
                  cols="6"
                  class="index linemob"
                >
                  <h2 class="subtitle-2 text-center font-weight-bold white--text">
                    10$
                  </h2>
                  <h2 class="caption text-center white--text">hourly rate</h2>
                </v-col>
                <v-col
                  sm="6"
                  cols="6"
                  class="index"
                >
                  <h2 class="subtitle-2 text-center font-weight-bold white--text">
                    35 HOURS
                  </h2>
                  <h2 class="caption text-center white--text">
                    weekly availability
                  </h2>
                </v-col>
              </v-row>
              <v-col
                cols="12"
                sm="12"
                class="index mt-12 text-center"
              >
                <v-btn
                  color="#104EFB"
                  x-large
                  elevation="4"
                  class="white--text"
                  width="265"
                  height="84"
                  style="border-radius:300px"
                >
                  HIRE ME
                </v-btn>
              </v-col>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row
        justify="center"
        align="center"
        class="marg"
      >

        <v-col
          md="8"
          cols="12"
        >

          <v-tabs
            v-model="tabmob"
            center-active
            show-arrows
            color="#104efb"
            grow
          >
            <v-tabs-slider class="slider"></v-tabs-slider>

            <v-tab
              v-for="i in tabs"
              :key="i.name"
              :to="i.link"
              exact
            >
              <div class="title text-capitalize">{{ i.name }}</div>

            </v-tab>

          </v-tabs>

        </v-col>
      </v-row>
      <v-row
        no-gutters
        justify="center"
      >
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
      tabmob: null,
      icons: [
        { name: "/pic/behance.svg", size: 18 },
        { name: "/pic/dribbble.svg", size: 16 },
        { name: "/pic/pinterest.svg", size: 16 },
        { name: "/pic/instagram.svg", size: 16 },
        { name: "/pic/linkedin.svg", size: 16 }
      ],
      iconsmob: [
        { name: "/pic/behance_2.svg", size: 18 },
        { name: "/pic/dribbble_2.svg", size: 16 },
        { name: "/pic/pinterest_2.svg", size: 16 },
        { name: "/pic/instagram_2.svg", size: 16 },
        { name: "/pic/linkedin_2.svg", size: 16 }
      ],
      media: ["/pic/message.svg", "/pic/audio.svg", "/pic/video.svg"],
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

<style >
.point {
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 15px;
}
.subpoint {
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 12px;
  line-height: 18px;
}
.v-tabs-slider-wrapper {
  height: 3px !important;
  padding: 0 100px !important;
  left: 0;
  opacity: 0.6;
}
.v-tab:not(.v-tab--active) {
  color: #104efb !important;
  opacity: 0.4 !important;
}

.cls-1 {
  fill: #104efb;
}
.textcol {
  color: #104efb !important;
}
section {
  position: relative;
  margin: 0;
  padding: 0;
  background: url("/pic/curve.svg");
  background-repeat: no-repeat;
  background-size: contain;
  width: 100%;
}
/* .backdesign:after {
  content: "";
  position: absolute;
  width: 100%;
  height: 280px;
  background: url("/pic/backdesign.png");
  background-repeat: repeat-y;
  background-size: cover;
  background-position: top;
} */
.marg {
  margin-top: 80px;
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
  .detail {
    margin-left: 24px !important;
  }
  .marg {
    margin-top: 30px !important;
  }
  .v-tabs-slider-wrapper {
    height: 3px !important;
    padding: 0 5px !important;
    left: 0;
    opacity: 0.6;
  }
}
@media screen and (max-width: 1360px) {
  .but {
    width: 150px !important;
  }
}
@media only screen and (max-width: 1000px) and (min-width: 650px) {
  .v-tabs-slider-wrapper {
    height: 3px !important;
    padding: 0 50px !important;
    left: 0;
    opacity: 0.6;
  }
  .but {
    width: 100px;
  }
  section {
    position: relative;
    margin: 0;
    padding: 0;
    top: 0;
    background: url("/pic/curvedtab.svg");
    background-repeat: no-repeat;
    background-size: contain;
  }
  .backdesign:after {
    content: "";
    position: absolute;
    width: 100%;
    height: 200px;
    top: 0;
    background: url("/pic/backdesign.png");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: top;
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
#curvemob {
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
  position: absolute;
  opacity: 0.44;
  width: 1px;
  top: -15px;
  right: 0;
  z-index: 100;
  height: 60px;
  border: 1px solid rgba(16, 78, 251, 0.3);
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
  top: 0px;
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
