<script>
import { ArrowUpRight } from 'lucide-vue-next'

export default {
  name: 'OurLenses',
  components: {
    ArrowUpRight
  }
}
</script>

<template>
  <div class="p-4 xl:px-10 xl:py-10 xl:pb-20 2xl:h-screen 2xl:px-40 2xl:py-24">
    <div
      class="bg-ourLenses flex flex-col justify-center bg-cover bg-center xl:h-[640px] xl:rounded-3xl"
    >
      <div class="flex flex-col items-end">
        <div class="md:w-1/2">
          <h2
            class="inline-block rounded-2xl bg-white/20 px-10 py-1 text-sm font-semibold text-white max-sm:text-sm md:text-2xl xl:text-xl"
          >
            Our Lenses
          </h2>

          <p class="font-inter my-5 text-3xl text-white xl:text-5xl">
            Enhance your vision with premium Novar & Tokai lense,crafted for clarity and comfort.
          </p>

          <div class="flex pt-6">
            <p class="inline-block rounded-2xl bg-white/20 px-5 py-1 text-white">
              Verifocal Lenses
            </p>

            <p class="ml-2 inline-block rounded-2xl bg-white/20 px-5 py-1 text-white">
              Bluecut Lenses
            </p>

            <p class="ml-2 inline-block rounded-2xl bg-white/20 px-5 py-1 text-white">
              Photochromic Lenses
            </p>
          </div>

          <div class="mt-6 flex">
            <div>
              <img
                class="max-sm:h-auto max-sm:w-[35vw]"
                src="/src/assets/images/novar.png"
                alt="novar"
              />
              <a class="ju mt-4 flex items-center" href="#">
                <p class="ml-3 text-white md:text-3xl xl:text-xl">Learn More</p>
                <ArrowUpRight :size="28" color="#ffffff" />
              </a>
            </div>
            <div>
              <img
                class="max-sm:h-auto max-sm:w-[35vw]"
                src="/src/assets/images/tokai.png"
                alt="tokai"
              />
              <a class="ju mt-4 flex items-center" href="#">
                <p class="ml-4 text-white md:text-3xl xl:text-xl">Learn More</p>
                <ArrowUpRight :size="28" color="#ffffff" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.bg-ourLenses {
  background-image: url(/src/assets/images/lenses.png);
}

.bg-ourLenses-tab {
  background-image: url(/src/assets/images/lenses-mobile.png);
}

.bg-ourLenses-mobile {
  background-image: url(/src/assets/images/lenses-mobile2.png);
}
</style>
