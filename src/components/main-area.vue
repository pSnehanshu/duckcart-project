<template>
  <v-container fluid>
    <v-row>
      <!-- Left side -->
      <v-col cols="8">
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

        <v-tabs fixed-tabs v-model="current_tab">
          <v-tab v-for="tab in info_tabs" :key="tab.name">{{ tab.label }}</v-tab>
        </v-tabs>

        <v-tabs-items v-model="current_tab" class="mt-5">
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>
            <v-card outlined>
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

            <v-card outlined class="mt-4">
              <v-card-title>Experience</v-card-title>
              <v-card-text>
                <div>
                  <h2>Lead Designer</h2>
                  <div>Google, Inc.</div>
                  <div>Sep 2019 - Dec 2019</div>
                  <p>During my internship, I developed UI and UX for an android app called Google Keep. I completely Re-Designed the application.</p>
                </div>
              </v-card-text>
            </v-card>

            <v-row>
              <v-col>
                <v-card outlined>
                  <v-card-title>Education</v-card-title>
                  <v-card-text>
                    <div>
                      <h2>SSC</h2>
                      <div>St. Mary High School</div>
                      <div>Sep 2016</div>
                      <div>CGPA- 9.2</div>
                    </div>
                    <div class="mt-3">
                      <h2>Higher Secondary</h2>
                      <div>St. Mary High School</div>
                      <div>Sep 2018</div>
                      <div>Percentage- 96.5%</div>
                    </div>
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col>
                <v-card outlined>
                  <v-card-title>Skills</v-card-title>
                  <v-card-text>
                    <v-chip v-for="(skill, i) in skills" :key="i" class="mr-2 mt-2">{{skill}}</v-chip>
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </v-tab-item>
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>Empty</v-tab-item>
          <v-tab-item>Empty</v-tab-item>
        </v-tabs-items>
      </v-col>

      <!-- Right sode -->
      <v-col cols="4">
        <v-card outlined>
          <v-list>
            <v-list-item>
              <v-list-item-content>Evaluation</v-list-item-content>
              <div class="d-flex">
                <v-btn depressed color="transparent">
                  <v-icon left>mdi-calendar-blank</v-icon>Schedule
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-share-variant</v-icon>
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-send</v-icon>
                </v-btn>
                <v-btn depressed color="transparent">More</v-btn>
              </div>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>Job Name</v-list-item-content>
              <div class="d-flex">
                <v-btn depressed color="transparent">
                  <v-icon left>mdi-check</v-icon>Proceed
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-cancel</v-icon>
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-dots-horizontal</v-icon>
                </v-btn>
              </div>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>Pool Name</v-list-item-content>
              <div class="d-flex">
                <v-btn depressed color="transparent">
                  <v-icon left>mdi-check</v-icon>Proceed
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-cancel</v-icon>
                </v-btn>
                <v-btn icon>
                  <v-icon>mdi-dots-horizontal</v-icon>
                </v-btn>
              </div>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
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
    ],
    skills: [
      "Python",
      "Web Development",
      "CSS",
      "Web Development",
      "Python",
      "CSS",
      "Web Development",
      "CSS",
      "Python",
      "Python",
      "CSS",
      "Web Development",
      "Python",
      "Web Development",
      "CSS"
    ]
  })
};
</script>
