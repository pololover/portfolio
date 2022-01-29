<template>
  <div class="Project_wrap" ref="project_wrap">
      <div class="project_title" style="color:white">
        Projects
      </div>
      <div class="fran_whiteBox" ref="whiteBox"> 
      <!-- franchise 프로젝트 -->
      <div class="project_fran_title" style="padding-right:2em;">
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
      <div class="container_wrapper">
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
        <!-- 반응형 -->
        <div class="responsive_youtube"> 
          <iframe border="0" width="250" height="150" src="https://www.youtube.com/embed/F3t98EjBnmo?autoplay=1&mute=1&controls=1&loop=1" title="YouTube video player" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
            <img src="../../src/images/diary.jpg" class="diary_img">
            <div class="text_in_img">Vue 컴포넌트화 및 Swiper에 대한 이해증가</div>
          </div>
        </div>
      </div>
      <div class="Project_padd3 Project_padd3_respon">
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
          <div class="responsive_title">유명 인스타그래머에게 맛집을 추천받을 수 있는 웹사이트입니다.</div>
          <!-- img gsap -->
          <div>
            <!-- img gsap 애니메이션 사진-1 -->
            <div class="health_responsive">
              <div>
                <img src="../../src/images/health-1.jpg" class="gsap_img gsap_imgs" @mouseenter="img_hover" ref="health_ani1">
              </div>
              <div>
                <img src="../../src/images/health-4.jpg" class="gsap_img2 gsap_imgs" ref="health_ani2">
              </div>
              <div>
                <img src="../../src/images/health-3.jpg" class="gsap_img3 gsap_imgs" ref="health_ani3">
              </div>
            </div>
            <!-- img gsap 애니메이션 사진-2 -->
            <div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  props: {
    scrollTop : Number,
  },
  methods: {
    get_scroll_ani : function(){
      const menuHeight = document.querySelector('.header_nav').offsetHeight
      const myworksLocation = document.querySelector('.Project_wrap').offsetTop - 400

      if (this.scrollTop > myworksLocation - menuHeight) {
        this.$refs.project_wrap.style.visibility = 'visible';
        this.$refs.project_wrap.style.animation = 'left 1s linear';
      }
    },
    img_hover : function(){
      console.log('aa');
      // this.$refs.health_ani2.style.transform = 'translate(0)';
      this.$refs.health_ani2.style.opacity = '1';
      this.$refs.health_ani2.style.animation = 'right .5s linear';
      // this.$refs.health_ani3.style.transform = 'translate(0)';
      this.$refs.health_ani3.style.opacity = '1';
      this.$refs.health_ani3.style.animation = 'right .6s linear';
    },
    onFocus : function() {
      if(!this.focusState){
        this.$store.commit('SET_FOCUS', true);
        this.$refs.whiteBox.style.background='rgba(255,255,255,0.3)';
      }else{
        this.$store.commit('SET_FOCUS', false);
        this.$refs.whiteBox.style.background='rgba(255,255,255,0.85)';
      }
      }
  }
  
}
</script>
<style>
  
</style>