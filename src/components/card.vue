<script setup>
defineProps({
  title: String,
  content:String,
  icon:String,
})

</script>

<template>
    <div class="max-w-lg mx-auto border px-6 py-4 rounded-lg">
            <div class="text-lg font-medium text-gray-800" >{{ title }}</div>
    <p class="text-lg leading-relaxed mb-6">{{ content }}</p>
    <div class="flex justify-between items-center">
        <div>
            <a class="text-gray-500 hover:text-gray-700 mr-4">{{ icon }} </a>
        </div>
    </div>
</div>
</template>