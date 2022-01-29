<template>

  <div class="wrap" @click="DropState=false">
    <!--introduce section-->
    <Introduce></Introduce>
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
    }
  },
  computed : {
    focusState(){
      return this.$store.state.focusState
    }
    
  },
  methods: {
    scrollEvent : function(){
      this.scrollTop = document.documentElement.scrollTop;
      console.log(this.scrollTop);
      this.$refs.skill_imgs.get_refs();
      this.$refs.project.get_scroll_ani();
    },
  },
  mounted() {
    document.addEventListener('scroll', this.scrollEvent);
  }
}
</script>
<style src="@/assets/style/style.css">
</style>
<style lang="scss">
@import "@/assets/style/sstyle.scss"
</style>