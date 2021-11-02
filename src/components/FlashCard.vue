<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card w-100">
    <div class="card-body">
      <h3>Physics - Waves and Sounds (100l 1st semester exams)</h3>
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
        <button class="flex btn bg-dark-gray coin-btn">
          <span>50</span>
          <img src="../assets/coin.png" class="coin-icon" alt="coin logo" />
        </button>
      </div>
      <div class="flex space-between">
        <div class="flex">
          <img src="../assets/card.png" class="card-icon" alt="" />
          <span>50 cards</span>
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

// export default {
//   name: 'App',
//   components: {
//     StudyCard,
//     HelloWorld
//   }
// }
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
.card {
  background: #f7f7fc;
  padding: 15px;
  /* border-radius: 10px; */
}
.card:hover {
  background: #EDF6FF;
  cursor: pointer;
}
.flex {
    gap: 5px;
}
.rating {
  /* background: #c7d6e3; */
  align-items: center;
  justify-content: center;
  /* margin: 0 -2px; */
}
.star {
  /* padding-left: 2px; */
  /* padding-right: 2px; */
}
</style>
