<template>
  <footer class="footer" id="custom-footer">
    <div class="to-top logo" @click="scrollTopTop"> 
    
    
    
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 13.3 10.5" xml:space="preserve"><defs></defs><path d="M12.3,9.5H5.3C2.9,9.5,1,7.6,1,5.3V1h7.1c2.3,0,4.3,1.9,4.3,4.3V9.5z" class="st0"></path></svg>

 </div>
    <div class="social">
      <a
        class="channel"
        v-for="(social, index) in data.social"
        :key="index"
        :href="`https://${social.channel}.com/${social.handle}`"
      >
        {{ social.link_text }}
      </a>
    </div>


  
 
  <div class="links">
    <a href="#">Terms & Conditions</a>
    <a href="#">Contact</a>
    <a href="#">Support</a>
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
.to-top {
  transform: rotate(-90deg);
  user-select: none;
  cursor: pointer;
  border: 2px solid transparent;
  text-align: center;
  font-weight: 700;
  line-height: 0;
  padding: 1rem 0.5rem;
  &:hover {
    border: 2px solid white;
  }
}
.social {
  .channel {
    margin-right: 1rem;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    &:last-of-type {
      margin: 0;
    }
  }
}











#custom-footer {
  padding: 20px 40px;
  color: #888;
  font-size: 14px;
}
footer .logo {
  max-width: 150px;
  display: inline-block;
}
footer .logo svg {
  max-width: 100%;
    width: 20px;
    stroke: #fff;
    fill: transparent;
    stroke-width: 2;
}
#custom-footer > div {
  position: relative;
  top: 2px;
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
#custom-footer .links a:hover {
  color: #ddd;
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

a:hover {
  text-decoration: none;
}

</style>