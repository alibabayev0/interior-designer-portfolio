<template>
  <Header />
  <router-view />
</template>

<script>
import Header from './components/Header'
export default {
  components:{
    Header
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
