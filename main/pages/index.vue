<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card max-width="600" class="mx-auto">
        <v-toolbar color="light-blue" dark>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>

          <v-toolbar-title>CMUDEVDAY2022_POC_Micro_Frontend</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-view-module</v-icon>
          </v-btn>
        </v-toolbar>

        <v-list subheader two-line>
          <v-subheader inset>Main</v-subheader>

          <v-list-item v-for="file in mains" :key="file.title" :to="file.link">
            <v-list-item-avatar>
              <v-icon :class="file.color" dark v-text="file.icon"></v-icon>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title v-text="file.title"></v-list-item-title>

              <v-list-item-subtitle
                v-text="file.subtitle"
              ></v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-action>
              <v-btn icon>
                <v-icon color="grey lighten-1">mdi-information</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>

          <v-divider inset></v-divider>

          <v-subheader inset>App1</v-subheader>

          <v-list-item
            v-for="file in app1s"
            :key="file.title"
            @click="menuActionClick(file.link)"
          >
            <v-list-item-avatar>
              <v-icon :class="file.color" dark v-text="file.icon"></v-icon>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title v-text="file.title"></v-list-item-title>

              <v-list-item-subtitle
                v-text="file.subtitle"
              ></v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-action>
              <v-btn icon>
                <v-icon color="grey lighten-1">mdi-information</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>
          <v-divider inset></v-divider>

          <v-subheader inset>App2</v-subheader>

          <v-list-item
            v-for="file in app2s"
            :key="file.title"
            @click="menuActionClick(file.link)"
          >
            <v-list-item-avatar>
              <v-icon :class="file.color" dark v-text="file.icon"></v-icon>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title v-text="file.title"></v-list-item-title>

              <v-list-item-subtitle
                v-text="file.subtitle"
              ></v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-action>
              <v-btn icon>
                <v-icon color="grey lighten-1">mdi-information</v-icon>
              </v-btn>
            </v-list-item-action>
          </v-list-item>
        </v-list>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      mains: [
        {
          color: 'blue',
          icon: 'mdi-clipboard-text',
          subtitle: 'link to /',
          title: 'Portal',
          link: '/',
        },
        {
          color: 'amber',
          icon: 'mdi-gesture-tap-button',
          subtitle: 'link to /inspire/',
          title: 'main : inspire',
          link: '/inspire/',
        },
      ],
      app1s: [
        {
          color: 'blue',
          icon: 'mdi-clipboard-text',
          subtitle: 'link to /App1/',
          title: 'App1 : index',
          link: '/App1/',
        },
        {
          color: 'amber',
          icon: 'mdi-gesture-tap-button',
          subtitle: 'link to /App1/inspire/',
          title: 'App1 : inspire',
          link: '/App1/inspire/',
        },
      ],
      app2s: [
        {
          color: 'blue',
          icon: 'mdi-clipboard-text',
          subtitle: 'link to /App2/',
          title: 'App2 : index',
          link: '/App2/',
        },
        {
          color: 'amber',
          icon: 'mdi-gesture-tap-button',
          subtitle: 'link to /App2/inspire/',
          title: 'App2 : inspire',
          link: '/App2/inspire/',
        },
      ],
    }
  },
  methods: {
    menuActionClick(action) {
      window.location.href = 'http://localhost' + action
    },
  },
}
</script>
