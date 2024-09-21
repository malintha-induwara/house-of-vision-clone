<script>
import { MessageCircleMore } from 'lucide-vue-next'
import { AlignJustify } from 'lucide-vue-next'

export default {
  name: 'WelcomeSection',
  components: {
    MessageCircleMore,
    AlignJustify
  }
}
</script>

<template>
  <div class="h-screen p-4 lg:p-6">
    <div class="bg-welcome flow-root h-full rounded-3xl bg-cover bg-center">
      <nav
        class="mx-auto my-10 flex h-16 w-11/12 items-center justify-between rounded-lg bg-white p-5 md:h-20 lg:shadow-xl"
      >
        <div class="w-40 sm:w-52 lg:w-64">
          <img src="/src/assets/images/navlogo.png" alt="Company Logo" />
        </div>

        <button class="lg:hidden" aria-label="Toggle menu">
          <AlignJustify />
        </button>

        <div class="hidden lg:block">
          <ul class="flex items-center space-x-10 text-blue-600">
            <li><a href="#services" class="hover:text-blue-800">Services</a></li>
            <li><a href="#lenses" class="hover:text-blue-800">Lenses</a></li>
            <li><a href="#brands" class="hover:text-blue-800">Brands</a></li>
            <li>
              <a
                href="#contact"
                class="flex items-center justify-center gap-2 rounded-full bg-blue-600 px-8 py-2 text-sm text-white transition-colors hover:bg-blue-700"
              >
                Contact Us
                <MessageCircleMore :size="20" />
              </a>
            </li>
          </ul>
        </div>
      </nav>

      <div
        class="flex h-4/6 flex-col justify-center space-y-5 text-white max-sm:mx-8 sm:mx-10 lg:mx-20"
      >
        <div class="flex">
          <h1 class="w-[800px] text-4xl max-sm:mx-8 max-sm:text-center sm:text-7xl">
            See the world clearly with House of Vision
          </h1>
        </div>
        <div class="text-lg font-light max-sm:text-center sm:max-w-[300px]">
          <p>Expert eye care, premium lenses,and desinger eyewear all in one place.</p>
        </div>
        <div class="flow flex max-sm:justify-center max-sm:pt-20">
          <a
            href="#contact"
            class="flex items-center justify-center gap-2 rounded-full bg-blue-600 px-8 py-2 text-sm text-white transition-colors hover:bg-blue-700"
          >
            Contact Us
            <MessageCircleMore :size="20" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg-welcome {
  background-image: url(/src/assets/images/hero1.png);
}
</style>
