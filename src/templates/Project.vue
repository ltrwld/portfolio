<template>
  <Layout :title="$page.project.title">
    <article class="project-post">
      <g-image
        class="thumnail"
        :src="$page.project.thumbnail"
        :alt="$page.project.title"
      />
      <ProjectMeta
        :title="$page.project.title"
        :categories="$page.project.categories"
        :year="$page.project.year"
      />
      <div class="content" v-html="$page.project.content" />
    </article>











<div class="job-explain">
      <img class="job-bg" alt="" src="https://unsplash.it/640/425?image=1" style="background: rgb(46, 40, 130);">
      <div class="job-logos"><svg viewBox="0 -13 512 512" xmlns="http://www.w3.org/2000/svg" style="background-color:#2e2882">
        <g fill="#feb0a5">
         <path d="M256 92.5l127.7 91.6L512 92 383.7 0 256 91.5 128.3 0 0 92l128.3 92zm0 0M256 275.9l-127.7-91.5L0 276.4l128.3 92L256 277l127.7 91.5 128.3-92-128.3-92zm0 0"></path>
         <path d="M127.7 394.1l128.4 92 128.3-92-128.3-92zm0 0"></path>
        </g>
        <path d="M512 92L383.7 0 256 91.5v1l127.7 91.6zm0 0M512 276.4l-128.3-92L256 275.9v1l127.7 91.5zm0 0M256 486.1l128.4-92-128.3-92zm0 0" fill="#feb0a5"></path>
       </svg></div>
      <div class="job-explain-content">
      <div class="job-title-wrapper">
       <div class="job-card-title">UI / UX Designer</div>
       <div class="job-action">
        <svg class="heart" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M20.8 4.6a5.5 5.5 0 00-7.7 0l-1.1 1-1-1a5.5 5.5 0 00-7.8 7.8l1 1 7.8 7.8 7.8-7.7 1-1.1a5.5 5.5 0 000-7.8z"></path></svg>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-share-2"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><path d="M8.6 13.5l6.8 4M15.4 6.5l-6.8 4"></path></svg>
       </div>
       </div>
       <div class="job-subtitle-wrapper">
        <div class="company-name">Patreon <span class="comp-location">Londontowne, MD.</span></div>
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
       <div class="overview-text">
        <div class="overview-text-header">Overview</div>
        <div class="overview-text-subheader">We believe that design (and you) will be critical to the company's success. You will work with our founders and our early customers to help define and build our product functionality, while maintaining the quality bar that customers have come to expect from modern SaaS applications. You have a strong background in product design with a quantitavely anf qualitatively analytical mindset. You will also have the opportunity to craft our overall product and visual identity and should be comfortable to flex into working.</div>
       </div>
       <div class="overview-text">
        <div class="overview-text-header">Job Description</div>
        <div class="overview-text-item">3+ years working as a product designer.</div>
        <div class="overview-text-item">A portfolio that highlights your approach to problem solving, as well as you skills in UI.</div>
        <div class="overview-text-item">Experience conducting research and building out smooth flows.</div>
        <div class="overview-text-item">Excellent communication skills with a well-defined design process.</div>
        <div class="overview-text-item">Familiarity with design tools like Sketch and Figma</div>
        <div class="overview-text-item">Up-level our overall design and bring consistency to end-user facing properties</div>
       </div>
      </div>
     </div>



  </Layout>
</template>

<page-query>
query Project ($path: String!) {
  project: project(path: $path) {
    title
    thumbnail
    year
    categories
    content
  }
}
</page-query>

<script>
import ProjectMeta from "@/components/ProjectMeta";

export default {
  components: {
    ProjectMeta
  },
  mounted() {
    // Instead of checking for firstChild nodes that is text elements,
    // check and see if the p tags only contains img elements and that noscript
    // generated by Gridsome.
    const contentElements = document.querySelectorAll("p");
    contentElements.forEach(
      element =>
        element.firstChild.nodeName === "#text" &&
        element.classList.add("content-text")
    );
  }
};
</script>

<style lang="scss">
.project-post {
  padding: 0 2rem;
  margin-bottom: 8rem;
}
img {
  width: 100% !important;
  margin-bottom: 2rem;
  border-radius: 10px;
}
p {
  margin: 0;
}
.content-text {
  padding: 4rem 0 6rem 0;
  font-size: 2rem;
  font-weight: 400;
  margin-left: 0;
  max-width: 780px;
  line-height: 1.5;
  @media (min-width: 920px) {
    margin-left: 40%;
  }
}




























