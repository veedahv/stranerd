<template>
  <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="card h-100">
    <div class="card-body">
        <div class="">
            <img
              src="../assets/card.png"
              class="icon"
              alt=""
              v-if="card.type === 'card'"
            />
            <img
              src="../assets/file.png"
              class="icon"
              alt=""
              v-else-if="card.type === 'file'"
            />
            <img
              src="../assets/map.png"
              class="icon"
              alt=""
              v-else
            />
        </div>
      <h3>{{ card.title }}</h3>
      <p class="my">{{ card.note }}</p>
          <button class="btn w-100">Study solutions</button>
    </div>
    <!-- <h2 class="section-title">My Study</h2> -->
    <!-- <aside class="aside"></aside> -->
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
.card .btn {
  border: 1px solid #4D5C6F;
}
.btn {
    padding: 10px 25px;
}
.icon {
    width: 48px;
}
/* .coin-btn {
    padding: 2px 4px;
} */
.card {
  border: 1px solid #4D5C6F;
    text-align: center;
    background: transparent;
    padding: 25px 15px;
}
</style>
