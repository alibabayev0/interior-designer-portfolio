<template>
  <Header />
  <router-view />
  <Footer/>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Copyright'
export default {
  components:{
    Header,
    Footer
  }
}
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700;800&display=swap');


html,body {
  margin: 0px !important;
  padding: 0px !important;
  background-color: #EEECE5;
}

p {
  font-family: Poppins,sans-serif;
}

</style>
