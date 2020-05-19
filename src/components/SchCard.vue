<template>
  <div>
    <v-card class="mx-auto">
      <v-list>
        <v-header class="mx-4">Tasks</v-header>
        <template>
          <v-list-item>
            <template>
              <v-list-item-content>
                <v-list-item-title>
                  <v-row>
                    <v-col cols="3">Evaluation</v-col>
                    <v-col cols="2">
                      <div v-ripple>
                        <v-icon size="18" color="primary">mdi-calendar-blank</v-icon>
                        <span class="overline">SCHEDULE</span>
                      </div>
                    </v-col>
                    <v-col cols="1"></v-col>
                    <v-col cols="1">
                      <div v-ripple>
                        <v-icon size="18" color="black">mdi-share-variant</v-icon>
                      </div>
                    </v-col>
                    <v-col cols="1"></v-col>
                    <v-col cols="2">
                      <v-icon size="18" color="black">mdi-send</v-icon>
                    </v-col>
                    <v-col cols="2">
                      <span class="overline">MORE</span>
                    </v-col>
                  </v-row>
                </v-list-item-title>
              </v-list-item-content>
            </template>
          </v-list-item>

          <v-divider></v-divider>
          <v-list-item>
            <template>
              <v-list-item-content>
                <v-list-item-title>
                  <v-row>
                    <v-col cols="3">Job Name</v-col>
                    <v-col cols="3"></v-col>
                    <v-col cols="3">
                      <v-icon size="18" color="black">mdi-check</v-icon>
                      <span class="overline">Proceed</span>
                    </v-col>
                    <v-col cols="1">
                      <v-icon size="18" color="black">mdi-cancel</v-icon>
                    </v-col>
                    <v-col cols="2">
                      <v-icon size="24" color="black">mdi-dots-horizontal</v-icon>
                    </v-col>
                  </v-row>
                </v-list-item-title>
              </v-list-item-content>
            </template>
          </v-list-item>

          <v-divider></v-divider>
          <v-list-item>
            <template>
              <v-list-item-content>
                <v-list-item-title>
                  <v-row>
                    <v-col cols="3">Job Name</v-col>
                    <v-col cols="3"></v-col>
                    <v-col cols="2">
                      <div v-ripple>
                        <v-icon size="18" color="black">mdi-check</v-icon>
                        <span class="overline">Proceed</span>
                      </div>
                    </v-col>
                    <v-col cols="1"></v-col>
                    <v-col cols="1">
                      <v-icon size="18" color="black">mdi-cancel</v-icon>
                    </v-col>
                    <v-col cols="2">
                      <v-icon size="24" color="black">mdi-dots-horizontal</v-icon>
                    </v-col>
                  </v-row>
                </v-list-item-title>
              </v-list-item-content>
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