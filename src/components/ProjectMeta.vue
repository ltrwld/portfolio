<template>
<div class="job-title-wrapper">
  <div class="job-card-title">{{ title }}</div>
  <div class="job-action">
    <svg class="heart" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M20.8 4.6a5.5 5.5 0 00-7.7 0l-1.1 1-1-1a5.5 5.5 0 00-7.8 7.8l1 1 7.8 7.8 7.8-7.7 1-1.1a5.5 5.5 0 000-7.8z"></path>
    </svg>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-share-2"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><path d="M8.6 13.5l6.8 4M15.4 6.5l-6.8 4"></path></svg>
  </div>
</div>
<div class="job-subtitle-wrapper">
  <div class="company-name">Patreon <span class="comp-location">Londontowne, MD.</span></div>
  <div class="posted">Posted 8 days ago<span class="app-number">98 Application</span></div>
</div>
<div class="explain-bar">
        <div class="explain-contents">
        <div class="explain-title">Zeitraum</div>
        <div class="explain-subtitle">{{ year }}</div>
         </div>
        <div class="explain-contents">
        <div class="explain-title">Work Level</div>
        <div class="explain-subtitle">Senior level</div>
         </div>
        <div class="explain-contents">
        <div class="explain-title">Employee Type</div>
        <div class="explain-subtitle">Full Time Jobs</div>
         </div>
        <div class="explain-contents">
        <div class="explain-title">Offer Salary</div>
        <div class="explain-subtitle">$2150.0 / Month</div>
         </div>
</div>
<div class="overview-text">
        <div class="overview-text-header">Overview</div>
        <div class="overview-text-subheader" v-html="$page.project.content"></div>
       </div>
       <div class="overview-text">
        <div class="overview-text-header">Aufgaben</div>
        <div class="overview-text-item">3+ years working as a product designer.</div>
        <div class="overview-text-item">A portfolio that highlights your approach to problem solving, as well as you skills in UI.</div>
        <div class="overview-text-item">Experience conducting research and building out smooth flows.</div>
        <div class="overview-text-item">Excellent communication skills with a well-defined design process.</div>
        <div class="overview-text-item">Familiarity with design tools like Sketch and Figma</div>
        <div class="overview-text-item">Up-level our overall design and bring consistency to end-user facing properties</div>
</div>
  
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