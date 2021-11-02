<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card h-100">
    <div class="card-body">
      <div class="flex card-flex">
        <div class="preview-box w-100">
          <div class="preview-flex flex w-100 h-100">
            <button class="video btn">
            <img src="../assets/Vector.png" alt="play logo" />
          </button>
            <!-- <button class="note btn">preview</button> -->
          </div>
        </div>
        <div class="card-main">
          <div class="flex space-between items-start my">
            <p class="w-100">{{ card.desc }}</p>
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
              <span class="instructor">Timmy</span>
              <img src="../assets/person.png" class="person-icon" alt="" />
            </div>
          </div>
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
.preview-box {
  background: #c7d6e3;
  /* width: 96px; */
  height: 210px;
}
.card:hover {
  background: #EDF6FF;
  cursor: pointer;
}
.flex {
    gap: 5px;
}
.preview-flex {
  align-items: center;
  justify-content: center;
}
.card-flex {
  align-items: center;
  flex-wrap: nowrap;
  flex-direction: column;
}
.card-main {
  padding: 15px;
  font-size: 15px;
}
/* .btn {
    padding: 10px 25px;
} */
</style>
