<template>
  <div class="w-full">
    <div class="w-full sticky flex items-center h-24 gap-5 text-[aliceblue]">
      <div class="text-4xl font-fester font-bold">Giriş</div>
    </div>
    <div class="w-full text-white">
      <div style="font-family: Verdana, Geneva, Tahoma, sans-serif">Son Medya</div>
      <div class="w-full h-auto flex flex-wrap gap-3 p-5">
        <div
          v-for="item in items"
          class="h-72 w-48 flex flex-col gap-1 transition duration-200 hover:bg-slate-700 rounded-lg p-1 hover-icons">
          <div class="relative h-4/6 w-full">
            <!-- Image -->
            <div class="h-full w-full bg-slate-500 rounded-lg object-contain">
              <img
                class="object-cover w-full h-full object-center rounded-lg image"
                src="../assets/photos/mctonight.png" />
            </div>
            <!-- Checkbox -->
            <div class="absolute top-1 left-1 icons cursor-pointer">
              <font-awesome :icon="['fas', 'square-check']" />
            </div>
            <!-- Play Button -->
            <div class="absolute bottom-1 left-2 icons cursor-pointer">
              <font-awesome :icon="['fas', 'play']"></font-awesome>
            </div>

            <!-- More Options Button -->
            <div class="absolute bottom-1 right-2 icons cursor-pointer">
              <font-awesome :icon="['fas', 'ellipsis']" />
            </div>
          </div>

          <!-- Remaining content -->
          <div class="flex-grow w-full rounded-lg p-2 overflow-hidden">
            Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';
const items = [
  '1',
  '2',
  '3',
  '4',
  '5',
  '6',
  '7',
  '8',
  '9',
  '10',
  '1',
  '2',
  '3',
  '4',
  '5',
  '6',
  '7',
  '8',
  '9',
  '10'
];
</script>

<style scoped>
.icons {
  opacity: 0;
  transition: opacity 0.2s ease-in-out;
}
.image {
  opacity: 1;
  transition: opacity 0.2s ease-in-out;
}
.hover-icons:hover .image {
  opacity: 0.7;
}
.hover-icons:hover .icons {
  opacity: 1;
}
</style>
<style>
.font_1 {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.font-fester {
  font-family: 'Fester Bold', sans-serif;
}
.font-yolk {
  font-family: 'TPF Yolk Bold', sans-serif;
}
.font-code-next {
  font-family: 'Code Next Book', sans-serif;
}
</style>
<style src="@/assets/css/fonts.css"></style>
