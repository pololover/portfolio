<template>
  <div class="Skills_wrap">
      <div class="Skill_title">
        Skills
      </div>
      <div class="skill_img_padd">
        <img src="../../src/images/html.png" class="skill_img logo_imgs" ref="logo_imgs1">
        <img src="../../src/images/css.png" class="skill_img_css logo_imgs" ref="logo_imgs2">
        <img src="../../src/images/js.png" class="skill_img logo_imgs" ref="logo_imgs3">
        <img src="../../src/images/vue.png" class="skill_img_vue logo_imgs" ref="logo_imgs4">
        <img src="../../src/images/firelogo.jpg" class="skill_img_fire logo_imgs" ref="logo_imgs5">
        <img src="../../src/images/aws_logo.png" class="skill_img_fire logo_imgs" ref="logo_imgs6">
        <img src="../../src/images/github.png" class="skill_img_git logo_imgs" ref="logo_imgs7">
      </div>
      <!-- secondary skills -->
      <div class="Skill_title">
        Secondary Skills
      </div>
      <div class="skill_img_padd">
        <img src="../../src/images/python-logo.png" class="skill_img_phy logo_imgs" ref="logo_imgs8">
        <img src="../../src/images/jsp.png" class="skill_img_phy logo_imgs" ref="logo_imgs9">
        <img src="../../src/images/java_logo.png" class="skill_img_java logo_imgs" ref="logo_imgs10">
      </div>
    </div>
</template>
<script>
export default {
  props: {
    scrollTop : Number,
  },
  methods: {
    get_refs : function(){
      if (this.scrollTop >= 410) {
        this.$refs.logo_imgs1.style.visibility = 'visible';
        this.$refs.logo_imgs1.style.animation = 'right 1.3s linear';
        this.$refs.logo_imgs2.style.visibility = 'visible';
        this.$refs.logo_imgs2.style.animation = 'top 1.3s linear';
        this.$refs.logo_imgs3.style.visibility = 'visible';
        this.$refs.logo_imgs3.style.animation = 'left 1.3s linear';
        this.$refs.logo_imgs4.style.visibility = 'visible';
        this.$refs.logo_imgs4.style.animation = 'top 1.3s linear';
        this.$refs.logo_imgs5.style.visibility = 'visible';
        this.$refs.logo_imgs5.style.animation = 'left 1.3s linear';
        this.$refs.logo_imgs6.style.visibility = 'visible';
        this.$refs.logo_imgs6.style.animation = 'left 1.3s linear';
        this.$refs.logo_imgs7.style.visibility = 'visible';
        this.$refs.logo_imgs7.style.animation = 'left 1.3s linear';
      }
      //410부터

      if (this.scrollTop > 720) {
        this.$refs.logo_imgs8.style.visibility = 'visible';
        this.$refs.logo_imgs8.style.animation = 'bottom 1.3s linear';
        this.$refs.logo_imgs9.style.visibility = 'visible';
        this.$refs.logo_imgs9.style.animation = 'top 1.3s linear';
        this.$refs.logo_imgs10.style.visibility = 'visible';
        this.$refs.logo_imgs10.style.animation = 'bottom 1.3s linear';
      }
    }
  }
}
</script>
<style>
  
</style>