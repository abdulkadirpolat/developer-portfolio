<template>
  <div class="header">
    <p
      @click="back"
      class="cursor-pointer md:hidden  w-full  text-2xl hover:text-purple-800 text-center "
    >
      {{ title }}
    </p>

    <div class="headerLeft">
      <a @click="back" class=" links">{{ button[0] }}</a>
      <nuxt-link class=" links" to="/projects">{{ button[1] }}</nuxt-link>
    </div>
    <div v-for="object in objects" class="headerRight" :key="object">
      <a v-for="(key, value) in object" :href="key" :key="key">
        <font-awesome-icon
          :key="icon"
          v-for="icon in icons"
          class="hover:text-purple-800"
          :icon="[icon, value]"
        />
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "HAPPY DEV",
      objects: [
        { github: "https://github.com" },
        {
          linkedin: "https://www.linkedin.com"
        },
        { twitter: "https://twitter.com" },
        { instagram: "https://www.instagram.com" }
      ],
      icons: ["fab"],
      button: ["Home", "Projects"]
    };
  },
  methods: {
    back() {
      this.$router.push("/");
    }
  }
};
</script>

<style lang="postcss" scoped>
.links {
  background: #e1e5f2;
  @apply cursor-pointer 2sm:text-xs md:w-40 sm:w-52 rounded-3xl  py-2 px-5 w-24 mx-2   text-center hover:bg-purple-800 hover:text-white;
}

.header {
  background-color: #f8f9fa;
  color: #2a2b2c;
  @apply select-none  z-10  sticky top-0  rounded-2xl shadow-md h-16 flex-row flex items-center;
}

.headerLeft {
  @apply w-1/2   flex justify-evenly md:w-full sm:w-full;
}
.headerRight {
  @apply w-1/4  flex justify-evenly sm:hidden text-2xl;
}
.headerRight :last-child {
}
</style>
