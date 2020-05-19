<template>
  <div>
    <v-card class="mx-auto">
      <v-list>
        <v-header class="mx-4">Tasks</v-header>
        <template>
          <v-divider></v-divider>
          <v-list-item>
            <template>
              <v-list-item-content>
                <v-list-item-title>Evaluation</v-list-item-title>
                <v-list-item-subtitle class="overline">
                  2MIN AGO &bull;
                  <v-icon size="12">mdi-calendar-blank</v-icon>DUE : 3:00 PM 02/05/2020
                </v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-avatar color="indigo">
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
export default {};
</script>

<style lang="scss" scoped>
</style>