<template>
  <header class="header">
 
     

    
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="92.3px"
	 height="10.5px" viewBox="0 0 92.3 10.5" style="overflow:visible;enable-background:new 0 0 92.3 10.5;" xml:space="preserve">

<g>
	<path class="st0" d="M16.8,0.2h1.8v10.1h-1.8V0.2z"/>
	<path class="st0" d="M27.6,3.2v7.1h-1.8V9.5c-0.6,0.6-1.4,1-2.3,1c-2,0-3.5-1.6-3.5-3.7C20,4.6,21.5,3,23.5,3c1,0,1.8,0.4,2.3,1
		V3.2H27.6z M25.8,6.7c0-1.1-0.8-2-2-2c-1.1,0-2,0.9-2,2s0.8,2,2,2C25,8.7,25.8,7.9,25.8,6.7z"/>
	<path class="st0" d="M29.3,7.5V3.2h1.8v4c0,0.9,0.6,1.5,1.5,1.5c0.9,0,1.5-0.6,1.5-1.5v-4h1.8v4.3c0,1.8-1.3,3-3.3,3
		C30.6,10.5,29.3,9.3,29.3,7.5z"/>
	<path class="st0" d="M40,4.8v3c0,0.6,0.3,0.9,1,0.9c0.4,0,0.7-0.1,0.9-0.2v1.7c-0.4,0.2-0.8,0.3-1.3,0.3c-1.6,0-2.4-1-2.4-2.4V4.8
		H37V3.2h1.1V1.4H40v1.8h1.9v1.7H40z"/>
	<path class="st0" d="M50.1,7.4h-5.5c0.3,0.9,1,1.5,2,1.5c0.9,0,1.6-0.4,2-0.9l1.2,1.1c-0.7,0.9-1.9,1.4-3.2,1.4c-2.3,0-4-1.6-4-3.8
		c0-2.1,1.6-3.7,3.8-3.7c2.1,0,3.8,1.6,3.8,3.8C50.2,6.9,50.1,7.2,50.1,7.4z M44.6,6.1h3.6c-0.2-0.9-0.9-1.5-1.8-1.5
		C45.5,4.6,44.8,5.2,44.6,6.1z"/>
	<path class="st0" d="M55.6,3.1v1.9h-0.3c-1.3,0-2.1,0.8-2.1,2v3.4h-1.8V3.2h1.8v0.9c0.5-0.7,1.2-1,2.1-1H55.6z"/>
	<path class="st0" d="M68,3.2l-2.5,7.1h-1.9l-1.5-4.9l-1.5,4.9h-1.9l-2.5-7.1h2L59.7,8l1.5-4.8h1.9L64.6,8l1.5-4.8H68z"/>
	<path class="st0" d="M75.8,3.2v7.1H74V9.5c-0.6,0.6-1.4,1-2.3,1c-2,0-3.5-1.6-3.5-3.7c0-2.1,1.5-3.7,3.5-3.7c1,0,1.8,0.4,2.3,1V3.2
		H75.8z M74,6.7c0-1.1-0.8-2-2-2c-1.1,0-2,0.9-2,2s0.8,2,2,2C73.2,8.7,74,7.9,74,6.7z"/>
	<path class="st0" d="M77.6,0.2h1.8v10.1h-1.8V0.2z"/>
	<path class="st0" d="M88.4,0.2v10.1h-1.8V9.5c-0.6,0.6-1.4,1-2.3,1c-2,0-3.5-1.6-3.5-3.7c0-2.1,1.5-3.7,3.5-3.7c1,0,1.8,0.4,2.3,1
		V0.2H88.4z M86.5,6.7c0-1.1-0.8-2-2-2c-1.1,0-2,0.9-2,2s0.8,2,2,2C85.7,8.7,86.5,7.9,86.5,6.7z"/>
	<path class="st1" d="M89.7,9.2c0-0.7,0.5-1.3,1.3-1.3c0.7,0,1.3,0.5,1.3,1.3s-0.5,1.3-1.3,1.3C90.3,10.4,89.7,9.9,89.7,9.2z"/>
	<path class="st2" d="M12.3,9.5H5.3C2.9,9.5,1,7.6,1,5.3V1h7.1c2.3,0,4.3,1.9,4.3,4.3V9.5z"/>
</g>
</svg>





    
  
    <div class="contact">
      <a class="link" :href="`mailto:${data.email}`">say hi !</a>
    </div>
  </header>
</template>

<script>
import data from "@/data/theme.json";

export default {
  name: "Header",
  data() {
    return {
      data
    };
  },
  computed: {
    siteName() {
      return data.header_title.split(" ");
    },
    multiLine() {
      return this.siteName.length >= 1;
    }
  }
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  padding: 4rem 2rem 5rem 2rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  z-index: 100;
  opacity: 1;
  mix-blend-mode: difference;
  transition: opacity 0.5s ease;
  &.hidden {
    opacity: 0;
  }
}


.st0 {
  fill:#FFFFFF;
  }
.st1 {
  fill:#3FB288;
  }
.st2 {
  fill:none;
  stroke:#3FB288;
  stroke-width:2;
  stroke-miterlimit:10;
  }
</style>