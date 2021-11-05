<template>
  <div class="side-nav">
      <div class="logo-box">
          <img src="../../assets/logoo.png" class="logo w-100" alt="stranerd logo" />
      </div>
          <ul class="links-ul">
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../../assets/home.svg" alt="">
                      <span>Home</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../../assets/help-circle.png" alt="">
                      <span>Questions</span>
                  </a>
              </li>
              <li class="navli active">
                  <a href="" class="navlinks">
                      <img src="../../assets/library.png" alt="">
                      <span>Study</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../../assets/people.png" alt="">
                      <span>Tutors</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../../assets/date.png" alt="">
                      <span>Schedule</span>
                  </a>
              </li>
              <li class="navli">
                  <a href="" class="navlinks">
                      <img src="../../assets/wallet.png" alt="">
                      <span>wallet</span>
                  </a>
              </li>
          </ul>
  </div>
</template>

<style scoped>
.side-nav {
    background: #F7F7FC;
    border-radius: 0 10px 0 10px;
    padding: 40px 0;
    padding-left: 10px;
}
.logo-box {
    padding: 0 30px 30px 20px;
}
li {
    padding: 20px;
}
li.active {
    padding-right: 0px;
  position: relative;
  color: #4D5C6F;
  height: 100%;
  background-color: #FFF;
  border-radius: 25px 0px 0px 25px;
}
li.active::after,
li.active::before {
  content: "";
  position: absolute;
  background-color: transparent;
  height: 50px;
  width: 25px;
  right: 0;
}
li.active::before {
  bottom: -50px;
  border-top-right-radius: 25px;
  box-shadow: 0 -25px 0 0 #FFF;
}
li.active::after {
  top: -50px;
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
