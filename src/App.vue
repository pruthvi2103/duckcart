  
<template>
  <v-app id="sandbox">
    <v-navigation-drawer v-model="primaryDrawer.model" app overflow>
      <v-list dense nav>
        <v-list-item>
          <v-app-bar-nav-icon
            v-if="primaryDrawer.model"
            @click.stop="primaryDrawer.model = !primaryDrawer.model"
          ></v-app-bar-nav-icon>
          <span class="blue--text">INOGIT</span>
        </v-list-item>
        <v-list-item></v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-account-multiple</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Candidates</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-briefcase</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Jobs</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-email</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Mailbox</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-brush</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-waves</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Pools</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-poll-box</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Assessments</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-kodi</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Team Members</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-currency-usd</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Billing</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar :clipped-left="primaryDrawer.clipped" dense flat color="white" app>
      <v-app-bar-nav-icon
        v-if="!primaryDrawer.model"
        @click.stop="primaryDrawer.model = !primaryDrawer.model"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>Vuetify</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container fluid>
        <v-row align="center" justify="center">
          <v-col cols="8">
            <v-row>
              <v-col cols="12">
                <ProfileHeader></ProfileHeader>
              </v-col>

              <Tabber></Tabber>
              <v-row>
                <v-col cols="12">
                  <InfoCard></InfoCard>
                </v-col>
                <v-col cols="12">
                  <ExpCard></ExpCard>
                </v-col>
                <v-col cols="6">
                  <EduCard></EduCard>
                </v-col>
                <v-col cols="6">
                  <SkillsCard></SkillsCard>
                </v-col>
              </v-row>
            </v-row>
          </v-col>
          <v-col cols="4">
            <v-row>
              <v-col cols="12">
                <SchCard></SchCard>
              </v-col>
              <v-col cols="12">
                <TnotesCard></TnotesCard>
              </v-col>
              <v-col cols="12">
                <TasksCard></TasksCard>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import SkillsCard from "./components/SkillsCard";
import TnotesCard from "./components/TnotesCard";
import TasksCard from "./components/TasksCard";
import InfoCard from "./components/InfoCard";
import EduCard from "./components/EduCard";
import SchCard from "./components/SchCard";
import ExpCard from "./components/ExpCard";
import Tabber from "./components/Tabber";
import ProfileHeader from "./components/ProfileHeader";
export default {
  components: {
    SkillsCard,
    TnotesCard,
    TasksCard,
    InfoCard,
    EduCard,
    SchCard,
    ExpCard,
    Tabber,
    ProfileHeader
  },
  data: () => ({
    drawers: ["Default (no property)", "Permanent", "Temporary"],
    primaryDrawer: {
      model: null,
      type: "default (no property)",
      clipped: false,
      floating: false,
      mini: false
    },
    footer: {
      inset: false
    }
  })
};
</script>