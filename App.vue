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
    <div class="Project_wrap">
      <div class="project_title">
        Project
      </div>
      <div class="fran_whiteBox"> 
      <!-- franchise 프로젝트 -->
      <div class="project_fran_title">
          신메뉴드루와
      </div>
      <div>
        <!-- 프랜차이즈 설명부분 -->
        <div class="fran_expl"> 
            <!--franchise 정보  -->
          <div class="fran_primary">프랜차이즈 신메뉴에 대해서 정보를 공유하고 토론할 수 있는 웹사이트입니다.<span style="font-size:0.8em;color:gray;"> (1人)</span></div>
            <!-- 기술 스택 -->
          <ul>
            <li>Frontend: 100%</li>
            <li>Backend: 100%</li>
            <li>Tech stack: vue, firebase, aws</li>
            <li>Library: tinymice</li>
          </ul>
          <!--배운 것들-->
          <div class="fran_learn">
            aws, firebase 등을 통하여 데이터 토큰 저장방식에 대하여 고민할 수 있었고, Vue에서 데이터를 CRUD 하는데 있어 배움이 있었던 프로젝트입니다.
          </div>
          <div>
            Vuex를 이용해 상태관리에 대한 이해도를 높였습니다. 
          </div>
          <!-- 깃허브 -->
          <div class="fran_git">
            깃허브: <a href="https://github.com/pololover/FranchiseNew">https://github.com/pololover/FranchiseNew</a>
          </div>
        </div>
        <div class="responsive_title">프랜차이즈 신메뉴에 대해서 정보를 공유하고 토론할 수 있는 웹사이트입니다. </div>
        <div class="container">
         <div class="wrapper">
          <input type="checkbox" @click="onFocus" class="watch">
            <div class="video">
          <iframe border="0" width="660" height="415" src="https://www.youtube.com/embed/F3t98EjBnmo?autoplay=1&mute=1&controls=1&loop=1" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
          <div class="text">
            <span data-text="Watch the video"></span>
          </div>
          </div>
        </div>
       </div>
      </div>
      <div class="Project_padd3">
        <div class="project_fran_title">맛집일기</div>
        <div class="project_health_wrap">
          <div class="health_description">
            <div class="fran_primary">유명 인스타그래머에게 맛집을 추천받을 수 있는 웹사이트입니다.<span style="font-size:0.8em;color:gray;"> (1人)</span></div>
            <ul>
              <li>Frontend: 100%</li>
              <li>Tech stack: vue</li>
              <li>Library: Swiper</li>
            </ul>
          <!-- 맛집일기 learn -->
          <div class="diary_learn">
            VueJs를 이용하여 UI디자인과 애니매이션에 대한 이해도를 높이기 위해 이에 포커스를 두어 프로젝트를 진행했습니다. 
          </div>
          <div>
            사용자가 정보를 가시적으로 볼 수 있도록 Swiper 라이브러리를 사용했고 이를 처음 적용함으로써 Vue의 Composition API에서 어떻게 정의하고 호출하는지 알게 되었습니다.
          </div>
          <!-- git_맛집일기 -->
          <div class="diary_git">
            깃허브:<a href="https://github.com/pololover/Mukhondon">https://github.com/pololover/Mukhondon</a>
          </div>
        </div>
        <div class="responsive_title">유명 인스타그래머에게 맛집을 추천받을 수 있는 웹사이트입니다.</div>
          <div class="text_photo">
            <img src="../src/images/diary.jpg" class="diary_img">
            <div class="text_in_img">Vue 컴포넌트화 및 Swiper에 대한 이해증가</div>
          </div>
        </div>
      </div>
      <div class="Project_padd3">
        <div class="project_fran_title">
          헬맵
        </div>
        <!-- 헬맵 내용 전체 -->
        <div class="project_health_wrap">
          <div class="health_description">
            
            <div class="fran_primary">COVID-19로 인한 실내헬스장에 가기 두려워지는 사람들을 위해 개발한 웹사이트입니다.<span style="font-size:0.8em;color:gray;"> (3人)</span></div>
          <div>
            <ul style="margin-bottom:2em;">
            <li>Frontend: 70%</li>
            <li>Backend: 50%</li>
            <li>Tech stack: Jsp, JDBC, SQL</li>
          </ul>
          <!-- 헬맵 내용 설명 -->
          <div>
            처음 진행한 협업 프로젝트로 jsp와 html, js, css로 전반적인 프론트엔드 부분을 구현하였고, sql과 JDBC를 통해 데이터베이스 부분을 처리했습니다. 
          </div>
          <div class="diary_learn">
            Ajax호출을 통해 비동기 함수 및 데이터에 대해 배울 수 있었고 카카오 Map API를 사용해 마커 및 Map객체 사용방법에 대해 학습했습니다.
          </div>
          <div class="diary_git">
            깃허브:<a href="https://github.com/pololover/healthymap">https://github.com/pololover/healthymap</a>
          </div>
            </div>
          </div>
          <!-- img gsap -->
          <div>
            <!-- img gsap 애니메이션 사진-1 -->
            <div class="health_responsive">
              <div>
                <img src="../src/images/health-1.jpg" class="gsap_img" @mouseenter="img_hover" ref="health_ani1">
              </div>
              <div>
                <img src="../src/images/health-4.jpg" class="gsap_img2" ref="health_ani2">
              </div>
              <div>
                <img src="../src/images/health-3.jpg" class="gsap_img3" ref="health_ani3">
              </div>
            </div>
            <!-- img gsap 애니메이션 사진-2 -->
            <div>

            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Contact -->
    <div class="contact_wrap">
      <div class="flex_contact">
        <a href="https://github.com/pololover">
          <img src="../src/images/github.png" class="contact_imgs">
        </a>
        <a href="https://pololove.tistory.com">
          <img src="../src/images/tistory.png" class="contact_imgs_tistory">
        </a>
      </div>
      <!-- text -->
      <div class="right_text">
        © 2021. Cheon Seung Hyun. All rights reserved.
      </div>
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
    },
    img_hover : function(){
      console.log('aa')
      
      // this.$refs.health_ani2.style.transform = 'translate(0)';
      this.$refs.health_ani2.style.opacity = '1';
      this.$refs.health_ani2.style.animation = 'right .5s linear';
      // this.$refs.health_ani3.style.transform = 'translate(0)';
      this.$refs.health_ani3.style.opacity = '1';
      this.$refs.health_ani3.style.animation = 'right .6s linear';
    },
    onFocus : function() {
      
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
     document.addEventListener('scroll', this.scrollEvent)
   }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700;800&family=Noto+Serif+KR:wght@700;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@700;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;500;700&family=Noto+Serif+KR:wght@700;900&display=swap');
