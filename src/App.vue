<script setup>
import { ref } from "vue";

import TopMenu from "./components/TopMenu.vue";
import CanvasBlock from "./components/CanvasBlock.vue";
import CodeBox from "./components/CodeBox.vue";
import BottomMenu from "./components/BottomMenu.vue";
import Console from "./components/Console.vue";
</script>

<template>
  <div class="header">
    <TopMenu />
  </div>
  <div>
    <div>
      <CanvasBlock :width="1600" :height="900" />
      <Console />
    </div>
    <CodeBox />
    <BottomMenu />
  </div>
</template>

<style>
.header {
  background-color: #535252;
  height: 50px;
  top: 0px;
  left: 0px;
  right: 0px;
  position: fixed;
}

body {
  background-color: dimgrey;
}
</style>
