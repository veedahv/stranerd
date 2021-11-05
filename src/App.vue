<template>
  <div class="app w-100">
    <div class="body w-100 grid">
      <nav class="side-nav">
        <SideNav class="h-100"></SideNav>
      </nav>
      <div class="left-header">
        <LeftHeader></LeftHeader>
      </div>
      <div class="right-header">
        <RightHeader></RightHeader>        
      </div>
      <main class="main">
        <Main></Main>
      </main>
      <aside class="aside">
        <Aside></Aside>
      </aside>
    </div>
  </div>
</template>

<script>
import Aside from './components/layouts/Aside'
import Main from './components/layouts/Main'
import LeftHeader from './components/layouts/LeftHeader'
import RightHeader from './components/layouts/RightHeader'
import SideNav from "./components/layouts/SideNav";

export default {
  name: "App",
  components: {
    Aside,
    Main,
    LeftHeader,
    RightHeader,
    SideNav,
  }
};
</script>

<style>
* {
  font-family: "Raleway", sans-serif;
  color: #4d5c6f;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  max-width: 1700px;
  margin: 0 auto;
}
a {
  text-decoration: none;
  display: inline-block;
}
ul {
  list-style: none;
}
section {
  margin-top: 30px;
  margin-bottom: 30px;
}
.section-title {
  margin-bottom: 15px;
  margin-top: 15px;
  font-size: 16px;
}
.btn {
  background: transparent;
  outline: none;
  border: none;
  border-radius: 7px;
}
.bg-dark-gray {
  color: #fff;
  border: 1px solid #4d5c6f;
  background: #4d5c6f;
}
.header-flex.flex {
  gap: 20px;
}
.input-box,
.header-btn {
  background: #f7f7fc;
  padding: 8px 20px;
}
input {
  font-size: 15px;
}
.header-btn:hover {
  cursor: pointer;
}
.add-btn {
  background: #546dd3;
  cursor: pointer;
}
.header-icon {
  width: 16px;
}
.header-card {
  padding: 8px 25px;
  border-radius: 8px;
}
.header-card .flex {
  gap: 4px;
}
.coin-btn {
  padding: 2px 3px;
}
.h-100 {
  height: 100%;
}
.w-100 {
  width: 100%;
}
.my {
  margin-top: 8px;
  margin-bottom: 8px;
}
.view-all span {
  color: #546dd3;
  font-weight: 500;
  font-size: 14px;
}
.instructor {
  font-size: 14px;
}
.view-all.flex {
  align-items: center;
  gap: 4px;
}
.person-icon,
.card-icon {
  width: 20px;
}
.coin-icon {
  width: 18px;
}
button.btn:hover {
  cursor: pointer;
}
.coin-btn span {
  color: #fff;
}
.star {
  width: 16px;
}
.flex {
  display: flex;
  align-items: center;
}
.grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 3fr 13fr 4fr;
  grid-template-areas:
    "sideNav leftHeader rightHeader"
    "sideNav main aside";
}
.side-nav {
  grid-area: sideNav;
}
.left-header {
  grid-area: leftHeader;
  padding-top: 40px;
}
.right-header {
  padding-right: 20px;
  grid-area: rightHeader;
  padding-top: 40px;
}
.main {
  grid-area: main;
  padding-bottom: 25px;
}
p {
  font-size: 15px;
}
.aside {
  grid-area: aside;
  padding-right: 20px;
}
.space-between {
  justify-content: space-between;
}
.flex-m {
  margin: 0 -10px;
  align-items: stretch;
}
.flex-p {
  padding: 0 10px;
  flex: 1;
}
.card {
  border-radius: 10px;
  background: #f7f7fc;
}
.preview-box {
  background: #c7d6e3;
  border-radius: 10px;
}
.preview-box .btn {
  color: #fff;
  text-transform: uppercase;
  font-weight: 600;
}
</style>
