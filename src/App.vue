<template>
  <v-app>
    <!-- Top bar -->
    <v-toolbar flat>
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <v-spacer />
      <span>
        <b>EMPLOYEES</b> / PROFILES
      </span>
      <v-spacer />
      <v-btn depressed color="transparent" :ripple="false">Back</v-btn>
    </v-toolbar>

    <!-- Sidebar -->
    <v-navigation-drawer v-model="drawer" temporary app>
      <v-list>
        <v-list-item>
          <v-list-item-icon>
            <v-app-bar-nav-icon @click="drawer = !drawer" />
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title style="color: #2962FF;">INOGIT</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item v-for="(item, i) in dashboard_items1" :key="i" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider />

        <v-list-item v-for="(item, i) in dashboard_items2" :key="i" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: false,
    dashboard_items1: [
      { title: "Dashboard", icon: "mdi-view-dashboard" },
      { title: "Candidates", icon: "mdi-account-supervisor" },
      { title: "Jobs", icon: "mdi-briefcase" },
      { title: "Mailbox", icon: "mdi-message-text" },
      { title: "Settings", icon: "mdi-cog" }
    ],
    dashboard_items2: [
      { title: "Pools", icon: "mdi-waves" },
      { title: "Assessments", icon: "mdi-poll-box" },
      { title: "Team Members", icon: "mdi-google-circles-communities" },
      { title: "Billing", icon: "mdi-currency-usd" },
      { title: "Guidelines", icon: "mdi-clipboard-text" },
      { title: "Feedback", icon: "mdi-message-alert" },
      { title: "Contact Us", icon: "mdi-comment-question" }
    ]
  })
};
</script>
