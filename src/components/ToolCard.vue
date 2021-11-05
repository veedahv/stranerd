<template>
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
      <h3 class="my">{{ card.title }}</h3>
      <p class="my">{{ card.note }}</p>
          <button class="btn w-100">Study solutions</button>
    </div>
  </div>
</template>

<script>
export default {
    props: ['card']
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
.card {
  border: 1px solid #4D5C6F;
    text-align: center;
    background: transparent;
    padding: 25px 15px;
}
p {
    color: #8B9EB1;
    font-size: 15px;
}
</style>
