<template>
  <div class="job-card-title">{{ title }}</div>
  <div class="job-action">
        <svg class="heart" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M20.8 4.6a5.5 5.5 0 00-7.7 0l-1.1 1-1-1a5.5 5.5 0 00-7.8 7.8l1 1 7.8 7.8 7.8-7.7 1-1.1a5.5 5.5 0 000-7.8z"></path></svg>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-share-2"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><path d="M8.6 13.5l6.8 4M15.4 6.5l-6.8 4"></path></svg>
  </div>
  <section class="project-meta">
    <h2 class="project-title">{{ title }}</h2>
    <ul class="project-categories">
      <li
        class="project-category"
        v-for="(category, index) in categories"
        :key="index"
      >
        {{ category }}
      </li>
    </ul>
    <time class="project-year" :datetime="year">{{ year }}</time>
  </section>
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
.project-meta {
  display: flex;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  line-height: 1.5;
}
.project-title {
  flex: 0 0 40%;
  font-size: 1rem;
  font-weight: 500;
  margin: 0;
}
.project-categories {
  flex: 1;
  padding: 0;
  margin: 0;
  list-style: none;
}
.project-category {
  padding: 0;
  margin: 0;
}
.project-year {
  flex: 1;
  text-align: right;
}
</style>