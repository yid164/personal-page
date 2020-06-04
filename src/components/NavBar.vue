<template>
    <nav>
        <v-app-bar
                class="transparent"
                dark
                app>
            <v-app-bar-nav-icon @click="drawer = !drawer" class="black"></v-app-bar-nav-icon>
            <v-toolbar-title class="black--text carousel-transition-enter">Ken's Page</v-toolbar-title>
        </v-app-bar>
        <v-navigation-drawer
                v-model="drawer"
                class="transparent"
                app>
            <v-list>
                <v-col>
                    <v-list-item class="black--text">
                        <v-list-item-avatar color="red">
                            <span class="black--text headline">KD</span>
                        </v-list-item-avatar>
                        <v-list-item-content class="px-0">
                            <v-list-item-title class="title">
                                Ken Dong
                            </v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-spacer></v-spacer>

                    <v-list-item-group>
                        <v-list-item
                                v-for="(item, i) in items"
                                :key="i"
                                :to="item.route"
                        >
                            <v-list-item-icon>
                                <v-icon v-text="item.icon"></v-icon>
                            </v-list-item-icon>
                            <v-list-item-content>
                                <v-list-item-title v-text="item.text"></v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-item-group>
                </v-col>
            </v-list>

        </v-navigation-drawer>

    </nav>
</template>

<script>
    export default {
        name: "NavBar",
        data(){
            return{
                drawer: false,
                popSearch: false,
                items: [
                    {
                        icon: 'mdi-home',
                        text: 'HOME',
                        route: '/'
                    },
                    {
                        icon: 'mdi-inbox',
                        text: 'PORTFOLIO',
                        route: '/portfolio'
                    },
                    {
                        icon: 'mdi-star',
                        text: 'ABOUT',
                        route: '/about'
                    },
                    {
                        icon: 'mdi-blogger',
                        text: 'BLOG',
                        route: '/blog'
                    },
                    {
                        icon:'mdi-contacts-outline',
                        text: 'CONTACTS',
                        route: '/contacts'
                    }
                ],
                model: 1,
            }
        },
        methods:{
            popSearchBar(){
            }
        }
    }
</script>

<style scoped>
    .transparent {
        background-color: white!important;
        opacity: 0.65;
        border-color: transparent!important;
    }

</style>
