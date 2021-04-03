<template>
  <div class="frontent">
    <span
      class=" absolute -top-4 left-14 bg-gray-100 p-1 px-2 rounded-xl shadow-lg "
      >{{ title }}</span
    >
    <div v-for="front in objects" class="tools" :key="front">
      <i
        :key="value"
        class="flex flex-col justify-center items-center h-full"
        v-for="(value, key) in front"
      >
        <font-awesome-icon
          :class="(color = value)"
          class="text-6xl   "
          :icon="['fab', key]"
        />
        <span>{{ key }} </span>
      </i>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Front-end Tools",
      frontents: [
        "js",
        "vue",
        "html5",
        "css3",
        "sass",
        "bootstrap"
        // "tailwind"
      ],

      objects: [
        { js: "text-yellow-300" },
        { vuejs: "text-green-500" },
        { html5: "text-red-500" },
        { css3: "text-blue-500" },
        { sass: "text-pink-500" },
        { bootstrap: "text-purple-800" }
      ]
    };
  }
};
</script>
<style lang="postcss" scoped>
.frontent {
  background-color: #f8f9fa;
  @apply select-none font-light relative  rounded-2xl shadow-md mt-7 p-10   grid grid-rows-2 grid-cols-4 gap-4   md:grid-cols-3  sm:grid-cols-2 2sm:grid-cols-1;
}
.tools {
  background-color: #e1e5f2;
  @apply transform   hover:scale-105 transition-all duration-300 rounded-2xl h-28;
}
</style>
