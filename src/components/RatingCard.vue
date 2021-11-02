<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card">
    <div class="card-body">
      <div class="card-flex flex space-between">
        <span class="sn">{{ card.sn }}</span>
        <span class="title">{{ card.title }}</span>
        <span class="rank">{{ card.rank }}</span>
      </div>
    </div>
  </div>
</template>

<script>
// import StudyCard from './components/StudyCard'
// import HelloWorld from './components/HelloWorld.vue'

export default {
    props: ['card'],
//   name: 'App',
//   components: {
//     StudyCard,
//     HelloWorld
//   }
}
</script>

<style scoped>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
.file-box {
  background: #c7d6e3;
  width: 64px;
  height: 64px;
}
.card {
  padding: 15px;
  margin-bottom: 20px;
}
.card:hover {
  background: #8B9EB1;
  cursor: pointer;
  color: #fff;
}
.card-flex {
    /* gap: 15px; */
    align-items: center;
    flex-wrap: nowrap;
    font-size: 14px;
}
.card-progress,
.progress-bar {
    position: relative;
}
.progress,
.progress-bar {
    border-radius: 5px;
}
.progress-bar {
    background: #C7D6E3;
}
.progress {
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    z-index: 5;
    background: #546DD3;
}
.sn {
  font-weight: 600;
  font-size: 14px;
}
.rank {
  color: #546dd3;
  font-weight: 600;
  font-size: 14px;
}
</style>
