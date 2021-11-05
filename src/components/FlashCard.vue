<template>
  <div class="card h-100 w-100">
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
          <span class="instructor">Timmy</span>
          <img src="../assets/person.png" class="person-icon" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  background: #f7f7fc;
  padding: 15px;
}
.card:hover {
  background: #EDF6FF;
  cursor: pointer;
}
.flex {
    gap: 5px;
}
.rating {
  align-items: center;
  justify-content: center;
}
.my {
  margin-top: 17px;
  margin-bottom: 17px;
}
h3 {
  font-size: 15px;
}
</style>
