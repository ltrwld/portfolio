<template>
  <footer class="footer" id="custom-footer">
    <div class="to-top" @click="scrollTopTop">-></div>
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


  
  <a class="logo" href="http://www.google.c" target="_blank">
    <img src="https://s3.amazonaws.com/f.cl.ly/items/0a32453Q1V1j3n1j0E2c/acmelogo.png?v=097c22e4" alt="Acme API Co. Logo">
  </a>
  <div class="links">
    <a href="#">Terms & Conditions</a>
    <a href="#">Contact</a>
    <a href="#">Support</a>
  </div>
  <div class="meta">
    <!-- the colored dot gets an extra class and description text gets inserted via javascript -->
    <a href="http://acmeapico.statuspage.io" target="_blank">
      <span class="color-dot"></span>
      <span class="color-description"></span>
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
  position: absolute;
  bottom: 0;
  left: 0;
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













.color-dot {
  -moz-border-radius: 99px;
  -webkit-border-radius: 99px;
  border-radius: 99px;
  display: inline-block;
  width: 10px;
  height: 10px;
  margin-right: 5px;
}
.color-dot.critical {
  background-color: #e74c3c;
}
.color-dot.major {
  background-color: #e67e22;
}
.color-dot.minor {
  background-color: #f1c40f;
}
.color-dot.none {
  background-color: #2ecc71;
}

body {
  background-color: #f8f8f8;
}

.dropdown-menu .divider {
  margin: 6px 0;
}

#custom-header {
  background-color: #fff;
  padding: 24px 40px 23px;
  position: relative;
  border-bottom: 1px solid #e0e0e0;
}
#custom-header .logo-container {
  float: left;
  max-width: 325px;
}
#custom-header .logo-container img {
  max-width: 100%;
}
#custom-header nav {
  float: right;
}
#custom-header nav > a {
  margin-right: 30px;
}
#custom-header nav > a, #custom-header nav .show-dropdown {
  color: #FFF;
  display: inline-block;
  font-weight: 500;
  color: #AFAFAF;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 1px;
}
#custom-header nav .dropdown {
  display: inline-block;
}
#custom-header .dropdown-menu {
  right: 0px;
  left: auto;
}
@media screen and (min-width: 900px) {
  #custom-header nav {
    position: relative;
    top: 8px;
  }
}
@media screen and (max-width: 900px) {
  #custom-header {
    text-align: center;
    padding-left: 5%;
    padding-right: 5%;
    padding-bottom: 18px;
  }
  #custom-header .logo-container {
    float: none;
    display: block;
    margin-bottom: 18px;
    max-width: none;
  }
  #custom-header .logo-container .logo {
    max-width: 325px;
    display: inline-block;
  }
  #custom-header nav {
    float: none;
  }
  #custom-header nav > a, #custom-header .updates-dropdown-container {
    float: none;
  }
}
@media screen and (max-width: 475px) {
  #custom-header nav > a {
    margin-right: 20px;
  }
  #custom-header nav > a, #custom-header nav .show-updates-dropdown {
    font-size: 13px;
  }
  #custom-header .logo-container .logo {
    max-width: 70%;
  }
  #custom-header nav > a:nth-child(1):before {
    content: none;
  }
}

.page-content {
  text-align: center;
  font-size: 30px;
  color: #d7d7d7;
  font-weight: 500;
  letter-spacing: 2px;
}

#custom-footer {
  padding: 20px 40px;
  color: #888;
  font-size: 14px;
  background-color: #333434;
}
#custom-footer .logo {
  max-width: 150px;
  display: inline-block;
}
#custom-footer .logo img {
  max-width: 100%;
}
#custom-footer > div {
  position: relative;
  top: 2px;
}
#custom-footer .meta {
  float: right;
}
#custom-footer .meta a {
  color: #888;
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