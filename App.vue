<template>

  <div class="wrap">
    <div class="introd_wrap">
      <!-- header -->
      <div class="header_content">
        <div class="header_title">
          SeungHyun's portfolio
        </div>
        <div class="header_nav">
          <span class="header_nav_ele">About me</span>
          <span class="header_nav_ele">Skills</span>
          <span class="header_nav_ele">Projects</span>
          <span class="header_nav_ele">Career</span>
        </div>
      </div>
      <!-- body_title -->
      <div class="body_title_ani">
      웹 프론트엔드 개발자 천승현입니다. 
      </div>      
    </div>
    <!-- About me -->
    <div class="About_wrap">
      <div class="About_title">
        About me
      </div>
      <div class="About_text">
      안녕하세요 천승현입니다. 끝을 모르게 성장하고 싶습니다. 감사합니다.
      </div>
      <!-- info -->
      <div class="icons_dummy">
        <div class="icons_flex" v-for="(item, index) in user" :key="index">
          <i :class="icons[index]"></i>
          <div class="icons_flex_col">
            <span v-if="userInfo">{{userInfo[index]}}</span>
            <span>{{userInfoValue[index]}}</span>
          </div>
        </div>
      </div>
    </div>
    <!-- skills-->
    <div class="Skills_wrap">
      <div class="Skill_title">
        Skills
      </div>
      <div class="skill_img_padd">
        <img src="../src/images/html.png" class="skill_img logo_imgs" ref="logo_imgs1">
        <img src="../src/images/css.png" class="skill_img_css logo_imgs" ref="logo_imgs2">
        <img src="../src/images/js.png" class="skill_img logo_imgs" ref="logo_imgs3">
        <img src="../src/images/vue.png" class="skill_img_vue logo_imgs" ref="logo_imgs4">
        <img src="../src/images/firelogo.jpg" class="skill_img_fire logo_imgs" ref="logo_imgs5">
        <img src="../src/images/aws_logo.png" class="skill_img_fire logo_imgs" ref="logo_imgs6">
        <img src="../src/images/github.png" class="skill_img_git logo_imgs" ref="logo_imgs7">
      </div>
      <!-- secondary skills -->
      <div class="Skill_title">
        Secondary Skills
      </div>
      <div class="skill_img_padd">
        <img src="../src/images/python-logo.png" class="skill_img_phy logo_imgs" ref="logo_imgs8">
        <img src="../src/images/jsp.png" class="skill_img_phy logo_imgs" ref="logo_imgs9">
        <img src="../src/images/java_logo.png" class="skill_img_java logo_imgs" ref="logo_imgs10">
      </div>
    </div>
    <!-- Projects -->
    <div>

    </div>
    <!-- Career -->
    <div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      userInfo : {},
      userInfoValue : {},
      scrollTop : 0,
    }
  },
  computed : {
    user() {
      return this.$store.state.user;
    },
    icons() {
      return this.$store.state.icons;
    },
  },
  methods: {
    filter(f,iter){
      var res = [];
      for (const a of iter){
        if(f(a)) res.push(a);
      }
      return res;
    },
    map(f, iter){
      var res =[];
      for (const a of iter){
        res.push(f(a))
      }
      return res;
    },
    scrollEvent : function(){
      this.scrollTop = document.documentElement.scrollTop;
      if(this.scrollTop >=410 ){
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
    
    if(this.scrollTop > 720){
      this.$refs.logo_imgs8.style.visibility = 'visible';
      this.$refs.logo_imgs8.style.animation = 'bottom 1.3s linear';
      this.$refs.logo_imgs9.style.visibility = 'visible';
      this.$refs.logo_imgs9.style.animation = 'top 1.3s linear';
      this.$refs.logo_imgs10.style.visibility = 'visible';
      this.$refs.logo_imgs10.style.animation = 'bottom 1.3s linear';
      }
    }
  },
  created(){
    const user = [{이름:'천승현', 아이콘:true}, 
                  {생년월일 :'98.08.07', 아이콘:true},
                  {이메일: 'csh7215@naver.com',아이콘:true}, 
                  {학력: '삼육대학교(4학년) 컴퓨터공학과', 아이콘: true},
                  {주소지 : '서울시 노원구', 아이콘:true}]
   
   const icons = ['fas fa-user', 'fas fa-calendar-week', 'fas fa-envelope', 'fas fa-pencil-alt',
                  'fas fa-map-marker-alt'];
   this.$store.commit('SET_ICONS', icons);
   this.$store.commit('SET_USER', user);
    
    //js 객체에서 한 요소만 제거하고 싶을때 delete키워드사용.
   },
   mounted() {
     this.userInfo = this.map(u=> u.shift(),this.map(u=>Object.keys(u),this.user));
     console.log(this.user);
     this.userInfoValue = this.map(u=>u.shift(),this.map(u=>Object.values(u),this.user));
     window.scrollTo(0, 0);
     document.addEventListener('scroll', this.scrollEvent)
   }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nanum+Myeongjo:wght@700&display=swap');
body {
  margin:0px;
  height: 10000px;
  overflow-x: hidden;
  font-family: 'Nanum Myeongjo', serif;
  }

.introd_wrap, .About_wrap{
  padding:2rem 2rem;
  margin:0 auto;
}

.introd_wrap {
  background-image: url("./assets/포폴_배경.jpg");
}

.header_content{
  position:fixed;
  top:0px;
  left:0px;
  right:0px;
  margin: 1em 4em;
  display:flex;
  align-items: center;
  justify-content: space-between;
}

.header_title{
  font-size:1.5rem;
}

.header_nav_ele{
  padding : 0 1rem;
  font-size : 1.1em;
  cursor : pointer;
}

.body_title_ani{
  display:flex;
  flex-direction: column;
  padding: 20rem 4rem 8rem;
  font-size:2em;
}

.About_wrap{
  padding: 2em 6em;
}


.About_title, .Skill_title{
  font-size:2em;
  border-bottom: 1px solid black;
  margin-right:50px;
}


.About_text{
  padding: 2em 0;
}

.icons_dummy {
  display:flex;
  flex-wrap: wrap;
}

.icons_flex{
  display:flex;
  width :30%;
  align-items: center;
  margin-bottom:2em;
}

.About_icons {
  font-size: 2em;
}

.icons_flex_col{
  margin-left : 1em;
  display: flex;
  flex-direction: column;
  line-height: 1.5em;
}

.Skills_wrap{
  background-color:whitesmoke;
  padding: 2em 6em 5em;
}

.skill_img{
  margin-top:1em;
  width : 8em;
  /* animation : right 1.3s linear; */
}

@keyframes right {
    from {
      opacity: 0;
      transform: translate(-40px);
    }
    to{
      opacity: 1;
      transform : translate(0px);
    }
}

.skill_img_padd {
  margin:2em 0;
  padding: 2em;
  border-radius: 30px;
  background-color:rgba(255, 255, 255, 0.589);
}

.logo_imgs{
  visibility: hidden;
}

.skill_img_css {
  margin-top:1em;
  width : 5.6em;
  /* animation : top 1.3s linear; */
}

@keyframes top {
  from {
    opacity: 0;
    transform: translate(0, -40px);
  }
  to {
    opacity: 1;
    transfrom : translate(0px);
  }
}

.skill_img_vue {
  width:7.1em;
  height:6.4em;
  /* animation : top 1.5s linear; */
}

.skill_img_fire{
  margin-left:1.2em;
  width:7.1em;
  height:6.4em;
  border-radius: 15px;
  animation : left 1.5s linear;
}

@keyframes left {
  from{
    opacity: 0;
    transform: translate(40px);
  }
  to {
    opacity: 1;
    transform: translate(0px);
  } 
}

@keyframes bottom {
  from{
    opacity: 0;
    transform: translate(0, 40px);
  }
  to {
    opacity: 1;
    transform: translate(0px);
  } 
}


.skill_img_git{
  width : 9.4em;
  height: 6.4em;
  animation : left 1.5s linear;
}

.skill_img_phy{
  width :8.5em;
  height:5em;
  margin-bottom:2em;
}

.skill_img_java{
  margin:1em;
  width : 8em;
}


</style>
