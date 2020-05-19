<template>
  <div>
    <v-card class="mx-auto">
      <v-list one-line>
        <template v-for="(item, index) in items">
          <v-header v-if="item.header" :key="item.header" v-text="item.header" class="mx-4">
            <v-spacer></v-spacer>
          </v-header>

          <v-divider v-else-if="item.divider" :key="index" :inset="item.inset"></v-divider>

          <v-list-item v-else :key="item.name">
            <v-list-item-avatar color="indigo">
              <span class="white--text">KP</span>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>
                {{item.name}} &bull;
                <span class="caption grey--text">2:30PM</span>
                <br />
                <span class="subtitle-2 grey--text">{{item.subtitle}}</span>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </template>
      </v-list>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      { header: "Team Notes" },
      {
        name: "Kamal Pratap",
        subtitle: "I have pushed my progress to the master branch"
      },
      { divider: true, inset: true },
      {
        name: "Kamal Pratap",
        subtitle: "I have pushed my progress to the master branch"
      },
      { divider: true, inset: true },
      {
        name: "Kamal Pratap",
        subtitle: "I have pushed my progress to the master branch"
      },
      { divider: true, inset: true },
      {
        name: "Kamal Pratap",
        subtitle: "I have pushed my progress to the master branch"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
</style>