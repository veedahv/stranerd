<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card">
    <div class="card-body">
      <div class="">
        <p class="w-100 my">{{ card.desc }}</p>
        <div class="card-progress my">
            <div class="w-100 progress-bar"></div>
            <div class="progress" :style="{width: card.progress}"></div>
        </div>
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
.preview-flex {
  align-items: center;
  justify-content: center;
}
.card:hover {
  background: #EDF6FF;
  cursor: pointer;
}
.flex {
    gap: 5px;
}
.card {
  padding: 10px 15px;
  margin-bottom: 20px;
}
.card-flex {
    gap: 15px;
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
    height: 8px;
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
</style>
