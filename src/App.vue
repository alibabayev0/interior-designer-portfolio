<template>
  <Header />
  <router-view />
  <Footer />
</template>

<script>
import Header from './components/Header'
import Footer from './components/Copyright'
export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700;800&display=swap');

html,
body {
  margin: 0px !important;
  padding: 0px !important;
  background-color: #eeece5;
}

button,
a { 
  outline: none;
}
::-webkit-scrollbar {
  width: 20px;
}

::-webkit-scrollbar-track {
  background-color: transparent;
}

::-webkit-scrollbar-thumb {
  background-color: #1c1c1d;
  border-radius: 20px;
  border: 6px solid transparent;
  background-clip: content-box;
}

p {
  font-family: Poppins, sans-serif;
}
</style>
