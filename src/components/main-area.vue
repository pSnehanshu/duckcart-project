<template>
  <v-container>
    <v-row>
      <!-- Left side -->
      <v-col>
        <!-- User info -->
        <v-row>
          <v-col>
            <v-img :src="require('../assets/logo.svg')" class="my-3" contain height="200" />
          </v-col>
          <v-col>
            <h1>Kamal Pratap</h1>
            <p>Fullstack developer</p>
            <p>Last activity</p>
          </v-col>
        </v-row>

        <v-tabs v-model="current_tab">
          <v-tab v-for="tab in info_tabs" :key="tab.name">{{ tab.label }}</v-tab>
        </v-tabs>

        <v-tabs-items v-model="current_tab" class="mt-5">
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>
            <v-card outlined shaped>
              <v-card-title>Information</v-card-title>
              <v-simple-table>
                <tbody>
                  <tr>
                    <th>EMAIl</th>
                    <td>kamalpratap@xyz.com</td>
                  </tr>
                  <tr>
                    <th>PHONE</th>
                    <td>+919876543210</td>
                  </tr>
                  <tr>
                    <th>SOCIAL</th>
                    <td>github.com/kamalpratap</td>
                  </tr>
                  <tr>
                    <th>LINKS</th>
                    <td>
                      <div>codepen.io/kamal</div>
                      <div>yahoo.io/kamal</div>
                    </td>
                  </tr>
                </tbody>
              </v-simple-table>
            </v-card>
          </v-tab-item>
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>Empty</v-tab-item>
        </v-tabs-items>
      </v-col>

      <!-- Right sode -->
      <v-col></v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    current_tab: 1,
    info_tabs: [
      { name: "overview", label: "Overview" },
      { name: "activities", label: "Activities" },
      { name: "assessments", label: "Assessments" },
      { name: "files", label: "Files" },
      { name: "resume", label: "Resume" }
    ]
  })
};
</script>
