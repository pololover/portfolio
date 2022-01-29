<template>
  <div class="introd_wrap">
      <!-- header -->
      <div class="header_content">
        <div class="header_title">
          SeungHyun's portfolio
        </div>
        <div class="header_nav">
          <span class="header_nav_ele" @click="moveAbout">About me</span>
          <span class="header_nav_ele" @click="moveSkills">Skills</span>
          <span class="header_nav_ele" @click="moveProject">Projects</span>
          <span class="header_nav_ele" @click="moveContact">Contact</span>
        </div>
        <div class="dropdown">
          <button class="menu_bar" @click.stop="DropDown">
              <i class="fas fa-bars menu_bar"></i>
          </button>
          <div class="dropdown-content" v-if="DropState">
            <div @click="moveAbout">About</div>
            <div @click="moveSkills">Skills</div>
            <div @click="moveProject">Project</div>
            <div @click="moveContact">Contact</div>
          </div>
        </div>
      </div>
      <!-- body_title -->
      <div class="body_title_ani">
      웹 프론트엔드 개발자 천승현입니다. 
      </div>      
    </div>
</template>
<script>
export default {
  data() {
    return {
      DropState : false,
    }
  },
  methods: {
    DropDown : function() {
      if(this.DropState){
        this.DropState = false;
      }else {
        this.DropState = true;
      }
    },
    moveAbout : function(){
      this.DropState=false;
      const menuHeight = document.querySelector('.header_nav').offsetHeight
      const myworksLocation = document.querySelector('.About_wrap').offsetTop
      scrollTo({ top: myworksLocation - menuHeight-30, behavior: 'smooth' })
    },
    moveSkills : function() {
      this.DropState=false;
      const menuHeight = document.querySelector('.header_nav').offsetHeight
      const myworksLocation = document.querySelector('.Skills_wrap').offsetTop
      scrollTo({ top: myworksLocation - menuHeight-40, behavior: 'smooth' })
    },
    moveProject : function() {
      this.DropState=false;
      const menuHeight = document.querySelector('.header_nav').offsetHeight
      const myworksLocation = document.querySelector('.Project_wrap').offsetTop
      scrollTo({ top: myworksLocation - menuHeight-63, behavior: 'smooth' })
     },
    moveContact : function() {
      this.DropState=false;
      const menuHeight = document.querySelector('.header_nav').offsetHeight
      const myworksLocation = document.querySelector('.contact_wrap').offsetTop
      scrollTo({ top: myworksLocation - menuHeight, behavior: 'smooth' })
     },
  }
}
</script>
<style>
  
</style>