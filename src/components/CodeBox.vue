<script setup lang="ts">
import { Codemirror } from "vue-codemirror";
import { javascript } from "@codemirror/lang-javascript";
import { oneDark } from "@codemirror/theme-one-dark";
import { ref } from "vue";
import { EditorView } from "@codemirror/view"

interface IProps {
  height?: string,
}
const props = withDefaults(defineProps<IProps>(), {
  height: '400px'
})
const code = ref(
`import { Car, object } from "newcar";

const car = new Car(document.querySelector("#animation"), 60);

const text = new object.Text("Hello world!", {
  x: 100,
  y: 100
});

car.addObject("text");

car.play()
`);
const extensions = [javascript(), oneDark];
const Change = () => {

}
</script>

<template>
  <div class="code">
    <codemirror v-model="code" placeholder="Code gose here..." style="height: 100%" :autofocus="true" :tabSize="2"
      :extensions="extensions" />
  </div>
</template>

<style>
.code {
  float: right;
  width: 50%;
  left: 50%;
  top: 50px;
  position: fixed;
  overflow: visible;
  height: 100%;
  /* background-color: white; */
}
</style>