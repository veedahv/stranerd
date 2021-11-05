<template>
  <div class="card">
    <div class="card-body">
      <div class="">
        <p class="w-100 my">{{ card.desc }} <strong>{{ card.em }} </strong></p>
        <div class="card-progress my">
            <div class="w-100 progress-bar"></div>
            <div class="progress" :style="{width: card.progress}"></div>
        </div>
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
