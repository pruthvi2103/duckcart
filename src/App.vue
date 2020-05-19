  
<template>
  <v-app id="sandbox">
    <v-navigation-drawer v-model="primaryDrawer.model" app overflow></v-navigation-drawer>

    <v-app-bar :clipped-left="primaryDrawer.clipped" dense flat color="white" app>
      <v-app-bar-nav-icon
        v-if="primaryDrawer.type !== 'permanent'"
        @click.stop="primaryDrawer.model = !primaryDrawer.model"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>Vuetify</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container fluid>
        <v-row align="center" justify="center">
          <v-col cols="6">
            <SkillsCard></SkillsCard>
          </v-col>
          <v-col cols="6">
            <TnotesCard></TnotesCard>
          </v-col>
          <v-col cols="6">
            <TasksCard></TasksCard>
          </v-col>
          <v-col cols="6">
            <InfoCard></InfoCard>
          </v-col>

          <v-col cols="6">
            <EduCard></EduCard>
          </v-col>
          <v-col cols="6">
            <SchCard></SchCard>
          </v-col>
          <v-col cols="6">
            <ExpCard></ExpCard>
          </v-col>
        </v-row>
      </v-container>
    </v-content>

    <v-footer :inset="footer.inset" app>
      <span class="px-4">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
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
export default {
  components: {
    SkillsCard,
    TnotesCard,
    TasksCard,
    InfoCard,
    EduCard,
    SchCard,
    ExpCard
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