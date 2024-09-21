<script setup>
import WelcomeSection from '@/components/WelcomeSection.vue'
import WhoWeAre from '@/components/WhoWeAre.vue'
import OurServices from '@/components/OurServices.vue'
import OurLenses from '@/components/OurLenses.vue'
import MarqueeList from './components/MarqueeList.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <main>
    <WelcomeSection />
    <WhoWeAre />
    <OurServices />
    <OurLenses />
    <MarqueeList />
    <FooterSection/>
  </main>
</template>

<style scoped></style>