/*! CSS Used from: https://cpwebassets.codepen.io/assets/global/global-287e19e0385dcda82839437227412a58ee4d27c64c582021f54dcac3cc8b2d9c.css ; media=all */
@media all{
h1,h2,h3,h4,h5{line-height:1.2;margin:0 0 10px;font-weight:400;}
h2,h3,h4,h5{font-family:var(--cp-font-family);}
h1{-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;font-family:var(--cp-font-family-header);line-height:1.1;font-size:3rem;}
@media (max-width:550px){
h1{font-size:2.2rem;}
}
h2{font-family:var(--cp-font-family-header-alt);font-size:1.8rem;}
h3{font-size:1.4rem;font-weight:700;}
h4{font-size:1.2rem;font-weight:700;text-transform:uppercase;}
h5{font-weight:700;text-transform:uppercase;}
p,pre{margin:0 0 1em;}
p:empty,pre:empty{display:none;}
a{text-decoration:none;color:var(--cp-color-link);}
a:hover,a:focus,a:active{cursor:pointer;color:#fff;}
*{margin:0;padding:0;-webkit-box-sizing:border-box;box-sizing:border-box;}
body{min-height:100%;}
img,a img{outline:0;border:0;}
img{max-width:100%;height:auto;}
input[type=text],input[type=tel],textarea{font-family:var(--cp-font-family);font-size:13px;-webkit-appearance:none;padding:4px 5px;outline:0;background:var(--cp-color-5);border:3px solid var(--cp-color-5);border-radius:3px;}
input[type=text]:focus,input[type=tel]:focus,textarea:focus{border-color:var(--cp-color-11);background:var(--cp-color-1);}
label[for],input[type=checkbox],input[type=radio]{cursor:pointer;}
.page-wrap{position:relative;padding:20px 20px 50px;}
.screen-reader-text{position:absolute;top:-9999px;left:-9999px;}
.visually-hidden{position:absolute!important;top:-9999px;left:-9999px;}
textarea:focus,textarea:active{outline:0;}
@media (min-width:831px){
body{position:relative;height:auto;min-height:100vh;}
}
.sidebar-false .main-header{background:var(--cp-color-19);height:var(--cp-header-height);}
@media (max-width:830px){
.sidebar-false .main-header{height:var(--cp-header-height-small);}
}
.sidebar-false .main-header .navigation-wrap{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;-webkit-flex-shrink:0;-ms-flex-negative:0;flex-shrink:0;}
.editor-actions-menu{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;}
.editor-actions-menu .toggle-actions-button{display:none;position:relative;}
@media (max-width:767px),(max-height:440px){
.editor-actions-menu .toggle-actions-button{display:block;}
}
.editor-actions{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;}
@media (max-width:767px),(max-height:440px){
.editor-actions{display:block;position:absolute;z-index:400;top:100%;right:0;width:225px;max-height:75vh;padding:.5rem 0;overflow:hidden;overflow-y:auto;background:var(--cp-color-16);-webkit-box-shadow:0 2rem 4rem var(--cp-color-18);box-shadow:0 2rem 4rem var(--cp-color-18);opacity:0;visibility:hidden;-webkit-transform:scale(.9);transform:scale(.9);-webkit-transform-origin:top right;transform-origin:top right;-webkit-transition:all .2s ease-in-out,visibility 0s linear .2s;transition:all .2s ease-in-out,visibility 0s linear .2s;}
.editor-actions::-webkit-scrollbar{width:.5em;height:.5em;}
.editor-actions::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.editor-actions::-webkit-scrollbar-track{background:var(--cp-color-5);}
.editor-actions>button{line-height:1.4;display:block;background:0 0;border:none;border-radius:0;margin:0 0 .25rem;font-weight:700!important;width:100%;text-align:left;}
}
.site-footer{font-family:var(--cp-font-family);height:30px;line-height:1;position:fixed;width:100%;bottom:0;left:0;padding:0 5px;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;-webkit-box-pack:justify;-webkit-justify-content:space-between;-ms-flex-pack:justify;justify-content:space-between;white-space:nowrap;color:var(--cp-color-9);background:var(--cp-color-14);border-top:1px solid var(--cp-color-13);z-index:10;font-size:1rem;}
.footer-left{-webkit-box-flex:0;-webkit-flex:0 1 auto;-ms-flex:0 1 auto;flex:0 1 auto;height:100%;padding:9px 0;z-index:1;}
@media (min-width:551px){
.footer-left{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;}
}
.footer-right{-webkit-box-flex:1;-webkit-flex:1 1 auto;-ms-flex:1 1 auto;flex:1 1 auto;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;-webkit-box-pack:end;-webkit-justify-content:flex-end;-ms-flex-pack:end;justify-content:flex-end;}
@media (max-width:610px){
.footer-right{position:relative;padding-left:5px;}
}
@media (max-width:610px){
.editor-footer .footer-right{position:absolute;right:5px;padding-left:0;}
}
.button.zoom-select{display:none;}
@media (max-width:767px),(max-height:440px){
.button.zoom-select{display:inline-block;}
}
.footer-actions-menu .toggle-footer-menu-button{display:none;}
.footer-actions-menu .footer-actions{display:-webkit-inline-box;display:-webkit-inline-flex;display:-ms-inline-flexbox;display:inline-flex;}
@media (max-width:550px){
.footer-actions-menu .toggle-footer-menu-button{display:inline-block;padding:0 16px;}
.footer-actions-menu .toggle-footer-menu-button svg{-webkit-transform:rotate(180deg);transform:rotate(180deg);-webkit-transition:.2s -webkit-transform;transition:.2s -webkit-transform;transition:.2s transform;transition:.2s transform,.2s -webkit-transform;}
.footer-actions-menu .footer-actions{display:block;position:absolute;left:0;bottom:100%;z-index:400;width:100%;padding:10px;-webkit-box-sizing:border-box;box-sizing:border-box;overflow:hidden;background:var(--cp-color-16);opacity:0;visibility:hidden;-webkit-transform:scale(.9);transform:scale(.9);-webkit-transform-origin:bottom left;transform-origin:bottom left;-webkit-transition:all .2s ease-in-out,visibility 0s linear .2s;transition:all .2s ease-in-out,visibility 0s linear .2s;}
}
textarea.is-code{font-family:Monaco,Courier,MonoSpace;line-height:2;}
label.small-inline{font-size:.8em;display:inline-block!important;margin-right:3px;}
.top-label-form label{font-weight:400;display:block;margin:0 0 3px;letter-spacing:.5px;}
.top-label-form input[type=text],.top-label-form textarea{padding:10px;width:100%;}
.top-label-form select{background:var(--cp-color-6);}
.normal-labels label{text-transform:none;letter-spacing:0;}
.selected{color:var(--cp-color-link);}
.ios-toggle-mega-label-wrap{display:inline-block;position:relative;white-space:nowrap;}
.ios-toggle-mega-label{position:absolute;position:absolute;top:0;left:0;width:100%;height:100%;}
.ios-toggle>input:active+label::before,.ios-toggle>input:checked+label::before{width:60%;left:20%;top:30%;height:40%;opacity:0;}
.ios-toggle{position:relative;display:inline-block;width:2.975em;height:1.75em;border-radius:1.75em;background:var(--cp-color-7);vertical-align:middle;margin:0 .5rem;}
.ios-toggle>input{-webkit-appearance:none;-moz-appearance:none;appearance:none;opacity:0;width:100%!important;height:100%;position:absolute!important;}
.ios-toggle>input:checked+label{background:var(--cp-color-9);}
.ios-toggle>input:checked+label::after{right:0;left:1.225em;}
.ios-toggle>input:active+label::after{right:.875em;left:0;}
.ios-toggle>input:active:checked+label::after{right:0;left:.875em;}
.ios-toggle>label:not(.ios-toggle-mega-label){display:block!important;width:100%!important;height:100%;border-radius:1.75em;-webkit-transition:background .125s;transition:background .125s;}
.ios-toggle>label:not(.ios-toggle-mega-label)::before,.ios-toggle>label:not(.ios-toggle-mega-label)::after{position:absolute;content:'';top:0;left:0;height:1.75em;border-radius:inherit;-webkit-transition:all .2s;transition:all .2s;}
.ios-toggle>label:not(.ios-toggle-mega-label)::before{background:var(--cp-color-green);width:100%;}
.ios-toggle>label:not(.ios-toggle-mega-label)::after{background:var(--cp-color-1);-webkit-transform:scale(1.1);transform:scale(1.1);right:1.225em;}
.ios-toggle.ios-toggle-reverse>input:checked+label{background:var(--cp-color-green);}
.ios-toggle.ios-toggle-reverse>label::before{background:var(--cp-color-9);}
.normal-labels label{font-weight:inherit;text-transform:inherit;letter-spacing:inherit;color:inherit;}
.resource-search-bar{border-radius:6px;position:relative;background:var(--cp-color-4);border:none;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-flex-wrap:wrap;-ms-flex-wrap:wrap;flex-wrap:wrap;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;margin:0!important;}
.resource-search-bar .icon-mag{width:18px;height:18px;fill:#535557;margin-left:.75rem;}
.resource-search-bar input[type=text]{width:100%;border:0;color:var(--cp-color-13);font-size:1rem;background:0 0;padding:1rem;}
.custom-select-wrap{border-radius:3px;position:relative;z-index:1;height:42px;background:var(--cp-color-1);}
.custom-select-wrap select{z-index:0;position:relative;-webkit-appearance:none;-moz-appearance:none;appearance:none;width:100%;border:none;cursor:pointer;padding:0 24px 0 12px;height:42px;line-height:42px;font-size:1.1rem;color:var(--cp-color-12);background:0 0;}
.custom-select-wrap .select-icon{z-index:1;padding:1px;position:absolute;width:18px;height:18px;right:6px;top:12px;pointer-events:none;}
.custom-select-wrap .select-icon svg{width:14px;height:30px;position:absolute;fill:var(--cp-color-12);padding:1px;}
.custom-select-wrap .select-icon svg:first-child{-webkit-transform:rotate(180deg);transform:rotate(180deg);top:-10px;}
.align-right{text-align:right;}
.rotate-cc90{-webkit-transform:rotate(-90deg);transform:rotate(-90deg);}
.rotate-c90{-webkit-transform:rotate(90deg);transform:rotate(90deg);}
.fullwidth{width:100%;}
.hide{display:none!important;}
.group::before,.group::after{content:'';display:table;}
.group::after{clear:both;}
.user-avatar{border-radius:4px;}
button{font-family:inherit;}
.button{font-family:var(--cp-font-family);-webkit-appearance:none;display:-webkit-inline-box;display:-webkit-inline-flex;display:-ms-inline-flexbox;display:inline-flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;vertical-align:middle;position:relative;font-family:inherit;font-size:1rem;text-shadow:none;line-height:1.2;white-space:nowrap;text-overflow:ellipsis;text-decoration:none!important;font-weight:400!important;cursor:pointer;background:var(--cp-button-bg);color:var(--cp-button-color);padding:var(--cp-button-padding);margin:var(--cp-button-margin);border-radius:var(--cp-button-border-radius);border:var(--cp-button-border-width) solid transparent;--cp-button-padding:var(--cp-button-padding-block)     var(--cp-button-padding-inline);--cp-button-margin:var(--cp-button-margin-block)     var(--cp-button-margin-inline) var(--cp-button-margin-block) 0;}
.button:hover,.button:focus{background:var(--cp-button-hover-bg,var(--cp-button-bg))!important;color:var(--cp-button-hover-color,var(--cp-button-color))!important;outline-offset:3px;}
.button:hover svg,.button:focus svg{fill:var(--cp-button-hover-icon,var(--cp-button-icon));}
.button::-moz-focus-inner{border:0;padding:0;}
.button:active{-webkit-transform:translateY(1px);transform:translateY(1px);}
.button>svg{width:16px;height:16px;display:inline-block;pointer-events:none;vertical-align:bottom;fill:var(--cp-button-icon);}
.button.green{--cp-button-bg:var(--cp-color-green);--cp-button-color:black;--cp-button-hover-bg:var(--cp-color-green-dark);}
button.invisible-button{border:0;background:0 0;}
.button-no-right-margin{margin-right:0;}
.mini-button{font-size:.8rem;padding:2px 7px;margin:0 3px 0 0;border-width:1px;border-radius:2px;}
.mini-button>svg{width:10px;height:10px;}
select.button{-webkit-appearance:none;-moz-appearance:none;appearance:none;text-indent:1px;text-overflow:'';}
.modal{position:fixed;width:600px;min-width:380px;left:50%;top:40px;margin-left:-300px;padding:20px;background:var(--cp-color-20);z-index:300;max-height:90%;max-height:calc(100% - 80px);overflow-x:hidden;overflow-y:auto;}
.modal::-webkit-scrollbar{width:.5em;height:.5em;}
.modal::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.modal::-webkit-scrollbar-track{background:var(--cp-color-5);}
.modal p{color:var(--cp-color-6);margin:0 0 25px;}
.modal.modal-neutral{border:10px solid var(--cp-color-12);}
@media (max-width:830px){
.modal{top:20px;left:10px;right:10px;width:auto;min-width:0;max-height:375px;overflow:auto;margin-left:0;}
}
@media (max-width:600px){
.modal{-webkit-box-sizing:border-box;box-sizing:border-box;width:90%;left:0;right:0;margin:auto;min-width:auto;}
}
.overlay{position:fixed;display:none;top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,.6);}
.modal-overlay{z-index:300;}
.popup-overlay{z-index:200;}
.help-flyout{font-family:var(--cp-font-family);display:none;position:absolute;z-index:10;left:100%;top:-20px;margin-left:12px;border:5px solid var(--cp-color-12);-webkit-box-shadow:2px 2px 8px rgba(0,0,0,.5);box-shadow:2px 2px 8px rgba(0,0,0,.5);width:300px;padding:20px;background:var(--cp-color-20);text-align:left;font-weight:400;color:var(--cp-color-8);cursor:auto;}
.help-flyout::before{content:'';position:absolute;left:0;margin-left:-14px;top:12px;width:0;height:0;border-right:10px solid var(--cp-color-12);border-top:10px solid transparent;border-bottom:10px solid transparent;}
.help-flyout h5{color:var(--cp-color-1);margin:0 0 .5rem;}
.help-flyout p{color:var(--cp-color-8)!important;font-size:.9rem;margin:0 0 1rem;}
.help-flyout p:last-child{margin:0;}
.settings .help-flyout a{color:var(--cp-color-link-on-black);white-space:nowrap;border-color:var(--cp-color-link-on-black);}
.settings .help-flyout a:hover,.settings .help-flyout a:focus{color:#fff;border:none;}
.help-flyout pre{white-space:pre-wrap;}
.help-flyout-reverse{left:auto;right:100%;margin-left:0;margin-right:12px;}
.help-flyout-reverse::before{left:auto;right:0;margin-left:0;margin-right:-24px;border-right:10px solid transparent;border-left:10px solid var(--cp-color-12);}
.help-flyout-link{position:absolute;top:3px;right:0;width:14px;height:14px;margin:0;cursor:pointer;}
.help-flyout-link .icon-help{width:100%;height:100%;fill:var(--cp-color-11);}
.help-flyout-link .icon-help:hover,.help-flyout-link .icon-help:focus{fill:var(--cp-color-blue);}
.help-flyout-link svg{display:block;}
.help-flyout-link .icon-x{width:12px;height:12px;fill:var(--cp-color-12);position:absolute;top:10px;right:10px;cursor:pointer;}
.help-flyout-link .icon-x:hover,.help-flyout-link .icon-x:focus{fill:var(--cp-color-6);}
@media print{
.follow-user-button{display:none;}
body{padding:1rem!important;overflow-x:visible;overflow-y:visible;}
body,pre{background:#fff!important;color:#000!important;}
.box{border:double .5em #666;margin:0 0 1em;}
}
}
/*! CSS Used from: https://cpwebassets.codepen.io/assets/packs/css/everypage-33b8a4ed.css ; media=screen */
@media screen{
.Button-module_root-26v5l{font-family:var(--cp-font-family);-webkit-appearance:none;display:inline-flex;align-items:center;vertical-align:middle;position:relative;font-family:inherit;font-size:1rem;text-shadow:none;line-height:1.2;white-space:nowrap;text-overflow:ellipsis;text-decoration:none!important;font-weight:400!important;cursor:pointer;background:var(--cp-button-bg);color:var(--cp-button-color);padding:var(--cp-button-padding);margin:var(--cp-button-margin);border-radius:var(--cp-button-border-radius);border:var(--cp-button-border-width) solid transparent;--cp-button-padding:var(--cp-button-padding-block) var(--cp-button-padding-inline);--cp-button-margin:var(--cp-button-margin-block) var(--cp-button-margin-inline) var(--cp-button-margin-block) 0;text-align:center;justify-content:center;}
.Button-module_root-26v5l:focus,.Button-module_root-26v5l:hover{background:var(--cp-button-hover-bg,var(--cp-button-bg))!important;color:var(--cp-button-hover-color,var(--cp-button-color))!important;outline-offset:3px;}
.Button-module_root-26v5l:focus svg,.Button-module_root-26v5l:hover svg{fill:var(--cp-button-hover-icon,var(--cp-button-icon));}
.Button-module_root-26v5l::-moz-focus-inner{border:0;padding:0;}
.Button-module_root-26v5l:active{transform:translateY(1px);}
.Button-module_root-26v5l>svg{width:16px;height:16px;min-height:1.2em;display:inline-block;pointer-events:none;vertical-align:bottom;fill:var(--cp-button-icon);}
.Button-module_root-26v5l[data-has-icon]>svg:first-child{margin-right:.35em;}
.Button-module_root-26v5l[data-color=green]{--cp-button-bg:var(--cp-color-green);--cp-button-color:#000;--cp-button-hover-bg:var(--cp-color-green-dark);}
.Button-module_root-26v5l[data-color=grad-blue]{--cp-button-bg:linear-gradient(90deg,var(--cp-color-blue-dark),var(--cp-button-default-bg));--cp-button-hover-bg:var(--cp-color-blue-dark);background-size:calc(100% + 6px);background-position:-3px 0;}
.Button-module_root-26v5l[data-color=grad-yellow]{--cp-button-bg:linear-gradient(90deg,var(--cp-color-yellow-dark),var(--cp-button-default-bg));--cp-button-hover-bg:var(--cp-color-yellow-dark);background-size:calc(100% + 6px);background-position:-3px 0;}
.Button-module_root-26v5l[data-align=start]{text-align:left;justify-content:start;}
.Button-module_root-26v5l[data-size=mini]{font-size:.8rem;--cp-button-padding-inline:7px;--cp-button-padding-block:3px;--cp-button-margin-block:0;--cp-button-margin-inline:4px;--cp-button-border-width:1px;--cp-button-border-radius:2px;}
.Button-module_root-26v5l[data-size=mini]>svg{width:10px;height:10px;vertical-align:middle;}
.Button-module_root-26v5l[data-size=small]{--cp-button-padding-inline:11px;--cp-button-padding-block:6px;font-size:.96rem;}
.Button-module_root-26v5l[data-full-width]{display:flex;width:100%;--cp-button-margin-block:var(--cp-button-margin-inline);}
.ButtonGroup-module_root-39y_y{display:inline-flex;align-items:stretch;margin:var(--cp-button-margin);--cp-button-margin:var(--cp-button-margin-block) var(--cp-button-margin-inline) var(--cp-button-margin-block) 0;}
.ButtonGroup-module_root-39y_y>*{--cp-button-margin-inline:1px;--cp-button-margin-block:0;border-radius:0;}
.ButtonGroup-module_root-39y_y>:first-child{border-top-left-radius:var(--cp-button-border-radius);border-bottom-left-radius:var(--cp-button-border-radius);}
.ButtonGroup-module_root-39y_y>:last-child{border-top-right-radius:var(--cp-button-border-radius);border-bottom-right-radius:var(--cp-button-border-radius);--cp-button-margin-inline:0;}
.DropdownControlled-module_root-1_SPF{position:relative;display:inline-block;}
.DropdownControlled-module_content-2k0O6{position:absolute;z-index:20;visibility:visible;}
.DropdownControlled-module_content-2k0O6[hidden]{display:block;visibility:hidden;pointer-events:none;}
.DropdownControlled-module_content-2k0O6[data-direction="top left"]{bottom:100%;right:0;transform-origin:bottom right;}
.DropdownControlled-module_content-2k0O6[data-direction="bottom left"]{top:100%;right:0;transform-origin:top right;}
.ButtonWithDropdownTrigger-module_root-1xvSj{--cp-button-padding-inline:5px;--cp-button-padding-block:5px;--cp-button-icon:var(--cp-color-8);--cp-button-hover-icon:var(--cp-color-1);position:relative;}
.ButtonWithDropdownTrigger-module_root-1xvSj:after{content:"";position:absolute;bottom:0;left:0;right:0;background:var(--cp-color-green);border-radius:inherit;height:2px;transform:scaleX(0);transition:transform .2s ease-out;}
.ButtonWithDropdownTrigger-module_icon-kvmuA.ButtonWithDropdownTrigger-module_icon-kvmuA{width:10px;height:8px;top:1px;position:relative;transition:transform .2s linear;}
.Badge-module_root-3RxmQ{-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;font-family:var(--cp-font-family-header-alt);text-transform:uppercase;font-size:.8rem;padding:.125rem .375rem 0;border-radius:2px;background:var(--cp-color-9);color:var(--cp-color-20);margin-right:.5rem;display:inline-block;}
.Badge-module_root-3RxmQ svg{display:block;}
.BadgePro-module_root-15RvN{background:var(--cp-color-yellow);color:#000!important;}
.BadgePro-module_svg-3HOXN{padding:0;margin-left:.4rem;}
.DropdownContent-module_root-tkW5u{padding:.5rem;border-radius:3px;background:var(--cp-color-1);color:var(--cp-color-16);opacity:1;transform:scale(1);transform-origin:inherit;min-width:150px;max-width:20em;transition:transform var(--dropdown-duration,.2s) ease-in-out,opacity var(--dropdown-duration,.2s) linear,visibility 0s linear;box-shadow:0 2px 8px var(--cp-color-shadow);visibility:visible;}
.DropdownContent-module_root-tkW5u[data-dark]{background:var(--cp-color-16);color:var(--cp-color-1);box-shadow:0 6px 15px var(--cp-color-shadow);}
[hidden]>.DropdownContent-module_root-tkW5u{transform:scale(.95);opacity:0;visibility:hidden;transition-delay:0s,0s,.2s;}
.Input-module_input-t-e1t.Input-module_input-t-e1t[type=tel]{background:var(--cp-color-4);border:2px solid transparent;border-radius:3px;padding:calc(1rem - 2px);font-size:.875rem;line-height:1.1;max-width:100%;color:var(--cp-color-17);}
.Input-module_input-t-e1t.Input-module_input-t-e1t[type=tel]::placeholder{color:var(--cp-color-10);opacity:1;}
.Input-module_input-t-e1t.Input-module_input-t-e1t:focus{border-color:var(--cp-color-11);background:var(--cp-color-1);}
.Input-module_fullWidth-19NOa{width:100%;}
.MobileNavButton-module_icon-1XOc-{width:24px;height:24px;margin:2px 0;position:relative;transition:all .2s ease;transition-property:transform,width;}
.MobileNavButton-module_icon-1XOc- svg{width:14px!important;position:absolute;top:5px;right:0;fill:currentColor;transition:transform .2s ease;transform:scale(1);}
.MobileNavButton-module_icon-1XOc- span{position:absolute;display:block;background:currentColor;border-radius:6px;height:2px;width:10px;left:0;top:12px;transition:inherit;}
.MobileNavButton-module_icon-1XOc- span:after,.MobileNavButton-module_icon-1XOc- span:before{content:"";position:absolute;left:0;height:inherit;background:inherit;border-radius:inherit;transition:inherit;}
.MobileNavButton-module_icon-1XOc- span:before{top:-6px;width:6px;}
.MobileNavButton-module_icon-1XOc- span:after{bottom:-6px;width:16px;}
.FollowButton-module_root-dJOFR{margin-left:6px!important;position:relative;}
.FollowButton-module_root-dJOFR[data-size=mini]{line-height:12px;--cp-button-padding-block:2px;--cp-button-padding-inline:5px;}
.FollowButton-module_root-dJOFR[data-size=mini] .FollowButton-module_statusIcon-1PHuV{top:0;}
.FollowButton-module_root-dJOFR .FollowButton-module_statusIcon-1PHuV{top:1px;}
.ItemTitle_root-1DCrM{white-space:nowrap;display:flex;align-items:center;flex-shrink:1;flex-grow:1;min-width:120px;}
.ItemTitle_text-L5Z9D{width:100%;overflow:hidden;}
.ItemTitle_title-3IXzM{font-family:var(--cp-font-family);font-size:1.3rem;margin:0 0 .1rem;display:flex;align-items:center;}
@media (max-height:440px),(max-width:767px){
.ItemTitle_title-3IXzM{margin:0 0 4px;font-size:1.1rem;}
}
.ItemTitle_titleLink-3b80D{color:var(--cp-color-1);font-weight:700;overflow:hidden;white-space:nowrap;text-overflow:ellipsis;max-width:100%;display:inline-block;vertical-align:middle;}
.ItemTitle_by-n66uI{display:flex;align-items:center;}
@media (max-height:440px),(max-width:767px){
.ItemTitle_by-n66uI .follow-user-button{display:none;}
}
.ItemTitle_followButton-2zR-z.ItemTitle_followButton-2zR-z{font-size:.7rem;height:16px;--cp-button-padding-block:1px;}
.ItemTitle_ownerLink-1KURC{overflow:hidden;white-space:nowrap;text-overflow:ellipsis;color:var(--cp-color-9);font-size:.9rem;text-transform:none;letter-spacing:0;max-width:100%;}
.EditorHeaderViewSwitcherLayoutButtons-module_buttonGroup-2qBzd{width:100%;--cp-button-active:var(--cp-color-12);--cp-button-bg:transparent;--cp-button-icon:var(--cp-button-active);--cp-button-hover-bg:var(--cp-color-14);--cp-button-hover-icon:var(--cp-color-7);--cp-button-border-width:2px;--cp-button-margin-inline:0;}
.EditorHeaderViewSwitcherLayoutButtons-module_buttonGroup-2qBzd [data-layout-type]{flex:1;border-color:var(--cp-button-active);margin:0;}
.EditorHeaderViewSwitcherLayoutButtons-module_buttonGroup-2qBzd [data-layout-type]:not(:first-child){border-left-width:0;}
body.layout-top .EditorHeaderViewSwitcherLayoutButtons-module_buttonGroup-2qBzd [data-layout-type=top]{--cp-button-bg:var(--cp-button-active);--cp-button-hover-bg:var(--cp-button-active);--cp-button-icon:#fff;--cp-button-hover-icon:#fff;}
.EditorHeaderViewSwitcher_root-kcTSX{display:flex;align-items:stretch;}
.EditorHeaderViewSwitcher_mobile-1WXlX{display:none;margin-top:.5rem;border-top:1px solid var(--cp-color-14);padding:.5rem 1rem;}
@media (max-height:440px),(max-width:767px){
.EditorHeaderViewSwitcher_root-kcTSX{display:none;}
.EditorHeaderViewSwitcher_mobile-1WXlX{display:block;}
}
.EditorHeaderViewSwitcher_iconPen-1Mc1B{display:block;transform:rotate(0turn);transition:transform .2s cubic-bezier(1,0,0,1);}
.EditorHeaderViewSwitcher_dropdown-1LM5k{border:3px solid var(--cp-color-20);border-radius:.5rem;padding:1rem;width:300px;text-align:left;}
.EditorHeaderViewSwitcher_dropdown-1LM5k h3{font-size:1.1rem;}
@media (max-height:440px),(max-width:767px){
.EditorHeaderViewSwitcher_dropdown-1LM5k h3{margin:.5rem 1rem;}
}
.EditorHeaderViewSwitcher_switch-1nHOd+.EditorHeaderViewSwitcher_switch-1nHOd{margin-top:1rem;}
.EditorHeaderViewSwitcherLink_link-1WfWP{font-family:var(--cp-font-family);position:relative;display:flex;align-items:center;flex-wrap:wrap;color:var(--cp-color-8);margin:0 -1rem;padding:6px 1rem;text-align:left;border-radius:0;line-height:1.1;font-size:.9rem;text-shadow:none;text-decoration:none;}
.EditorHeaderViewSwitcherLink_link-1WfWP:focus,.EditorHeaderViewSwitcherLink_link-1WfWP:hover{color:inherit;background:var(--cp-color-12);}
.EditorHeaderViewSwitcherLink_link-1WfWP:focus .EditorHeaderViewSwitcherLink_linkMeta-63jt2,.EditorHeaderViewSwitcherLink_link-1WfWP:hover .EditorHeaderViewSwitcherLink_linkMeta-63jt2{opacity:.8;}
.EditorHeaderViewSwitcherLink_link-1WfWP.active{background:var(--cp-color-13);color:var(--cp-color-1);}
.EditorHeaderViewSwitcherLink_link-1WfWP.active .EditorHeaderViewSwitcherLink_linkMeta-63jt2{opacity:.8;}
.EditorHeaderViewSwitcherLink_badgePro-2v1Vq{margin-left:0;}
.EditorHeaderViewSwitcherLink_linkMeta-63jt2{margin-left:auto;color:inherit;opacity:.6;display:flex;align-items:center;line-height:1;}
.EditorHeaderViewSwitcherLink_linkMeta-63jt2 .EditorHeaderViewSwitcherLink_learnMore-38FPT{display:inline-block;margin-left:10px;}
.EditorHeaderViewSwitcherLink_linkMeta-63jt2 svg{display:block;pointer-events:none;width:12px;height:12px;fill:currentColor;}
.run{display:none!important;}
.Logo_root-28eiX{margin:0;height:var(--cp-header-height);}
@media (max-width:830px){
.Logo_root-28eiX{height:var(--cp-header-height-small);}
}
.Logo_root-28eiX .Logo_small-2rYbf{display:block;width:30px;height:100%;margin:0 8px;}
@media (min-width:831px){
.Logo_root-28eiX .Logo_small-2rYbf{display:none;}
}
@media (max-width:550px){
body.editor .Logo_root-28eiX .Logo_small-2rYbf{width:20px;}
}
.Logo_root-28eiX .Logo_small-2rYbf svg{display:block;fill:var(--cp-color-1);height:100%;width:100%;}
.Logo_root-28eiX .Logo_large-3wkfp{display:none;height:65px;border:0;padding:0 1.25rem;}
@media (min-width:831px){
.Logo_root-28eiX .Logo_large-3wkfp{display:inline-block;height:75px;}
}
.Logo_root-28eiX .Logo_large-3wkfp svg{display:block;fill:none;stroke:var(--cp-color-1);stroke-width:2.3;stroke-linejoin:round;stroke-linecap:round;height:100%;width:150px;}
.main-header .Logo_large-3wkfp{display:none;}
.main-header .Logo_small-2rYbf{display:block;}
.UserMenu_userMenuButton-1uSED{font-family:var(--cp-font-family);display:grid;grid:"layer";align-items:center;position:relative;cursor:pointer;border:0;margin-right:1rem;transition:background-color .2s linear;width:44px;height:44px;border-radius:3px;background-color:var(--cp-color-16);}
.UserMenu_userMenuButton-1uSED .UserMenu_sessionUserAvatar-2WeRf{display:block;grid-area:layer;width:100%;height:100%;border-radius:3px;background-color:inherit;background-size:contain;background-position:50%;}
.UserMenu_userMenuButton-1uSED .UserMenu_sessionUserAvatar-2WeRf{transition:transform .2s cubic-bezier(.6,0,.3,1);transform-origin:bottom right;}
.UserMenu_userMenuButton-1uSED:after{content:"";display:block;width:100%;position:absolute;top:100%;margin-top:3px;z-index:101;border-bottom:3px solid var(--cp-color-green);transform:scaleX(0);transform-origin:center right;transition:transform .1s ease;}
.UserMenu_userMenuDropdownParent-3PtgF{position:relative;}
.UserMenu_userMenu-2n6e1{overflow-y:auto;position:absolute;z-index:100;right:1rem;top:51px;width:225px;list-style:none;max-height:80vh;max-height:calc(100vh - 71px);white-space:nowrap;opacity:0;visibility:hidden;padding:.5rem 0;background:var(--cp-color-16);color:var(--cp-color-4);border-radius:6px 0 6px 6px;box-shadow:0 2rem 4rem var(--cp-color-18);transform:scale(.9);transform-origin:top right;transition:all .2s ease-in-out,visibility 0s linear .2s;}
.UserMenu_userMenu-2n6e1::-webkit-scrollbar{width:.5em;height:.5em;}
.UserMenu_userMenu-2n6e1::-webkit-scrollbar-thumb{background:var(--cp-color-12);}
.UserMenu_userMenu-2n6e1::-webkit-scrollbar-track{background:0 0;}
body.editor .UserMenu_userMenuButton-1uSED{margin-right:10px;}
@media (max-height:440px),(max-width:767px){
body.editor .UserMenu_userMenuButton-1uSED{width:32px;height:32px;margin-right:.5rem;}
body.editor .UserMenu_userMenu-2n6e1{right:.5rem;}
}
.HeaderWrap-module_root-aRSWR{height:100%;display:flex;align-items:center;position:relative;z-index:11;}
.LoveButtonIcon-module_root-3dw_B{fill:var(--cp-color-1);transform:scale(1) translateY(0);transition:.1s;transition-timing-function:cubic-bezier(.39,-.17,.67,1.23);}
.PinButton-module_pinButton-1Ykmn{--cp-button-padding-inline:0.625rem;}
@media (max-width:830px){
.editor-header .PinButton-module_pinButtonGroup-3oRI0{margin-right:4px;}
}
@media (max-height:440px),(max-width:767px){
.editor-header .PinButton-module_pinButtonGroup-3oRI0{display:none!important;}
}
@media (max-width:830px){
.EditorHeader-module_root-2-32Y{--cp-button-margin-inline:5px;--cp-button-padding-inline:10px;--cp-button-padding-block:6px;}
}
.PenEditorFooterExportDropdown-module_dropdown-1pNCn{padding:1rem;width:295px;background:var(--cp-color-16);color:var(--cp-color-1);}
.PenEditorFooterExportDropdown-module_dropdown-1pNCn button{font-weight:700!important;}
.PenEditorFooterExportDropdown-module_header-pMcqr{display:flex;align-items:center;justify-content:space-between;}
.PenEditorFooterExportDropdown-module_header-pMcqr svg{width:14px;height:14px;fill:var(--cp-color-11);}
.PenEditorFooterExportDropdown-module_header-pMcqr a:focus svg,.PenEditorFooterExportDropdown-module_header-pMcqr a:hover svg{fill:var(--cp-color-1);}
.PenEditorFooterExportDropdown-module_proWrap-3dNG4{--cp-button-margin-block:0;--cp-button-margin-inline:0;}
.PenEditorFooterExportDropdown-module_proWrap-3dNG4 .PenEditorFooterExportDropdown-module_proBadge-35QPz{display:block;height:0;position:relative;z-index:1;top:-7px;}
.ShareSMS-module_root-1gNGP{margin:0 0 1rem;}
.ShareSMS-module_root-1gNGP p{margin:0 0 .33rem;color:var(--cp-color-9);}
.ShareSMS-module_header-1U9m5{display:flex;align-items:center;justify-content:space-between;}
.ShareSMS-module_header-1U9m5 svg{width:14px;height:14px;fill:var(--cp-color-11);}
.ShareSMS-module_header-1U9m5 a:focus svg,.ShareSMS-module_header-1U9m5 a:hover svg{fill:var(--cp-color-1);}
.ShareSMS-module_input-UU3zR{margin:0 0 .33rem;}
.ShareDropdown-module_dropdown-LZAZy{padding:1rem;width:295px;background:var(--cp-color-16);color:var(--cp-color-1);}
.ShareDropdown-module_dropdown-LZAZy>:last-child{--cp-button-margin-block:0;--cp-button-margin-inline:0;}
.PenEditorFooterStatus_editorState-2S_W-{display:inline-flex;align-items:center;justify-content:flex-end;margin:0 .5rem;height:20px;flex:1 1 200px;padding:3px 0;text-align:right;}
.PenEditorFooterStatus_editorState-2S_W- svg{width:14px;height:14px;}
@media (max-height:440px),(max-width:767px){
.PenEditorFooterStatus_editorState-2S_W-{min-width:20px;}
.PenEditorFooterStatus_editorState-2S_W- .PenEditorFooterStatus_text-1jvoK{display:none;}
}
.PenEditorFooterStatus_text-1jvoK{flex:1;min-width:150px;font-size:.8rem;color:var(--cp-color-6);margin-right:.25rem;overflow:hidden;white-space:nowrap;text-overflow:ellipsis;}
}
/*! CSS Used from: https://cpwebassets.codepen.io/assets/editor/editor-ec834d7ed6d95e38b2715af283b4c3fb6bd5d2aa0c3e0c37927cd2aea1e53e54.css ; media=all */
@media all{
.editor-dropdown,.tab-layout-modal{background:var(--cp-color-1);-webkit-box-shadow:0 4px 20px rgba(0,0,0,.2);box-shadow:0 4px 20px rgba(0,0,0,.2);border-radius:3px;position:absolute;top:100%;padding:5px 0;width:220px;color:var(--cp-color-14);opacity:0;visibility:hidden;-webkit-transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;-webkit-transform:scale(.95);transform:scale(.95);-webkit-transform-origin:top right;transform-origin:top right;}
.editor-dropdown,.tab-layout-modal{background:var(--cp-color-1);-webkit-box-shadow:0 4px 20px rgba(0,0,0,.2);box-shadow:0 4px 20px rgba(0,0,0,.2);border-radius:3px;position:absolute;top:100%;padding:5px 0;width:220px;color:var(--cp-color-14);opacity:0;visibility:hidden;-webkit-transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;-webkit-transform:scale(.95);transform:scale(.95);-webkit-transform-origin:top right;transform-origin:top right;}
body.layout-top .resizer{height:18px;cursor:row-resize;position:relative;z-index:10;}
body.layout-top .resizer{-webkit-flex-shrink:0;-ms-flex-negative:0;flex-shrink:0;}
@media (min-width:768px) and (min-height:440px){
body.layout-top .boxes{-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;}
body.layout-top .top-boxes{width:100%;height:350px;min-height:125px;-webkit-flex-shrink:0;-ms-flex-negative:0;flex-shrink:0;}
body.layout-top .top-boxes[data-number-of-editors='3'] .box{width:32%;width:calc((100% - 20px * 3)/3);}
body.layout-top .top-boxes .editor-resizer{position:relative;z-index:2;width:18px;cursor:col-resize;}
body.layout-top .editor-resizer:first-child{cursor:auto;}
body.layout-top .top-boxes .box .box-title-name,body.layout-top .top-boxes .box .box-title-preprocessor-name,body.layout-top .top-boxes .box .file-type-icon{visibility:hidden;}
body.layout-top .box-title--resizer{position:absolute;left:17px;top:0;z-index:2;pointer-events:none;-webkit-transition:-webkit-transform .2s;transition:-webkit-transform .2s;transition:transform .2s;transition:transform .2s,-webkit-transform .2s;-webkit-transform-origin:left center;transform-origin:left center;}
body.layout-top .width-readout{left:50%;top:50%;padding:4px 8px;}
}
.editor-dropdown,.tab-layout-modal{background:var(--cp-color-1);-webkit-box-shadow:0 4px 20px rgba(0,0,0,.2);box-shadow:0 4px 20px rgba(0,0,0,.2);border-radius:3px;position:absolute;top:100%;padding:5px 0;width:220px;color:var(--cp-color-14);opacity:0;visibility:hidden;-webkit-transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;-webkit-transform:scale(.95);transform:scale(.95);-webkit-transform-origin:top right;transform-origin:top right;}
.editor-dropdown,.tab-layout-modal{background:var(--cp-color-1);-webkit-box-shadow:0 4px 20px rgba(0,0,0,.2);box-shadow:0 4px 20px rgba(0,0,0,.2);border-radius:3px;position:absolute;top:100%;padding:5px 0;width:220px;color:var(--cp-color-14);opacity:0;visibility:hidden;-webkit-transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s;transition:transform .15s,opacity .15s,visibility 0s linear .15s,-webkit-transform .15s;-webkit-transform:scale(.95);transform:scale(.95);-webkit-transform-origin:top right;transform-origin:top right;}
@media (min-width:768px) and (min-height:440px){
.editor-resizer-console{height:1px;cursor:row-resize;}
.box-console .powers-drag-handle{display:block;cursor:row-resize;}
}
.CodeMirror{font-family:monospace;height:300px;color:var(--cp-color-20);direction:ltr;}
.CodeMirror-lines{padding:4px 0;}
.CodeMirror pre.CodeMirror-line,.CodeMirror pre.CodeMirror-line-like{padding:0 4px;}
.CodeMirror-scrollbar-filler,.CodeMirror-gutter-filler{background-color:var(--cp-color-1);}
.CodeMirror-gutters{border-right:1px solid #ddd;background-color:#f7f7f7;white-space:nowrap;}
.CodeMirror-linenumber{padding:0 3px 0 5px;min-width:20px;text-align:right;color:var(--cp-color-9);white-space:nowrap;}
.CodeMirror-guttermarker-subtle{color:var(--cp-color-9);}
.CodeMirror{position:relative;overflow:hidden;background:var(--cp-color-1);}
.CodeMirror-scroll{overflow:scroll!important;margin-bottom:-30px;margin-right:-30px;padding-bottom:30px;height:100%;outline:none;position:relative;}
.CodeMirror-sizer{position:relative;border-right:30px solid transparent;}
.CodeMirror-scrollbar-filler,.CodeMirror-gutter-filler{position:absolute;z-index:6;display:none;}
.CodeMirror-scrollbar-filler{right:0;bottom:0;}
.CodeMirror-gutter-filler{left:0;bottom:0;}
.CodeMirror-gutters{position:absolute;left:0;top:0;min-height:100%;z-index:3;}
.CodeMirror-gutter{white-space:normal;height:100%;display:inline-block;vertical-align:top;margin-bottom:-30px;}
.CodeMirror-gutter-wrapper{position:absolute;z-index:4;background:0 0!important;border:none!important;}
.CodeMirror-gutter-elt{position:absolute;cursor:default;z-index:4;}
.CodeMirror-gutter-wrapper ::-moz-selection{background-color:transparent;}
.CodeMirror-gutter-wrapper ::selection{background-color:transparent;}
.CodeMirror-gutter-wrapper ::-moz-selection{background-color:transparent;}
.CodeMirror-lines{cursor:text;min-height:1px;}
.CodeMirror pre.CodeMirror-line,.CodeMirror pre.CodeMirror-line-like{border-radius:0;border-width:0;background:0 0;font-family:inherit;font-size:inherit;margin:0;white-space:pre;word-wrap:normal;line-height:inherit;color:inherit;z-index:2;position:relative;overflow:visible;-webkit-tap-highlight-color:transparent;-webkit-font-variant-ligatures:contextual;font-variant-ligatures:contextual;}
.CodeMirror-wrap pre.CodeMirror-line,.CodeMirror-wrap pre.CodeMirror-line-like{word-wrap:break-word;white-space:pre-wrap;word-break:normal;}
.CodeMirror-code{outline:none;}
.CodeMirror-scroll,.CodeMirror-sizer,.CodeMirror-gutter,.CodeMirror-gutters,.CodeMirror-linenumber{-webkit-box-sizing:content-box;box-sizing:content-box;}
.CodeMirror-measure{position:absolute;width:100%;height:0;overflow:hidden;visibility:hidden;}
.CodeMirror-measure pre{position:static;}
div.CodeMirror-cursors{visibility:hidden;position:relative;z-index:3;}
.CodeMirror-line::-moz-selection,.CodeMirror-line>span::-moz-selection,.CodeMirror-line>span>span::-moz-selection{background:#d7d4f0;}
.CodeMirror-line::selection,.CodeMirror-line>span::selection,.CodeMirror-line>span>span::selection{background:#d7d4f0;}
.CodeMirror-line::-moz-selection,.CodeMirror-line>span::-moz-selection,.CodeMirror-line>span>span::-moz-selection{background:#d7d4f0;}
@media print{
.CodeMirror div.CodeMirror-cursors{visibility:hidden;}
}
.CodeMirror{font-family:var(--cp-font-family-monospace);font-size:15px;line-height:1.5;background:0 0;height:100%;}
.CodeMirror pre{z-index:4;margin:0;}
.CodeMirror-gutters{border:0;background:0 0;}
@media (max-width:767px),(max-height:440px){
.CodeMirror-gutters{display:none;}
}
.CodeMirror-sizer{margin-bottom:0!important;}
.CodeMirror-scrollbar-filler,.CodeMirror-gutter-filler{background-color:transparent;}
@media (max-width:767px),(max-height:440px){
.CodeMirror-gutter-wrapper{display:none;}
}
@media (max-width:767px),(max-height:440px){
.CodeMirror-sizer{margin-left:0!important;}
}
.CodeMirror-foldgutter{width:.7em;}
.CodeMirror-foldgutter-open{cursor:pointer;}
.CodeMirror-foldgutter-open::after{font-family:sans-serif;content:'\25BE';}
.CodeMirror-simplescroll-horizontal div,.CodeMirror-simplescroll-vertical div{position:absolute;background-clip:padding-box!important;}
.CodeMirror-simplescroll-horizontal div{border-bottom:4px solid transparent;}
.CodeMirror-simplescroll-vertical div{border-right:4px solid transparent;}
.CodeMirror-simplescroll-horizontal,.CodeMirror-simplescroll-vertical{position:absolute;z-index:6;}
.CodeMirror-simplescroll-horizontal{bottom:0;left:0;height:9px;}
.CodeMirror-simplescroll-horizontal div{bottom:0;height:100%;}
.CodeMirror-simplescroll-vertical{right:0;top:0;width:9px;}
.CodeMirror-simplescroll-vertical div{right:0;width:100%;}
.error-bar{display:none;position:absolute;z-index:5;bottom:10px;right:10px;width:20px;font-weight:700;text-align:right;color:#fff;padding-right:10px;}
.error-icon{cursor:pointer;border-radius:50%;width:15px;height:15px;line-height:15px;display:inline-block;text-align:center;background:var(--cp-color-red);color:#fff;}
.error-icon:hover,.error-icon:focus{background:#fff;color:var(--cp-color-red);}
#keycommands{display:none;top:25px;width:800px;max-width:90%;margin:auto;left:0;right:0;z-index:201;overflow:auto;}
#keycommands::-webkit-scrollbar{width:.5em;height:.5em;}
#keycommands::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
#keycommands::-webkit-scrollbar-track{background:0 0;}
#keycommands h2{margin:15px 0 5px;padding-bottom:3px;border-bottom:1px solid var(--cp-color-11);}
#keycommands h2:first-child{margin-top:0;}
#keycommands .key-group{font-size:14px;margin:0 0 5px;color:var(--cp-color-1);}
.keycommands-container{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-flex-wrap:wrap;-ms-flex-wrap:wrap;flex-wrap:wrap;-webkit-box-pack:center;-webkit-justify-content:center;-ms-flex-pack:center;justify-content:center;margin:-10px;}
.keycommands-container>section{-webkit-box-flex:1;-webkit-flex:1 1 30%;-ms-flex:1 1 30%;flex:1 1 30%;margin:10px 10px 30px;}
.mac_only,.pc_only{display:none;}
.keycommand{display:-webkit-inline-box;display:-webkit-inline-flex;display:-ms-inline-flexbox;display:inline-flex;color:var(--cp-color-yellow);font-family:system-ui,monospace;font-size:12px;font-weight:700;white-space:normal;margin-right:.25em;}
.keycommand .key{margin-right:2px;padding:3px 6px;line-height:1;background:var(--cp-color-6);color:var(--cp-color-16);border-radius:2px;}
.keycommand .key.-command::before{content:'Cmd/Ctrl';}
.tab-layout-modal{border:3px solid var(--cp-color-15);background:var(--cp-color-17);top:70px;left:1rem;right:1rem;bottom:2rem;margin:0 auto auto;padding:0;color:var(--cp-color-1);border-radius:4px;z-index:200;-webkit-transform:scale(.9);transform:scale(.9);-webkit-transform-origin:center center;transform-origin:center center;width:700px;max-width:calc(100% - 2rem);max-height:80vh;}
@media (max-width:767px),(max-height:440px){
.tab-layout-modal{top:30px;width:auto;max-height:none;}
}
@media (max-width:550px){
.tab-layout-modal{width:100%;width:calc(100% - 2rem);}
}
.tab-layout-modal input[type=text],.tab-layout-modal textarea{background:var(--cp-color-4)!important;border-color:var(--cp-color-4)!important;color:var(--cp-color-14);}
.tab-layout-modal input[type=text]:focus,.tab-layout-modal textarea:focus{background:var(--cp-color-1);border-color:var(--cp-color-1);}
.tab-layout{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;}
.tab-layout>.tabs{padding-bottom:0;}
.tab-layout footer{background:var(--cp-color-15);border-radius:0 0 4px 4px;-webkit-box-shadow:0 -4px 10px var(--cp-color-shadow);box-shadow:0 -4px 10px var(--cp-color-shadow);padding:.75rem;position:relative;}
.tab-layout footer .close{margin-left:auto;}
.tab-layout footer .save-and-close-wrap{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-pack:justify;-webkit-justify-content:space-between;-ms-flex-pack:justify;justify-content:space-between;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;}
.tab-layout-header{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;-webkit-flex-shrink:0;-ms-flex-negative:0;flex-shrink:0;border-bottom:2px solid var(--cp-color-14);margin:.375rem 1.25rem 0;}
.tab-layout-header-title{font-family:var(--cp-font-family);color:inherit;margin:.2rem auto 0 0;font-size:1.125rem;font-weight:700;border-bottom:2px solid var(--cp-color-green);padding:.625rem 0;margin-bottom:-2px;}
.tab-layout-tabs{overflow-y:auto;overflow-x:hidden;padding:1rem 0;margin-bottom:0!important;}
.tab-layout-tabs::-webkit-scrollbar{width:.5em;height:.5em;}
.tab-layout-tabs::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.tab-layout-tabs::-webkit-scrollbar-track{background:var(--cp-color-18);}
@media (max-width:767px),(max-height:440px){
.tab-layout-tabs{padding:.2rem 0 1rem;margin:1rem .75rem 0;overflow-y:hidden;overflow-x:auto;white-space:nowrap;border-bottom:2px solid var(--cp-color-14);}
}
.tab-layout-tabs a{display:block;color:var(--cp-color-1);-webkit-transition:.3s ease;transition:.3s ease;-webkit-transition-property:background-color,-webkit-transform;transition-property:background-color,-webkit-transform;transition-property:transform,background-color;transition-property:transform,background-color,-webkit-transform;line-height:1.7;padding:0 1.25rem;overflow:hidden;position:relative;}
.tab-layout-tabs a::before{position:absolute;left:0;top:0;bottom:0;content:'';width:3px;background:var(--cp-color-green);-webkit-transform:translateX(-100%);transform:translateX(-100%);-webkit-transition:inherit;transition:inherit;}
.tab-layout-tabs a.active,.tab-layout-tabs a:hover,.tab-layout-tabs a:active{background:var(--cp-color-14);}
.tab-layout-tabs a.active{font-weight:700;}
.tab-layout-tabs a.active::before{-webkit-transform:translateX(0);transform:translateX(0);}
@media (max-width:767px),(max-height:440px){
.tab-layout-tabs a{display:inline-block;padding:0 .5rem;}
.tab-layout-tabs a::before{display:none;}
}
.tab-layout-tab-group{margin-bottom:1rem;}
@media (max-width:767px),(max-height:440px){
.tab-layout-tab-group{margin-bottom:0;display:inline-block;}
}
.tab-layout-wrapper{padding-bottom:1rem;height:100%;overflow-y:hidden;display:grid;grid-template-columns:160px 1fr;-webkit-box-align:stretch;-webkit-align-items:stretch;-ms-flex-align:stretch;align-items:stretch;}
@media (max-width:767px),(max-height:440px){
.tab-layout-wrapper{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;}
}
.tab-page{overflow-y:auto;overflow-x:hidden;height:100%;padding:1.125rem 1.25rem 3rem;}
.tab-page::-webkit-scrollbar{width:.5em;height:.5em;}
.tab-page::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.tab-page::-webkit-scrollbar-track{background:var(--cp-color-18);}
.tab-page h3{height:0;overflow:hidden;margin:0;}
.tab-page>*:last-child{padding-bottom:1rem;}
.tab-page p a:not(.button){border-bottom:1px solid var(--cp-color-link-on-black);}
.tab-page p a:not(.button):hover,.tab-page p a:not(.button):focus{color:var(--cp-color-link-on-black);border-bottom:none;}
.tab-layout .ios-toggle{margin-left:0;}
.tab-layout .ios-toggle input+label{pointer-events:none;}
.tab-layout .ios-toggle-mega-label{text-transform:none;letter-spacing:0;margin:.125rem 0 0 3.75rem;}
.tab-layout .ios-toggle-mega-label::after{opacity:1;content:'Off';}
.tab-layout .ios-toggle>input:checked~.ios-toggle-mega-label::after{content:'On';}
.tab-layout .radio-list{list-style:none;color:var(--cp-color-6);}
.tab-layout .top-label-form label.small-inline{text-transform:none;margin:0;vertical-align:top;line-height:1.6;font-size:1rem;letter-spacing:0;margin-left:.25rem;}
.settings-nub svg{-webkit-transition:-webkit-transform .4s;transition:-webkit-transform .4s;transition:transform .4s;transition:transform .4s,-webkit-transform .4s;}
.item-settings-modal{z-index:201;}
.item-settings-modal::before{display:none;}
.settings p a{border-bottom:1px solid var(--cp-color-link-on-black);}
.settings p a:hover,.settings p a:focus{color:var(--cp-color-link-on-black);border-bottom:none;}
.item-settings-modal .ios-toggle{margin-left:0;}
.item-settings-modal .ios-toggle input+label{pointer-events:none;}
.item-settings-modal .ios-toggle-mega-label{text-transform:none;letter-spacing:0;margin:.125rem 0 0 3.75rem;}
.item-settings-modal .ios-toggle-mega-label::after{opacity:1;content:'Off';}
.item-settings-modal .ios-toggle>input:checked~.ios-toggle-mega-label::after{content:'On';}
.item-settings-modal .radio-list{list-style:none;color:var(--cp-color-6);}
.item-settings-modal .top-label-form label.small-inline{text-transform:none;margin:0;vertical-align:top;line-height:1.6;font-size:1rem;letter-spacing:0;margin-left:.25rem;}
.insecure-resource-tooltip{background:var(--cp-color-red);position:absolute;top:6px;right:28px;width:25px;height:25px;line-height:25px;color:var(--cp-color-1);font-size:18px;text-align:center;border-radius:3px;display:none;}
.insecure-resource-tooltip .help-flyout-link{top:0;left:0;width:100%;height:100%;cursor:pointer;}
.insecure-resource-tooltip .icon-help{width:100%;position:absolute;left:0;cursor:pointer;}
.external-resource-url-row{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;width:100%;margin-bottom:.5rem;position:relative;}
.external-resource-url-row .move-external-url{cursor:pointer;margin:10px 5px 0 0;height:17px;}
.external-resource-url-row .move-external-url svg{fill:var(--cp-color-10);}
.external-resource-url-row input{border-radius:4px;padding:12px 10px;overflow:hidden;white-space:nowrap;text-overflow:ellipsis;}
.external-resource-url-row .external-url-option{background:var(--cp-color-4);display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-pack:center;-webkit-justify-content:center;-ms-flex-pack:center;justify-content:center;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;text-align:center;border-radius:0 4px 4px 0;width:20px;height:18px;margin-bottom:2px;border-bottom:none;cursor:pointer;}
.external-resource-url-row .external-url-option svg{height:10px;fill:var(--cp-color-10);}
.external-resource-actions .add-resource{margin-left:25px;margin-top:-10px;position:relative;}
.external-resource{padding:7px!important;border-radius:3px 0 0 3px;}
.remove-external-url,.external-resource{vertical-align:middle;}
.external-url-option{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;-webkit-box-pack:center;-webkit-justify-content:center;-ms-flex-pack:center;justify-content:center;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;border:0;cursor:pointer;height:calc(50% - 1px);width:20px;padding:4px 0;border-radius:0 3px 3px 0;position:relative;background:var(--cp-color-4);}
.external-url-option svg{-webkit-box-flex:1;-webkit-flex:1;-ms-flex:1;flex:1;position:relative;width:12px;height:12px;fill:var(--cp-color-11);pointer-events:none;}
.remove-external-url:hover{background:var(--cp-color-20);}
.remove-external-url:hover svg{fill:var(--cp-color-red);}
.open-external-url{text-decoration:none;border:0;}
.open-external-url:hover{background:var(--cp-color-20);}
.open-external-url:hover svg{fill:var(--cp-color-1);}
.open-external-url[href='']{display:none;}
.resource-actions{margin:3px 0;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;-webkit-box-pack:center;-webkit-justify-content:center;-ms-flex-pack:center;justify-content:center;-webkit-box-align:start;-webkit-align-items:flex-start;-ms-flex-align:start;align-items:flex-start;}
.resource-actions a{padding:4px 10px;}
.custom-select-wrap{margin-bottom:0;}
.custom-select-wrap select{background:var(--cp-color-4);font-size:14px;font-family:var(--cp-font-family);color:var(--cp-color-11);padding:0 12px;-webkit-appearance:none;outline:0;border-radius:4px;}
.custom-select-wrap select:focus{border-color:3px solid #616574;}
.algolia-shoutout{font-size:.8rem;text-align:right;margin:-3px 0 5px;}
.algolia-shoutout img{width:45px;vertical-align:middle;position:relative;top:-1px;}
.algolia-shoutout a{border-bottom:none;background:var(--cp-color-4);padding:1px 5px;border-radius:0 0 2px 2px;color:var(--cp-color-link-on-white);}
.algolia-autocomplete{position:static!important;-webkit-box-flex:1;-webkit-flex:1;-ms-flex:1;flex:1;}
.aa-dropdown-menu{width:100%;background:var(--cp-color-14);color:var(--cp-color-1);margin-top:-4px;}
.settings-row{color:var(--cp-color-1);position:relative;margin:0 0 1rem;padding:1rem;background:-webkit-gradient(linear,left top,right top,from(var(--cp-color-15)),to(var(--cp-color-17)));background:linear-gradient(to right,var(--cp-color-15),var(--cp-color-17));border-left:3px solid var(--cp-color-13);}
.settings-row h4{font-family:var(--cp-font-family);text-transform:none;margin:0 0 4px;font-size:1rem;}
.settings-row p{color:var(--cp-color-6);font-size:1rem;line-height:1.4;margin-bottom:.75em;}
.settings-row p a{color:var(--cp-color-link-on-black);border-color:var(--cp-color-link-on-black);}
.settings-row p a:hover,.settings-row p a:focus{color:var(--cp-color-blue);border-color:var(--cp-color-blue);}
.settings-row:last-child,.settings-row>*:last-child{border-bottom:0;margin:0;}
.item-settings-javascript{padding-bottom:400px!important;}
.head-content{min-height:100px;resize:vertical;}
#meta-tag-insert{display:inline-block;font-size:.85rem;margin:0;cursor:pointer;}
.css-preprocessor{margin:0 0 10px;}
.add-ons{padding-top:1rem;}
.add-ons h5{margin:0 0 3px;}
#need-an-addon{margin:0;}
.need-an-addon-button{border-bottom:none!important;position:absolute;top:0;right:25px;color:var(--cp-color-1)!important;}
.add-ons-container{border-radius:3px;background:var(--cp-color-14);position:relative;}
input.add-ons-filter[type=text]{font-size:1rem;border-radius:4px 4px 0 0;}
.add-ons-clear-filter{position:absolute;width:39px;height:39px;top:0;right:0;cursor:pointer;display:none;}
.add-ons-clear-filter .icon-x{width:14px;height:14px;fill:var(--cp-color-6);margin:12px;}
.add-ons-scroll{height:130px;overflow-y:scroll;border-radius:0 0 4px 4px;}
.add-ons-scroll::-webkit-scrollbar{width:.5em;height:.5em;}
.add-ons-scroll::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.add-ons-scroll::-webkit-scrollbar-track{background:0 0;}
.add-ons-list{list-style:none;background:var(--cp-color-5);padding-bottom:5px;}
.add-ons-list li{position:relative;padding:4px 5px 4px 10px;color:var(--cp-color-13);border:none;}
.add-ons-list li.depends-on{padding-left:30px;}
.add-ons-list li.depends-on .add-on-code::before{content:'↳ ';color:var(--cp-color-10);}
.add-ons-list li .help-flyout-link{display:inline-block;right:10px;top:7px;width:14px;height:14px;}
.add-ons-list li .help-flyout-link .icon-help{fill:var(--cp-color-8);}
.add-ons-list li .add-add-on{font-size:.7rem;position:absolute;right:20px;top:6px;padding:2px 5px;border:0;}
.add-ons-list li .add-add-on:hover,.add-ons-list li .add-add-on:focus{cursor:pointer;color:var(--cp-color-1);}
.add-ons-list li:hover,.add-ons-list li:focus{cursor:pointer;color:var(--cp-color-1);background:var(--cp-color-13);}
.CodeMirror-foldgutter{width:.7em;}
.CodeMirror-foldgutter-open{cursor:pointer;}
.CodeMirror-foldgutter-open::after{content:"\25BE";}
.console-wrap{height:calc(100% - 36px);position:relative;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;}
.console-entries{padding:0;margin:0;width:100%;overflow-y:auto;height:100%;}
.console-entries::-webkit-scrollbar{width:.5em;height:.5em;}
.console-entries::-webkit-scrollbar-thumb{background:var(--cp-color-11);}
.console-entries::-webkit-scrollbar-track{background:0 0;}
.console-arrow{font-weight:700;padding-left:10px;}
.console-arrow.forwards{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;}
.console-arrow.forwards::before{content:'>';}
.console-command-line{background:rgba(255,255,255,.1);padding:0 8px 0 0;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-flex-shrink:0;-ms-flex-negative:0;flex-shrink:0;}
.console-command-line-input{background:0 0;-webkit-box-flex:1;-webkit-flex:1;-ms-flex:1;flex:1;color:var(--cp-color-1);border:0;padding:7px 0 7px 7px;resize:none;overflow:hidden;min-height:30px;}
.console-command-line-input:disabled{pointer-events:none;}
.console-command-line-input:focus{background:0 0;}
.main-header>.header-wrap{border-bottom:1px solid var(--resizer-border,var(--cp-color-16));}
span.inline-note{color:#ffdc40;}
h4.inline-tour{margin-top:1rem;}
.inline-editor-commands{padding-right:10px;}
p.inline-tab-triggers{margin:20px 0 0;}
.tabs{padding-bottom:40px;position:relative;}
.tabs>div{clear:both;display:none;}
.tabs>div.active{display:block;}
body{overflow:hidden;}
body{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;padding-bottom:30px;}
.page-wrap{padding:0;-webkit-box-flex:1;-webkit-flex-grow:1;-ms-flex-positive:1;flex-grow:1;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;width:100%;}
.boxes{position:absolute;width:100%;height:100%;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;}
.top-boxes{position:relative;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;overflow:hidden;}
@media (max-width:767px),(max-height:440px){
.top-boxes .box-html.switch-off,.top-boxes .box-css.switch-off,.top-boxes .box-js.switch-off{visibility:hidden;position:absolute;}
}
.top-boxes .box{height:100%;position:relative;overflow:hidden;}
.top-boxes .box .code-wrap{overflow:hidden;}
@media (max-width:767px),(max-height:440px){
.CodeMirror{font-size:10px!important;}
}
.editor-actions-left{-webkit-box-flex:1;-webkit-flex:1 1 auto;-ms-flex:1 1 auto;flex:1 1 auto;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;}
.link-list{list-style:none;}
.link-list button{color:var(--cp-color-20);display:block;width:100%;text-align:left;border-radius:0;padding:7px 15px 8px;line-height:1.1;font-size:.9rem;text-shadow:none;text-decoration:none;}
.link-list button:hover,.link-list button:focus{color:inherit;background:#e7e8f1;}
.powers{background:var(--editor-top-bar-background);white-space:nowrap;position:relative;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;padding-right:.5rem;}
.powers .editor-actions-right{margin-left:auto;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;}
.powers-drag-handle{display:none;position:absolute;width:100%;height:100%;left:0;top:0;z-index:0;}
.editor-resizer,.resizer{background:var(--resizer-background);border:solid 1px var(--resizer-border);-webkit-box-sizing:border-box;box-sizing:border-box;}
.layout-top .editor-resizer{border-top:none;border-bottom:none;}
.layout-top .editor-resizer:first-child{border-left:none;}
.layout-top .editor-resizer:first-child .box-title{margin-left:1px;}
.layout-top .resizer{border-left:none;border-right:none;}
.box-title{font-family:var(--cp-font-family);border-top:3px solid transparent;white-space:nowrap;font-weight:700;color:var(--cp-color-8);margin:0;font-size:1.1rem;line-height:1;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;padding:9px 12px;}
.editor-resizer:not(.is-horiz-skinny) .box-title{background:var(--tab-bg);border-top:3px solid var(--tab-border-color);}
.box-title-preprocessor-name{font-size:80%;margin-left:.2rem;font-weight:400;}
.file-type-icon{width:17px;height:17px;-webkit-margin-end:.4rem;margin-inline-end:.4rem;}
.code-editor-status::after{position:absolute;right:13px;top:47px;font-size:10px;font-weight:400;background:var(--cp-color-green);color:var(--cp-color-20);display:inline-block;padding:0 5px;border-radius:2px;visibility:hidden;opacity:0;-webkit-transition:visibility 0s linear .2s,all .2s linear;transition:visibility 0s linear .2s,all .2s linear;z-index:1;}
.editor-dropdown{right:0;z-index:100;margin-top:5px;}
@media (max-width:767px),(max-height:440px){
.editor-dropdown{width:auto;}
}
.code-wrap{overflow:hidden;height:100%;height:calc(100% - 36px);}
.code-wrap .CodeMirror-sizer{min-width:200px;}
.output-container{-webkit-box-flex:1;-webkit-flex-grow:1;-ms-flex-positive:1;flex-grow:1;position:relative;}
.output-sizer{position:absolute;left:0;top:0;width:100%;height:100%;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;}
.result{position:relative;-webkit-box-flex:1;-webkit-flex-grow:1;-ms-flex-positive:1;flex-grow:1;overflow:hidden;background:radial-gradient(circle,var(--cp-color-13),var(--cp-color-14));}
.result-iframe{border:0;background:var(--cp-color-1);width:100%;height:100%;position:absolute;top:0;left:0;z-index:1;}
.drag-cover{position:absolute;z-index:2;top:0;right:0;left:0;bottom:0;display:none;}
.width-readout{position:absolute;z-index:50;background:var(--cp-color-6);color:var(--cp-color-13);padding:4px 8px;border-radius:10px;font-size:9px;-webkit-transform:translate(-50%,-50%);transform:translate(-50%,-50%);-webkit-box-shadow:0 1px 1px rgba(0,0,0,.5);box-shadow:0 1px 1px rgba(0,0,0,.5);opacity:0;visibility:hidden;-webkit-transition:opacity .1s;transition:opacity .1s;}
.box-console{overflow:hidden;display:none;height:30%;}
@media (min-width:1101px){
.keyboard-commands-button::after{content:'Keys';margin-left:.125rem;}
}
html:not(.mac) .keyboard-commands-button::after{content:'Shortcuts';}
html:not(.mac) .keyboard-commands-button>span{display:none;}
.navigation-wrap{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:center;-webkit-align-items:center;-ms-flex-align:center;align-items:center;}
@media (max-width:550px){
.embed-modal-button,.keyboard-commands-button{display:none!important;}
}
@media (max-width:767px),(max-height:440px){
.embed-modal-button{display:none!important;}
}
.mobile-editor-nav{display:none;}
@media (max-width:767px),(max-height:440px){
body{min-width:320px;-ms-touch-action:manipulation;touch-action:manipulation;}
#resizer,.editor-resizer{display:none;}
.editor-dropdown .maximize-button,.editor-dropdown .minimize-button{display:none;}
body.editor .boxes{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-webkit-flex-direction:column;-ms-flex-direction:column;flex-direction:column;height:100%;}
body.editor .top-boxes{display:block;width:100%!important;height:40vh;min-height:2em;}
body.editor .top-boxes .box-title{visibility:hidden;}
.boxes.mobile-hide-code .top-boxes{height:40px;}
.box{width:100%!important;height:100%!important;}
.code-wrap{padding:5px 10px 0;}
.mobile-editor-nav{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-align:end;-webkit-align-items:end;-ms-flex-align:end;align-items:end;position:absolute;z-index:1;padding-left:.5rem;text-align:center;width:100%;top:8px;height:32px;overflow:hidden;pointer-events:none;}
.mobile-editor-nav button{display:block;pointer-events:auto;margin:0;margin-right:1px;padding:8px 16px;min-width:50px;background:var(--cp-color-14);color:var(--cp-color-1);border:none;border-top:2px solid var(--cp-color-13);-webkit-box-sizing:border-box;box-sizing:border-box;cursor:pointer;}
.mobile-editor-nav button.selected{border-top:2px solid var(--cp-color-5);background:var(--cp-color-13);}
.mobile-editor-nav button:first-child{border-top-left-radius:2px;}
.mobile-editor-nav button:last-child{border-top-right-radius:2px;margin-right:0;}
.powers{height:40px;}
.settings-nub,.editor-dropdown-button{z-index:2;padding:6px 8px;}
.settings-nub svg,.editor-dropdown-button svg{top:0;width:14px;height:14px;}
.editor-dropdown-button svg{margin-right:0!important;}
.output-container{border-top:1px solid var(--cp-color-13);}
body.editor{padding-bottom:0;}
.site-footer{position:relative;height:auto;}
.footer-left,.footer-right{padding:4px 0;}
.site-footer .keyboard-commands-button{display:none;}
}
@media (max-width:767px) and (orientation:landscape),(max-height:440px) and (orientation:landscape){
body.editor .boxes{display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-box-orient:horizontal;-webkit-box-direction:normal;-webkit-flex-direction:row;-ms-flex-direction:row;flex-direction:row;-webkit-box-align:stretch;-webkit-align-items:stretch;-ms-flex-align:stretch;align-items:stretch;}
body.editor .top-boxes{min-height:60px;height:100%!important;width:50%!important;}
.boxes.mobile-hide-code .top-boxes{width:0!important;}
.mobile-editor-nav{width:50%;z-index:5;}
.mobile-hide-code .mobile-editor-nav{-webkit-box-pack:start;-webkit-justify-content:flex-start;-ms-flex-pack:start;justify-content:flex-start;left:5px;}
.mobile-hide-code .mobile-editor-nav button{display:none;}
.mobile-hide-code .mobile-editor-nav #result-toggle{display:inline-block;}
.mobile-hide-code .mobile-editor-nav #html-toggle{display:inline-block;border-radius:2px;}
.mobile-hide-code .mobile-editor-nav #html-toggle span{display:none;}
.mobile-hide-code .mobile-editor-nav #html-toggle::before{content:'Code';}
.box{width:100%!important;}
.powers{height:40px;}
.output-container{border:none;border-left:1px solid var(--cp-color-13);}
body.editor .main-header .header-wrap{border-bottom:1px solid #444857;}
}
}
/*! CSS Used from: https://cpwebassets.codepen.io/assets/editor/themes/twilight-f15048ee49783cd27718c33661cb85565f285778b4899097ae7b0c620f0445d2.css ; media=screen */
@media screen{
.sidebar-false .main-header,.sidebar-false .main-header .header-wrap,.editor-footer{background:var(--editor-top-bar-background);}
.editor-footer{border-top-color:var(--resizer-border,var(--cp-color-6));}
.cm-keyword{color:#ddca7e;}
.cm-atom{color:#ddca7e;}
.cm-number{color:#d0782a;}
.cm-def{color:#809bbd;}
.cm-variable{color:#ddca7e;}
.cm-variable-2{color:#809bbd;}
.cm-property{color:#9a8297;}
.cm-operator{color:#ccc;}
.cm-comment{color:#717790;}
.cm-string{color:#96b38a;}
.cm-tag{color:#a7925a;}
.cm-attribute{color:#ddca7e;}
body.editor{background:#1d1e22;}
.box.box.box,.editor .top-boxes,.CodeMirror-gutter-wrapper{background:#1d1e22;}
.box.box.box pre,.editor .top-boxes pre{color:#fff;}
.CodeMirror-guttermarker-subtle,.CodeMirror-linenumber{color:#34363e;}
.CodeMirror-simplescroll-horizontal div,.CodeMirror-simplescroll-vertical div{background:#666b7a;}
}
/*! CSS Used from: Embedded */
.CodeMirror,.console-command-line-input{font-family:SFMono-Regular, Consolas, Liberation Mono, Menlo,   monospace;}
/*! CSS Used from: Embedded */
.CodeMirror,.console-command-line-input{font-size:15px;}
/*! CSS Used from: Embedded */
#sessionUserAvatar{background-image:url(https://assets.codepen.io/t-1/user-default-avatar.jpg?fit=crop&format=auto&height=80&version=0&width=80);}
</style>