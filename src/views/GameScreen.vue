<template>
  <div class="game-screen">
    <div class="game-row">
      <button class="game-btn light-blur">
        <img src="../assets/direction(4).svg" alt="">
      </button>
    </div>
    <div class="game-row">
      <button class="game-btn light-blur">
        <img src="../assets/direction(1).svg" alt="">

      </button>
      <div class="grid-container light-blur">
        <div class="grid-row" v-for="(row,rowIndex) in gameField" :key="rowIndex">
          <div class="grid-cell light-blur" v-for="(cell,cellIndex) in row" :key="cellIndex"
               :class="`grid-cell-${cell > 1024 ? 'more' : cell}`">{{ cell || '' }}
          </div>
        </div>
      </div>
      <button class="game-btn light-blur">
        <img src="../assets/direction(3).svg" alt="">

      </button>
    </div>
    <div class="game-row">
      <button class="game-btn light-blur">
        <img src="../assets/direction(2).svg" alt="">

      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GameScreen',
  data: () => ({
    gameField: [[0, 2, 4, 8], [16, 32, 64, 128], [256, 512, 1024, 2048], [0, 0, 0, 0]]
  })
}
</script>

<style scoped>

</style>
