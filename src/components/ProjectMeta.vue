<template>
  <div class="job-card-title">{{ title }}</div>

  <div class="explain-subtitle">{{ year }}</div>
  
    <ul class="project-categories">
      <li
        class="project-category"
        v-for="(category, index) in categories"
        :key="index"
      >
        {{ category }}
      </li>
    </ul>
   
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false
    },
    categories: {
      type: Array,
      required: false
    },
    year: {
      type: String,
      required: false
    }
  }
};
</script>

<style lang="scss" scoped>

</style>