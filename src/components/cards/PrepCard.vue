<template>
  <div class="card h-100">
    <div class="card-body">
      <h3>{{ prep.title }}</h3>
      <p class="my">{{ prep.note }}</p>
      <div class="paid" v-if="prep.paid">
          <button class="bg-dark-gray my btn w-100">Test yourself</button>
          <button class="btn w-100">Study solutions</button>
      </div>
      <div class="unpaid" v-else>
          <p class="my">
            <strong class="my">
              Unlock for a month
          <span>50</span>
          <img src="../../assets/coin.png" class="coin-icon" alt="coin" />

            </strong>
        </p>
          <button class="bg-dark-gray btn w-100">Unlock</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: ['prep'],
}
</script>

<style scoped>
.card .btn {
  border: 1px solid #4D5C6F;
}
.btn {
    padding: 10px 25px;
}
.card {
    text-align: center;
    padding: 15px;
}
.card:hover {
  background: #FFECFF;
  cursor: pointer;
}
.flex {
    gap: 5px;
}
</style>
