<script>
export default {
  name: 'WhoWeAre'
}
</script>

<template>
  <div class="mx-5 grid grid-cols-1 gap-4 px-4 py-8 sm:grid-cols-2 sm:gap-12 lg:mx-24 lg:my-16">
    <div class="flex flex-col items-start pt-10 lg:gap-5">
      <h3
        class="mb-4 rounded-xl bg-blue-400/40 px-4 text-sm font-semibold text-blue-700 sm:text-base md:text-lg lg:text-xl"
      >
        Who We Are
      </h3>
      <p class="mb-4 text-xl text-gray-700 max-sm:text-3xl xl:text-4xl">
        Providing <span class="text-blue-600">expert eye care</span> with cutting edge technology
        and a curated selection of <span class="text-blue-600">premium eyewear</span> ensuring you
        and your loved ones have access to the best eye care and eyewear options available.
      </p>
    </div>
    <div class="flex items-center justify-center sm:py-0">
      <img src="/src/assets/images/aboutus.png" alt="aboutus" />
    </div>
  </div>
</template>

<style scoped></style>
