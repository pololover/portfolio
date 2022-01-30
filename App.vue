<template>
  <div class="wrap" @click="DropState=false">
    <!--introduce section-->
    <Introduce ref="introduce" :scrollTop="scrollTop" :DropState="DropState" @DropState="DropChange"></Introduce>
    <!-- About me -->
    <About></About>
    <!-- skills-->
    <Skill ref="skill_imgs" :scrollTop="scrollTop"></Skill>
    <!-- Projects -->
    <project ref="project" :scrollTop="scrollTop"></project>
    <!-- Contact -->
    <contact></contact>
  </div>
</template>

<script>
import Introduce from './components/introduce.vue'
import About from './components/About.vue'
import Skill from './components/skill.vue'
import Project from './components/project.vue'
import Contact from './components/contact.vue'
export default {
  name: 'App',
  components: {
    Introduce,
    About,
    Skill,
    Project,
    Contact,
  },
  data(){
    return {
      scrollTop : 0,
      scrollProject : 0,
      scrollDiary : 0,
      scrollHealth : 0,
      DropState : false,
    }
  },
  methods: {
    scrollEvent : function(){
      this.scrollTop = document.documentElement.scrollTop;
      this.$refs.introduce.bar_move();
      this.$refs.skill_imgs.get_refs();
      this.$refs.project.get_scroll_ani();
    },
    DropChange : function(bol){
      this.DropState = bol;
    }
  },
  mounted() {
    window.scrollTo(0, 0);
    document.addEventListener('scroll', this.scrollEvent);
  }
}
</script>
<style src="@/assets/style/style.css">
</style>
<style lang="scss" src="@/assets/style/sstyle.scss">
</style>