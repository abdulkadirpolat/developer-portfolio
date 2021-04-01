<template>
  <figure>
    <img
      class=" transition-transform  duration-300 transform hover:scale-105 shadow-md w-52 h-52 md:w-48 md:h-auto md:rounded-none rounded-full md:mx-auto  mr-8"
      src="/portfolio.png"
      alt=""
      width="384"
      height="512"
    />
    <div class=" md:text-center  md:pt-0 font-light ">
      <p class="text-lg   ">Hi, my name is</p>
      <p class="text-4xl font-semibold ">Happy Dev</p>
      <p class="text-lg  my-7  md:m-3  md:mx-0 md:mb-8 ">
        “I am a Sofware Developer Lorem ipsum dolor sit amet consectetur
        adipisicing elit. Quibusdam, dolores assumenda. Sit, cum dignissimos
        dolorum neque unde natus minus.”
      </p>

      <nuxt-link class="links" to="/resume" target="_blank"
        >RESUME</nuxt-link
      >
      <a
        class="links"
        href="#"
        >CONTACT</a
      >
    </div>
  </figure>
</template>
<script>
export default {};
</script>
<style lang="postcss" scoped>
figure {
  background-color: #f8f9fa;
  @apply md:block p-8   rounded-2xl  shadow-md   flex-row flex items-center mt-7;
}
.links {
  background-color: #e1e5f2;
  @apply 2sm:text-xs rounded-3xl font-light  py-2 px-5 text-center hover:bg-purple-800 hover:text-white;
}
</style>