body {
  margin:0px;
  height: 3600px;
  overflow-x: hidden;
  font-weight:400;
  font-family: 'Noto Serif KR', serif;
  }

.introd_wrap, .About_wrap{
  padding:2rem 2rem;
  margin:0 auto;
}

.introd_wrap {
  background-image: url("./assets/포폴_배경.jpg");
}

.header_content{
  z-index: 3;
  position:fixed;
  background-color:rgba(255,255,255,0.8);
  color:black;
  height:40px;
  top:0px;
  left:0px;
  right:0px;
  padding: 1em;
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


.About_title, .Skill_title, .project_title{
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
  padding: 2em 6em 4em;
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

.Project_wrap{
  background-color:rgba(0,0,0,0.9);
  padding: 2em 6em 6em;
  font-family: 'Noto Sans KR', sans-serif;
  font-weight:400;
}

.Project_padd {
  margin-top:1em;
  margin-bottom:1em;
  padding: 3em;
  border-radius: 30px;
  background-color:transparent;
  height:20em;
}

.Project_padd3{
  background-color:rgba(255, 255, 255, 0.589);
  height:auto;
  padding-bottom:7em;
  position:relative;
  padding-left:2em;
}

.project_fran_title {
  display:flex;
  justify-content: center;
  margin-right:1%;
  font-size:1.7em;
  margin-top:1em;
  font-weight:600;
}

.fran_whiteBox{
  background-color:rgba(255, 255, 255, 0.85);
  padding : 0 1em 3em;
  padding-right:1em;
  position:relative;
}

.fran_expl {
  position:absolute;
  margin-top:3em;
  margin-left:1em;
  width :350px;
}
.fran_expl_title{
  display:flex;
  font-size:1.5em;
  justify-content: center;
}
.fran_primary{
  line-height:1.4em;
  margin-bottom:3em;
  font-weight:800;
  font-family: 'Nanum Gothic', sans-serif;
}
.fran_learn {
  margin-top : 2em;
  margin-bottom :1em;
}
.fran_git {
  margin-top: 2em;
  font-size: 0.9em;
  
}

.responsive_title{
  display:none;
  position:absolute;
  left:50%;
  transform: translate(-50%);
  bottom:5%;
  font-size:1.1em;
  font-weight:800;
  font-family: 'Nanum Gothic', sans-serif;
}

.project_health_wrap{
  display:flex;
  flex :1;
  margin-top:3em;
  margin-left:2em;
}
.health_description{
  width: 360px;
  margin-right:1.5em;
}

.health_description_fade{
  width: 360px;
  margin-right:1.5em;
}

.text_in_img{
  position:absolute;
  opacity: 0;
  top:35%;
  left:25%;
  font-size:1.2em;
  font-weight:700;
}

.text_photo{
  position:relative;
  display:flex;
  flex :1;
  margin-right:0.5em;
  padding-left:1.5em;
}

.diary_img{
  width:87%;
  height:auto;
  margin : 0 auto;
}


.text_photo:hover .diary_img{
  opacity: 0.5;
  filter:blur(5px);
}

.text_photo:hover .text_in_img{
  opacity: 1;
}

.project_diary_title{
  margin-left: 1em;
  font-weight:800;
  font-family: 'Nanum Gothic', sans-serif;
}

.diary_learn{
  margin : 2em 0;
}

.diary_git{
  margin-top:1em;
  font-size:0.9em;
}
.health_responsive{
  overflow:hidden;
  position:relative;
  display:flex;
  width:100%;
  margin-left:2em;
  justify-content: space-between;
}
.health_responsive div{
  width:calc(100/3);
  position:relative;
  margin-right: 4em;
}

.gsap_img{
  z-index:1;
  border-radius: 10px;
  width : 120%;
  height:400px;
}

.gsap_img2{
  z-index:1;
  /* transform : translate(-100%); */
  border-radius: 10px;
  width:120%;
  height:400px;
  opacity: 0;
}
.gsap_img3 {
  z-index:1;
  border-radius: 10px;
  /* transform: translate(-220%); */
  width:120%;
  height:400px;
  opacity: 0;
}

.contact_wrap{
  padding: 2em;
}

.flex_contact{
  display:flex;
  justify-content: center;
  align-items: center;
}

.contact_imgs{
  width:50px;
  height:25px;
  cursor: pointer;
}

.contact_imgs:hover{
  opacity: 0.5;
}

.contact_imgs_tistory{
  width:30px;
  height:25px;
  cursor: pointer;
}

.contact_imgs_tistory:hover {
  opacity: 0.5;
}

.right_text{
  margin-top:1em;
  display:flex;
  justify-content: center;
  align-items: center;
  font-size:0.8em;
}

@media (max-height : 700px) {
  .fran_whiteBox{
    padding:0 1em 6em;
  }
}

@media (max-height:600px){
  .fran_whiteBox{
    padding:0 1em 9em;
  }
}

@media (max-height:500px){
  .fran_expl{
    display:none;
  }
  .container{
    padding-right:24%;
  }
}
@media (max-width:1120px){
  .fran_expl{
    display:none;
  }
  .container{
    padding-right:24%;
  }
  .responsive_title{
    display:block;
  }
}

@media (max-width:1120px) {
 .health_description{
   display:none;
 } 
 .Project_padd3{
   padding-left: 0;
   padding-right: 2em;
 }
}


</style>

<style lang="scss">
@import "@/assets/style/sstyle.scss"
</style>