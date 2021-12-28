<template>
  <div>

  <div class="job-title-wrapper">
    <div class="job-card-title">{{ title }}</div>
    <div class="job-action">
      <svg class="heart" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M20.8 4.6a5.5 5.5 0 00-7.7 0l-1.1 1-1-1a5.5 5.5 0 00-7.8 7.8l1 1 7.8 7.8 7.8-7.7 1-1.1a5.5 5.5 0 000-7.8z"></path></svg>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-share-2"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><path d="M8.6 13.5l6.8 4M15.4 6.5l-6.8 4"></path></svg>
    </div>
  </div>
  <div class="job-subtitle-wrapper">
    <div class="company-name">Patreon <span class="comp-location">{{ location }}</span></div>
    <div class="posted">Posted 8 days ago<span class="app-number">98 Application</span></div>
  </div>

  <div class="explain-bar">
    <div class="explain-contents">
      <div class="explain-title">Experience</div>
      <div class="explain-subtitle">Minimum 1 Year</div>
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

  </div>

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

<style lang="css" scoped>
.job-card-title{font-weight:600;margin-top:16px;font-size:14px;}
.job-explain{background-color:var(--header-bg-color);border-radius:0 0 8px 8px;}
.job-bg{border-radius:8px 8px 0 0;-o-object-fit:cover;object-fit:cover;width:100%;height:180px;transition:0.3s;position:relative;}
.job-logos {
    margin-top: -50px;
    position: relative;
    margin-bottom: -36px;
    padding: 0 20px;
}
.job-logos svg{width:66px;padding:12px;background-color:#fff;border-radius:10px;border:4px solid var(--header-bg-color);}
.job-title-wrapper{display:flex;align-items:center;}
.job-title-wrapper .job-card-title{font-size:20px;margin-top:0;font-weight:600;}
.job-action{display:flex;align-items:center;margin-left:auto;}
.job-action svg{width:32px;border:1px solid var(--border-color);color:var(--subtitle-color);border-radius:8px;padding:6px;}
.job-action svg + svg{margin-left:12px;}
.job-explain-content{padding:50px 25px 30px;}
.job-subtitle-wrapper{display:flex;align-items:center;margin-top:20px;}
.job-subtitle-wrapper .posted{margin-left:auto;}
.job-subtitle-wrapper .company-name{color:var(--active-color);font-weight:600;font-size:14px;}
.job-subtitle-wrapper .comp-location,.job-subtitle-wrapper .posted{color:var(--subtitle-color);font-size:12px;font-weight:500;}
.job-subtitle-wrapper .comp-location{position:relative;margin-left:10px;}
.job-subtitle-wrapper .comp-location:before{content:"";width:3px;height:3px;border-radius:50%;background-color:var(--placeholder-color);top:49%;left:-8px;position:absolute;}
.job-subtitle-wrapper .app-number{color:var(--body-color);position:relative;margin-left:12px;}
.job-subtitle-wrapper .app-number:before{content:"";width:3px;height:3px;border-radius:50%;background-color:var(--placeholder-color);top:50%;left:-7px;position:absolute;}
.explain-bar {
  margin-top:20px;
  border:1px solid #fff;
  border-radius:8px;
  display:flex;
  height:66px;
  padding:0 16px;
  align-items:center;
  justify-content:space-between;
}
.explain-title{color:var(--subtitle-color);font-size:12px;line-height:40px;white-space:nowrap;}
.explain-subtitle{font-size:13px;font-weight:500;margin-top:-2px;white-space:nowrap;}
.explain-contents{height:66px;}
.explain-contents + .explain-contents{border-left:1px solid var(--border-color);padding-left:16px;}
.overview-text{margin-top:30px;}
.overview-text-header{font-weight:600;margin-bottom:25px;}
.overview-text-subheader{font-size:13px;line-height:2em;}
.overview-text-item + .overview-text-item{margin-top:20px;}
@media screen and (max-width: 990px){
.explain-contents,.explain-bar{height:auto;}
.explain-bar{flex-wrap:wrap;padding-bottom:14px;}
.explain-contents{width:50%;}
.explain-contents + .explain-contents{padding:0;border:0;}
.explain-contents:nth-child(2) ~ .explain-contents{margin-top:16px;border-top:1px solid var(--border-color);}
.job-subtitle-wrapper{flex-direction:column;align-items:flex-start;}
.job-subtitle-wrapper .posted{margin-left:0;margin-top:6px;}
}
@media screen and (max-width: 760px){
.job-explain{margin-left:0;}
}
@media screen and (max-width: 380px){
.explain-contents{width:100%;margin:0;}
.explain-contents:nth-child(2) ~ .explain-contents{margin:0;border:0;}
}
</style>