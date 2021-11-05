<template>
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

export default {
    props: ['card']
}
</script>

<style scoped>
.card {
  padding: 15px;
  margin-bottom: 20px;
}
.card:hover {
  background: #8B9EB1;
  cursor: pointer;
  font-weight: 600;
}
.card:hover span {
  color: #fff;
}
.card-flex {
    align-items: center;
    flex-wrap: nowrap;
    font-size: 14px;
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
