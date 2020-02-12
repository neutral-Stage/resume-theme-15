<template>
  <v-app>
    <v-row
      no-gutters
      justify="center"
      class="mt-10"
    >
      <v-col md="8">
        <v-tabs
          v-model="tab"
          background-color="transparent"
          color="#104EFB"
          center-active
          show-arrows
          grow
        >
          <v-tabs-slider style="height:0px;padding:0 0 !important;">
            <div class="tabid"></div>
          </v-tabs-slider>
          <v-tab
            v-for="item in items"
            :key="item.name"
            exact
            class="subtitle-1 text-capitalize "
            active-class="font-weight-bold"
          >
            {{ item.name }}

          </v-tab>
        </v-tabs>

        <v-row
          no-gutters
          class="mt-12"
        >
          <v-col md="12">
            <v-tabs-items
              v-model="tab"
              v-for="item in items"
              :key="item.name"
            >
              <v-tab-item
                v-for="(s,index) in item.skills"
                :key="index"
              >
                <v-row
                  class="justify-center py-2"
                  align="center"
                >
                  <v-col
                    cols="3"
                    sm="3"
                    md="1"
                  >
                    <v-img
                      :src="s.src"
                      width="38"
                      class="ml-6"
                    ></v-img>
                  </v-col>
                  <v-col
                    sm="7"
                    md="7"
                    cols="7"
                  >

                    <v-progress-linear
                      rounded
                      :value="s.per"
                      color="#104EFB"
                    ></v-progress-linear>
                  </v-col>

                </v-row>

              </v-tab-item>
            </v-tabs-items>
          </v-col>
        </v-row>

      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "skills",
  data() {
    return {
      tab: null,
      items: [
        {
          name: "Programming Languages",
          skills: [
            {
              src: "pic/php.svg",
              per: 67
            },
            {
              src: "pic/html.svg",
              per: 56
            },
            {
              src: "pic/css.svg",
              per: 78
            },
            {
              src: "pic/html.svg",
              per: 56
            },
            {
              src: "pic/js.svg",
              per: 86
            }
          ]
        },

        {
          name: "Frameworks/ Databases",
          skills: [
            {
              src: "pic/html.svg",
              per: 56
            },
            {
              src: "pic/css.svg",
              per: 78
            },
            {
              src: "pic/html.svg",
              per: 56
            },
            {
              src: "pic/js.svg",
              per: 86
            }
          ]
        },

        {
          name: "Design Skills",
          skills: [
            {
              src: "pic/php.svg",
              per: 67
            },
            {
              src: "pic/html.svg",
              per: 56
            },

            {
              src: "pic/html.svg",
              per: 56
            },
            {
              src: "pic/js.svg",
              per: 86
            }
          ]
        },

        {
          name: "Software",
          skills: [
            {
              src: "pic/php.svg",
              per: 67
            },

            {
              src: "pic/html.png",
              per: 56
            },
            {
              src: "pic/js.png",
              per: 86
            }
          ]
        }
      ],
      skills: [
        {
          src: "pic/php.png",
          per: 67
        },
        {
          src: "pic/html.png",
          per: 56
        },
        {
          src: "pic/css.png",
          per: 78
        },
        {
          src: "pic/html.png",
          per: 56
        },
        {
          src: "pic/js.png",
          per: 86
        }
      ]
    };
  }
};
</script>

<style scoped>
.v-tabs {
  position: relative;
}
.v-tabs:after {
  content: "";
  position: absolute;
  height: 1px;
  width: 90%;
  background-color: #104efb;

  margin: 0 50px 0 50px;
  bottom: 0;
}
.theme--light.v-application {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
}

.basil--text {
  color: #104efb !important;
}
</style>
