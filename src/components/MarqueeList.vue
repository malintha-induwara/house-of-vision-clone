<script>
import Taifnity from '@/assets/images/logo1.png'
import Chanel from '@/assets/images/logo2.png'
import Lacoste from '@/assets/images/logo3.png'
import Boss from '@/assets/images/logo4.png'
import Dior from '@/assets/images/logo5.png'
import Gucci from '@/assets/images/logo6.png'

export default {
  name: 'MarqueeList',
  data() {
    return {
      logos: [
        { id: 1, alt: 'Tafinity', image: Taifnity },
        { id: 2, alt: 'Chanel', image: Chanel },
        { id: 3, alt: 'Lacoste', image: Lacoste },
        { id: 4, alt: 'Boss', image: Boss },
        { id: 5, alt: 'Dior', image: Dior },
        { id: 6, alt: 'Gucci', image: Gucci }
      ]
    }
  }
}
</script>

<style scoped>
.marquee-container {
  width: 100%;
}

.marquee-content {
  display: flex;
  animation: marquee 15s linear infinite;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(-50%);
  }
}
</style>

<template>
  <div class="marquee-container overflow-hidden">
    <div class="marquee-content flex">
      <div v-for="logo in logos" :key="logo.id" class="mx-6 h-[150px] w-[150px] flex-shrink-0">
        <img :src="logo.image" :alt="logo.alt" class="h-full object-contain" />
      </div>
      <div
        v-for="logo in logos"
        :key="`duplicate-${logo.id}`"
        class="mx-6 h-[150px] w-[150px] flex-shrink-0"
      >
        <img :src="logo.image" :alt="logo.alt" class="h-full object-contain" />
      </div>
    </div>
  </div>
</template>
