<template>
  <div class="w-100">
    <div class="flex space-between">
      <h2 class="section-title">
          <slot></slot>
      </h2>
      <div class="paginate flex">
        <span class="arrow">
          <img src="../assets/arrow-l.png" class="arrow-img" alt="" />
        </span>
        <span class="circle c-active"></span>
        <span class="circle"></span>
        <span class="circle"></span>
        <span class="arrow">
          <img src="../assets/arrow-r.png" class="arrow-img" alt="" />
        </span>
      </div>
      <a href="" class="view-all flex">
        <span>view all</span>
        <img src="../assets/right.png" class="view-icon" alt="right" />
      </a>
    </div>
  </div>
</template>

<style scoped>
.paginate {
  gap: 4px;
  align-items: center;
}
.circle {
  height: 5px;
  width: 5px;
  border: 1px solid #c7d6e3;
  background: #c7d6e3;
  border-radius: 5px;
}
.c-active {
  border: 1px solid #546dd3;
  background: #546dd3;
}
</style>
