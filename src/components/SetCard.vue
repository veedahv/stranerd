<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card">
    <div class="card-body">
      <div class="flex card-flex">
        <div class="file-box">
          <div class="preview-flex flex w-100 h-100">
            <!-- <button class="video btn" v-if="courseType=='video'"> -->
            <img src="../assets/file.png" alt="file logo" />
            <!-- </button> -->
            <!-- <button class="note btn" v-else>preview</button> -->
          </div>
        </div>
        <p class="w-100">{{ card.desc }}</p>
      </div>
      <!-- <div class="card-main"> -->
      <div class="flex space-between my">
        <div class="flex">
          <span class="tag" v-for="(tag, index) in card.tags" :key="index">
            <img
              src="../assets/card.png"
              class="card-icon"
              alt=""
              v-if="tag === 'card'"
            />
            <img
              src="../assets/reader.png"
              class="card-icon"
              alt=""
              v-else-if="tag === 'note'"
            />
            <img
              src="../assets/logo-youtube.png"
              class="card-icon"
              alt=""
              v-else
            />
          </span>
        </div>
        <div class="unpaid" v-if="!card.paid">
          <button class="bg-dark-gray coin-btn flex btn w-100">
            <span>50</span>
            <img src="../assets/coin.png" class="coin-icon" alt="coin" />
          </button>
        </div>
      </div>
      <div class="flex space-between w-100 my">
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
      <!-- </div> -->
    </div>
    <!-- <h2 class="section-title">My Study</h2> -->
    <!-- <aside class="aside"></aside> -->
  </div>
</template>

<script>
// import StudyCard from './components/StudyCard'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  props: ["card"],
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
.file-box {
  /* background: #c7d6e3; */
  width: 64px;
  height: 64px;
}
.flex {
  gap: 5px;
}
.preview-flex {
  align-items: center;
  justify-content: center;
}
.card {
  padding: 15px;
}
.card:hover {
  background: #fff7d0;
  cursor: pointer;
}
.card-flex {
  gap: 15px;
  align-items: center;
  flex-wrap: nowrap;
  font-size: 14px;
}
</style>
