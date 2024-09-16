<script>

import {ArrowUpRight} from "lucide-vue-next"

export default{
    components:{
        ArrowUpRight
    }
}

</script>

<template>
    <div class="2xl:h-screen p-4 2xl:py-24 xl:pb-20 xl:py-10 2xl:px-40 xl:px-10">
        <div class="bg-ourLenses flex flex-col justify-center xl:h-[640px] rounded-3xl bg-cover bg-center">
            <div class="flex flex-col items-end">
                <div class="md:w-1/2">
                    <h2
                        class="px-10 py-1 inline-block text-sm font-semibold rounded-2xl bg-white/20 text-white  xl:text-xl md:text-2xl max-sm:text-sm">
                        Our Lenses
                    </h2>

                    <p class="text-white my-5 text-3xl xl:text-5xl font-inter ">
                        Enhance your vision with premium Novar & Tokai lense,crafted for clarity and comfort.</p>

                    <div class="flex pt-6">
                        <p class="px-5 py-1 inline-block rounded-2xl bg-white/20 text-white  ">
                            Verifocal Lenses
                        </p>

                        <p class="px-5 ml-2 py-1 inline-block rounded-2xl bg-white/20 text-white">
                            Bluecut Lenses
                        </p>

                        <p class="px-5 ml-2 py-1 inline-block rounded-2xl bg-white/20 text-white" >
                            Photochromic Lenses
                        </p>
                    </div>

                    <div class="flex mt-6">
                        <div >
                            <img  class="max-sm:h-auto max-sm:w-[35vw]" src="/src/assets/images/novar.png" alt="novar">
                            <a class="flex ju items-center mt-4" href="#">
                                <p class="xl:text-xl md:text-3xl  ml-3  text-white ">Learn More</p>
                                <ArrowUpRight :size="28" color="#ffffff" />
                            </a>
                        </div>
                        <div>
                            <img class="max-sm:h-auto max-sm:w-[35vw]" src="/src/assets/images/tokai.png" alt="tokai">
                            <a class="flex ju items-center mt-4" href="#">
                                <p class="xl:text-xl md:text-3xl  ml-4   text-white ">Learn More</p>
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
</style>