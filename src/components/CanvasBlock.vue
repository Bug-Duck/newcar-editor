<script setup>
import { Car } from "newcar";

const props = defineProps({
  width: Number,
  height: Number,
  code: String,
});

window.onload = () => {
  const car = new Car(document.querySelector("#animation"), 60)
}
</script>

<template>
  <div class="canvas">
    <canvas style="width: 100%; height: 100%;" id="animation"></canvas>
  </div>
</template>

<style>
.canvas {
  float: left;
  width: 50%;
  background-color: rgb(169, 169, 169);
  height: 50%;
  position: fixed;
  top: 50px;
}
</style>
