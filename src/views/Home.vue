<template>
  <iam-gunay></iam-gunay>
  <div class="space" />
  <about-me></about-me>
  <div class="space" />
  <my-works></my-works>
  <div class="space" />
  <contact-us></contact-us>
</template>

<style lang="css" scoped>
.space {
  height: 2vw;
  border-bottom: 1px solid black;
  border-top: 1px solid black;
}
</style>

<script>
import AboutMe from '../components/AboutMeCard.vue'
import ContactUs from '../components/ContactUsCard.vue'
import IamGunay from '../components/IamGunay.vue'
import MyWorks from '../components/MyWorks.vue'
export default {
  components: {
    IamGunay,
    AboutMe,
    MyWorks,
    ContactUs
  }
}
</script>
, ContactUs
