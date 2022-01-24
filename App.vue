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
      <div>
        <div class="icons_flex" v-for="(item, index) in user" :key="index">
          <i class="fas fa-user About_icons"></i>
          <div class="icons_flex_col">
            <span>{{index}}</span> 
            <span>{{item}}</span>
          </div>
        </div>
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
    }
  },
  computed : {
    user() {
      return this.$store.state.user;
    }
  },
  created(){
    const user = {이름:'천승현', 생년월일 :'98.08.07',
                  이메일: 'csh7215@naver.com', 학력: '삼육대학교(4학년 재학)',
                  학과 : '컴퓨터공학과', 주소지 : '서울시 노원구' }
    this.$store.commit('SET_USER', user)
    this.userInfo = Object.keys(this.user);
    console.log(this.userInfo);
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
  top: 0px;
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
.header_nav{
  float: right;
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


.About_title{
  font-size:2em;
  border-bottom: 1px solid black;
  margin-right:50px;
}


.About_text{
  padding: 2em 0;
}

.icons_flex{
  display:flex;
  align-items: center;
}

.About_icons {
  font-size: 2em;
}

.icons_flex_col{
  margin-left : 1.5em;
  display: flex;
  flex-direction: column;
  line-height: 1.5em;
}

</style>
