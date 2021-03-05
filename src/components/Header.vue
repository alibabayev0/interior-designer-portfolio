<template>
  <div class="container">
    <div class="logo"><p>GUNAY BABAYEVA</p> 
      <div class="menu" v-on:click="navbar_open">
        <div class="menu-item"></div>
        <div class="menu-item"></div>
        <div class="menu-item"></div>
      </div>
    </div>
    <ul class="navbar" ref="navbar">
      <li class="nav-list">
        <router-link to="/">
            Home
        </router-link>
      </li>
      <li class="nav-list">
        <router-link to="/About">
            About
        </router-link>
      </li>
      <li class="nav-list">
        <router-link to="/Service">
            Service
        </router-link>
      </li>
      <li class="nav-list">
        <router-link to="/Portfolio">
            Portfolio
        </router-link>
      </li>
      <li class="nav-list">
        <router-link to="/Resume">
            Resume
        </router-link>
      </li>
      <li>
        <button class="contact-us">Contact Us</button>
      </li>
    </ul>
 
    
  </div>

</template>


<style lang="css" scoped>

*,html {
  margin: 0;
  padding: 0;
  /* border: 1px solid red; */
}

.logo {
  font-family: Poppins,sans-serif;
  font-weight: 300;
}

.container {
  padding: 1em 5em 1em 5em;
  display:flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  border-bottom: 1px solid black  ;
}

.logo {
  display: flex;
  font-size: 24px;
}


.navbar {
  display: flex;
  justify-items: center;
  align-items: center;
  list-style: none;
  margin:0;
}

.nav-list {
  margin: 1.5em;
  align-items: center;
}

.nav-list a{
  text-decoration: none;
  display: block;
  color:#1C1C1D;
  font-family: 'Poppins',sans-serif;
  font-weight: 400;
  font-size: 16px;
}


.nav-list a::after {
    content: '';
    display: block;
    width: 0;
    height: 1.5px;
    background: #000;
    transition: width 1s;
}

.nav-list a:hover::after {
    width: 100%;
    transition: width .3s;
}


/* .navigation li a.router-link-exact-active{
  font-weight: 550;
} */

.contact-us {
  width: 130px;
  height: 40px;
  background: #F8F8F8;
  border: 0.5px solid #1C1C1D;
  font-weight: 700;
  border-radius: 30px;
  -webkit-box-shadow: 0px 0px 24px -10px rgba(0,0,0,0.75);
  -moz-box-shadow: 0px 0px 24px -10px rgba(0,0,0,0.75);
  box-shadow: 0px 0px 24px -11px rgba(0,0,0,0.75);
  cursor: pointer;
}

.menu {
  display: none;
}

.menu:hover{
  cursor: pointer;
}

.menu-item{
  width: 20px;
  height: 3px;
  background-color: #1c1c1d;
  margin-bottom: 3px;
}


@media (max-width: 575.98px) { 

}

 /* Small devices (landscape phones, less than 768px) */
@media (max-width: 767.98px) { 

}

/* // Medium devices (tablets, less than 992px) */
@media (max-width: 991.98px) { 
  
}
/* // Large devices (desktops, less than 1200px) */
@media (max-width: 1199.98px) { 

}

@media (max-width: 1035.98px) { 
  .container{
    flex-direction: column;
  }

  .logo {
    display: flex;
    align-items: center; 
    width: 100%;
    text-align: center;
    justify-content: center;
    align-content: center;
    justify-content:space-between ;
    font-size: 24px;
  }

  .navbar{
    flex-direction: column;
    display: block;
  }
  .nav-list{
    padding: 0;
    margin: 15px 0 15px 0;
    text-align: center;
  }
  .menu {
    display: block;
  }
  .navbar {
    display: none;
  }
  .active {
    display: block;
  }
}



</style>

<script>
export default {
  
  methods:{
    navbar_open: function(){
      this.$refs.navbar.classList.toggle('active');
    } 
  },
}
</script>