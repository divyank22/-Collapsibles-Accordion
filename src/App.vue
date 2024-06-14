<script setup>
import { ref } from "vue";
import card from "./components/card.vue";
const accordionData = ref([
  {
    title: "Section 1",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus. Suspendisse lectus tortor, dignissim sit amet, adipiscing nec, ultricies sed, dolor.",
    icon: "fas fa-plus",
    isOpen: true,
  },
  {
    title: "Section 2",
    content:
      "Cras eget nisi dicit amet. Mauris massa enim, condimentum sed, vehicula quis, facilisis a, odio. Proin id orci porta volutpat sollicitudin mauris. Integer in mauris eu nibh euismod gravida. Duis ac tellus et pede iaculis vehicula.",
    icon: "fas fa-minus",
    isOpen: true,
  },
  {
    title: "Section 3",
    content:
      "Phasellus tempor bibendum enim rutrum ut, nunc. Proin pede metus, vulputate nec, fermentum fringilla, vehicula vitae, justo. Integer in sapien.",
    icon: "fas fa-plus",
    isOpen: true,
  },
  {
    title: "Section 4",
    content:
      "Fusce feugiat. Curabitur a sapien ac eros dapibus interdum. Mauris laoreet. Curabitur nec justo. Sed non pede in dui laoreet fermentum.",
    icon: "fas fa-plus",
    isOpen: true,
  },
  {
    title: "Section 5",
    content:
      "Donec nibh enim, tincidunt vel, facilisis a, sollicitudin sed, eros. Duis aliquam est eu arcu. Fusce feugiat vehicula enim. Proin a augue. Aliquam erat volutpat.",
    icon: "fas fa-minus",
    isOpen: true,
  },
  {
    title: "Section 6",
    content:
      "Nullam ut enim. Quisque mauris dolor, nonummy in, facilisis in, sollicitudin vel, mauris. Nulla semper, ante non feugiat blandit, felis enim viverra arcu, non accumsan tortor quam id tellus.",
    icon: "fas fa-plus",
    isOpen: true,
  },
]);
function toggleSection(index) {
  accordionData.value[index].isOpen = !accordionData.value[index].isOpen;
}
</script>
<template>
  <div v-for="(item, index) in accordionData" :key="index">
    <card :title="item.title" />
    <card
      v-show="item.isOpen"
      :content="item.content"
      :icon="item.icon"
    />
    <div class="flex justify-center items-center">
  <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full" @click="toggleSection(index)">
    <span v-if="item.isOpen == true">to be</span>
    <span v-if="item.isOpen == false">not to be</span>
  </button>
</div>

  </div>
</template>
