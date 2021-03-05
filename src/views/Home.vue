<template>
  <iam-gunay></iam-gunay>
  <div class="space"/>
  <about-me></about-me>
  <div class="space"/>
  <my-works></my-works>
  <div class="space"/>
  <contact-us></contact-us>
  <copyright id="copyright"></copyright>
</template>

<style lang="css" scoped>
  


.space {
  height:2vw; 
  border-bottom: 1px solid black;
  border-top: 1px solid black;
      background:url(
  data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAICAYAAADED76LAAAAMklEQVQoU2NkwA/+M+KR/8/AwMCISwFYEqQZmwK4JDYFKJLoCjAkkRVglYQpwCkJUgAAGOQICDcTvB4AAAAASUVORK5CYII=
    ) repeat;
}

#copyright{
  margin-top: 60px;
  margin-bottom: 10px;
}

</style>

<script>
import AboutMe from '../components/AboutMe.vue';
import ContactUs from '../components/ContactUs.vue';
import IamGunay from '../components/IamGunay.vue';
import MyWorks from '../components/MyWorks.vue';
import Copyright from '../components/Copyright.vue';
export default {
  components:{
    IamGunay,
    AboutMe,
    MyWorks,
    ContactUs,
    Copyright
  }
}
</script>,
    ContactUs