<template>
  <div class="page-container">
    <div class="emptyness">
    </div>
    <chessboard class="chessboard" :iconDir="iconDir" :pgn="pgn" :side="side" v-on:change="boardChange($event)"></chessboard>
    <div class="controls">
      <!-- <a class="button" v-on:click="randomMove()">Random</a> -->
      <a class="button btn btn-default" v-on:click="reset()">Recommencer la partie</a>
      <!-- <a class="button" v-on:click="swapSides()">Swap</a> -->
      <chat></chat>
    </div>
  </div>
</template>

<script src="./chess.js"></script>

<style scoped lang="scss">
@import '../../_variables';

.page-container {
  display: flex;
  flex-direction: row;

  @include media('medium') {
    flex-direction: column;
  }
}

.emptyness {
  flex-basis: 20%;
}

.chessboard {
  flex: 1;
  flex-basis: 60%;
  max-width: 100vh;
}

.controls {
  flex: 0;
  flex-basis: 20%;
}

</style>
