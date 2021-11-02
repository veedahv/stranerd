<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="side-nav">
      <div class="logo-box">

          <img src="../assets/logoo.png" class="logo w-100" alt="stranerd logo" />
      </div>
          <ul class="links-ul">
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../assets/home.svg" alt="">
                      <span>Home</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../assets/help-circle.png" alt="">
                      <span>Questions</span>
                  </a>
              </li>
              <li class="navli active">
                  <a href="" class="navlinks">
                      <img src="../assets/library.png" alt="">
                      <span>Study</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../assets/people.png" alt="">
                      <span>Tutors</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../assets/date.png" alt="">
                      <span>Schedule</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../assets/wallet.png" alt="">
                      <span>wallet</span>
                  </a>
              </li>
          </ul>
  </div>
</template>

<script>
// import StudyCard from './components/StudyCard'
// import HelloWorld from './components/HelloWorld.vue'

// export default {
//   name: 'App',
//   components: {
//     StudyCard,
//     HelloWorld
//   }
// }
</script>

<style scoped>
.side-nav {
    background: #F7F7FC;
    border-radius: 0 10px 0 10px;
    padding: 30px 0;
    padding-left: 10px;
}
.logo-box {
    padding: 30px;
    padding-top: 0;
}
.logo {
    /* width: 150px; */
}
li {
    padding: 20px;
}
li.active {
    padding-right: 0px;
  position: relative;
  color: #4D5C6F;
  height: 100%;
  /* width: 325px; */
  background-color: #FFF;
  border-radius: 25px 0px 0px 25px;
}
li.active::before {
  content: "";
  position: absolute;
  
  background-color: transparent;
  bottom: -50px;
  height: 50px;
  width: 25px;
  right: 0;
  border-top-right-radius: 25px;
  box-shadow: 0 -25px 0 0 #FFF;
}
li.active::after {
  content: "";
  position: absolute;
  
  background-color: transparent;
  top: -50px;
  height: 50px;
  width: 25px;
  right: 0;
  border-bottom-right-radius: 25px;
  box-shadow: 0 25px 0 0 #FFF;
}
li .navlinks {
    display: flex;
    align-items: center;
    gap: 10px;
}
li img {
    width: 20px;
}
</style>
