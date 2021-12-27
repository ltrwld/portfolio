<template>
  <footer class="footer" id="custom-footer">
   
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
}
@media screen and (max-width: 600px) {
  #custom-footer {
    text-align: center;
    font-size: 13px;
    line-height: 20px;
  }
  #custom-footer .links {
    float: none;
  }
  #custom-footer .links {
    margin-bottom: 5px;
  }
}

</style>