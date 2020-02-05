<template>
    <v-app>
        <v-row no-gutters justify="center">
            <v-col md="8">
                    <v-tabs
                            v-model="tab"
                            background-color="transparent"
                            color="#104EFB"
                            grow
                    >
                        <v-tab
                                v-for="item in items"
                                :key="item.name"
                        >
                            {{ item.name }}
                        </v-tab>
                    </v-tabs>

                    <v-tabs-items v-model="tab" v-for="item in items"
                                  :key="item.name">
                        <v-tab-item
                                v-for="(s,index) in item.skills"
                                :key="index"

                        >
                            <v-row class="justify-center" align="center">
                                <v-col cols="2" sm="2" md="2">
                                    <v-img :src="s.src" width="64"></v-img>
                                </v-col>
                                <v-col sm="7" md="7" cols="7">

                                    <v-progress-linear rounded :value="s.per" color="#104EFB"></v-progress-linear>
                                </v-col>

                            </v-row>

                        </v-tab-item>
                    </v-tabs-items>

            </v-col>
        </v-row>
    </v-app>
</template>

<script>
    export default {
        name: "skills",
        data () {
            return {
                tab: null,
                items: [
                    {name:'Programming Languages',
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
                    },
                ]
                    },

                    {name:'Frameworks/ Databases',
                        skills: [

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
                    },
                ]
                    },

                    {name:'Design Skills',
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
                        src: "pic/html.png",
                        per: 56
                    },
                    {
                        src: "pic/js.png",
                        per: 86
                    },
                ]
                    },

                    {name:'Software',
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
                        src: "pic/js.png",
                        per: 86
                    },
                ]
                    },
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
                    },
                ]
            }
        },
    }
</script>

<style scoped>
    .theme--light.v-application {
        background: transparent;
        color: rgba(0,0,0,.87);
    }

    .basil--text {
        color: #104EFB !important;
    }
</style>
