<template>
  <footer class="footer" id="custom-footer">
    <div class="logo" @click="scrollTopTop"> 
    
    
    
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 13.3 10.5" xml:space="preserve"><defs></defs><path d="M12.3,9.5H5.3C2.9,9.5,1,7.6,1,5.3V1h7.1c2.3,0,4.3,1.9,4.3,4.3V9.5z" class="st0"></path></svg>

 </div>
    <div class="links">
      <a
        v-for="(social, index) in data.social"
        :key="index"
        :href="`https://${social.channel}.com/${social.handle}`"
      >
        {{ social.link_text }}
      </a>
    </div>


  

  

  </footer>
</template>

<script>
import data from "@/data/theme.json";

export default {
  data() {
    return {
      data
    };
  },
  methods: {
    scrollTopTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    }
  }
};
</script>

<style lang="scss">
.footer {
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 0 2rem;
  z-index: 100;
}












#custom-footer {
  padding: 20px 40px;
  color: #888;
  font-size: 14px;
}

#custom-footer > div {
  position: relative;
  top: 2px;
}
#custom-footer .logo svg {
  height: 100%;
  stroke: #fff;
  padding: 3px;
  fill: none;
  stroke-width: 2;
}

#custom-footer .links {
  float: right;
  margin-left: 30px;
}
#custom-footer .links a {
  color: #bbb;
  display: inline-block;
  margin-left: 20px;
}

#custom-footer .links a:first-of-type {
  margin-left: 0px;
}
@media screen and (max-width: 880px) {
  #custom-footer {
    overflow: hidden;
  }
  #custom-footer > div {
    top: 0px;
  }
  #custom-footer .links {
    margin-left: 0px;
  }
  #custom-footer .meta {
    float: left;
  }
  #custom-footer .logo {
    display: none;
  }
}
@media screen and (max-width: 600px) {
  #custom-footer {
    text-align: center;
    font-size: 13px;
    line-height: 20px;
  }
  #custom-footer .meta, #custom-footer .links {
    float: none;
  }
  #custom-footer .links {
    margin-bottom: 5px;
  }
}


</style>