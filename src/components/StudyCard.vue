<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card h-100">
    <div class="card-body">
      <div class="flex card-flex">
        <div class="preview-box">
          <div class="preview-flex flex w-100 h-100">
            <button class="video btn" v-if="courseType == 'video'">
              <img src="../assets/play.png" alt="play logo" />
            </button>
            <button class="note btn" v-else>preview</button>
          </div>
        </div>
        <div class="w-100 p-tag">
          <p class="w-100">
            Work and Energy Introduction to University Physics
          </p>
        </div>
      </div>
      <div class="flex space-between my">
        <div class="flex rating">
          <img
            src="../assets/star-fill.png"
            class="star"
            alt="star filled logo"
          />
          <img
            src="../assets/star-fill.png"
            class="star"
            alt="star filled logo"
          />
          <img
            src="../assets/star-fill.png"
            class="star"
            alt="star filled logo"
          />
          <img
            src="../assets/star-fill.png"
            class="star"
            alt="star filled logo"
          />
          <img src="../assets/star.png" class="star" alt="star logo" />
        </div>
        <div class="flex">
          <span>Timmy</span>
          <img src="../assets/person.png" class="person-icon" alt="" />
        </div>
      </div>
    </div>
    <!-- <h2 class="section-title">My Study</h2> -->
    <!-- <aside class="aside"></aside> -->
  </div>
</template>

<script>
// import StudyCard from './components/StudyCard'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  props: ["courseType"],
  //   name: 'App',
  //   components: {
  //     StudyCard,
  //     HelloWorld
  //   }
};
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
.card:hover {
  background: #fff7d0;
  cursor: pointer;
}
.flex {
  gap: 5px;
}
.preview-box {
  background: #c7d6e3;
  width: 84px;
  height: 84px;
}
.preview-flex {
  align-items: center;
  justify-content: center;
}
.card {
  padding: 15px;
}
.card-flex {
  gap: 15px;
  align-items: center;
  flex-wrap: nowrap;
  font-size: 14px;
}
p {
  font-size: 14px;
}
.p-tag {
  max-width: 125px;
}
</style>
