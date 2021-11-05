<template>
      <div class="">
        <div class="flex header-flex">
          <div class="input-box btn w-100 flex">
            <input
              type="text"
              placeholder="Search for anything"
              class="input w-100 btn"
            />
            <button class="search btn">
              <img
                src="../../assets/search.png"
                class="search-icon header-icon"
                alt="coin"
              />
            </button>
          </div>
          <button class="header-btn add-btn btn">
            <img src="../../assets/add.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="../../assets/bell.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="../../assets/grad.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="../../assets/chatbubble.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="../../assets/person.png" class="header-icon" alt="coin" />
          </button>
        </div>
      </div>
</template>

<style scoped>
.header-flex.flex {
  gap: 20px;
}
.input-box,
.header-btn {
  background: #f7f7fc;
  padding: 8px 20px;
}
.header-btn:hover {
  cursor: pointer;
}
.add-btn {
  background: #546dd3;
  cursor: pointer;
}
.header-card {
  padding: 8px 25px;
  border-radius: 8px;
}
.header-card .flex {
  gap: 4px;
}
</style>
