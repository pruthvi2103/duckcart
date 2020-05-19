<template>
  <div>
    <v-card>
      <v-list-item-subtitle>
        <div class="subtitle-1 ma-2">Skills</div>
      </v-list-item-subtitle>
      <v-chip v-for="(names,id) in skills" :key="id" class="ma-1" color="blue lighten-4">{{ names }}</v-chip>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        "Python",
        "Web Development",
        "Java",
        "C++",
        "GO",
        "SQL",
        "Full-Stack Development",
        "Vuejs",
        "Linux"
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
</style>