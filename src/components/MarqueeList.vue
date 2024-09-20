<template>
    <div class="marquee-container my-8 overflow-hidden">
        <div class="marquee-content flex">
            <div v-for="logo in logos" :key="logo.id" class="flex-shrink-0 w-[150px] h-[150px] mx-6">
                <img :src="logo.image" :alt="logo.alt" class="object-contain h-full">
            </div>
            <div v-for="logo in logos" :key="`duplicate-${logo.id}`" class="flex-shrink-0 w-[150px] h-[150px] mx-6">
                <img :src="logo.image" :alt="logo.alt" class="object-contain h-full">
            </div>
        </div>
    </div>
</template>

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
                { id: 1, alt: "Tafinity", image: Taifnity },
                { id: 2, alt: "Chanel", image: Chanel },
                { id: 3, alt: "Lacoste", image: Lacoste },
                { id: 4, alt: "Boss", image: Boss },
                { id: 5, alt: "Dior", image: Dior },
                { id: 6, alt: "Gucci", image: Gucci }
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