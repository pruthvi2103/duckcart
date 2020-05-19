<template>
  <div>
    <v-card class="mx-auto">
      <v-list>
        <v-header class="mx-4">Tasks</v-header>
        <template v-for="(item, index) in items">
          <v-divider v-if="item > 1" :key="index" :inset="item.inset"></v-divider>
          <v-list-item :key="index">
            <template>
              <v-checkbox :key="index"></v-checkbox>
              <v-list-item-content :key="index">
                <v-list-item-title>Add checkout button</v-list-item-title>
                <v-list-item-subtitle class="overline">
                  2MIN AGO &bull;
                  <v-icon size="12">mdi-calendar-blank</v-icon>DUE : 3:00 PM 02/05/2020
                </v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-avatar color="indigo" :key="index">
                <span class="white--text">KP</span>
              </v-list-item-avatar>
            </template>
          </v-list-item>
        </template>
      </v-list>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [1, 2, 3, 4, 5]
  })
};
</script>

<style lang="scss" scoped>
</style>