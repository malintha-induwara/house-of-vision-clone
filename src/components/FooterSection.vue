<script>
import { Phone } from 'lucide-vue-next'
import { Mail } from 'lucide-vue-next'
import { MapPin } from 'lucide-vue-next'

export default {
  name: 'FooterSection',
  components: {
    Phone,
    Mail,
    MapPin
  },
  data() {
    return {
      contacts: [
        {
          id: 1,
          value: '098 876656',
          icon: Phone
        },
        {
          id: 2,
          value: '098 876656',
          icon: Phone
        },
        {
          id: 3,
          value: '098 876656',
          icon: Phone
        },
        {
          id: 1,
          value: 'info@houseofvision.lk',
          icon: Mail
        }
      ]
    }
  }
}
</script>
<template>
  <div
    class="m-4 flex flex-col items-center justify-between gap-4 rounded-3xl bg-[hsla(228,64%,39%,1)] bg-[radial-gradient(at_93%_14%,rgb(58,170,217)_0px,transparent_50%),radial-gradient(at_6%_95%,rgb(58,170,217)_0px,transparent_50%)] p-2 md:p-6"
  >
    <h1 class="mb-4 mt-5 w-8/12 text-center text-3xl text-white md:mb-8 md:text-5xl lg:text-6xl">
      Have questions about your vision? We're here to help!
    </h1>
    <div
      class="grid max-w-6xl flex-grow grid-cols-1 flex-col-reverse gap-8 text-white md:grid-cols-2 md:gap-8 md:p-8"
    >
      <div class="order-2 flex w-full flex-col items-center md:order-1">
        <div class="flex space-x-5">
          <MapPin />
          <p class="font-inter text-xl font-normal text-white">25/A Bus stand Galle</p>
        </div>
        <div class="flex h-full w-full items-center justify-center p-4">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4201.372829796323!2d80.2154644628159!3d6.031841508407337!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3ae173bcaebbf171%3A0xc64b248b21dda869!2sBus%20Stand%20-%20Galle!5e0!3m2!1sen!2slk!4v1726861556620!5m2!1sen!2slk"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            class="mt-5 h-64 rounded-2xl shadow-md md:h-full md:w-full"
          ></iframe>
        </div>
      </div>
      <div class="space-y-5 px-5 text-center sm:text-left md:order-2">
        <h2
          class="inline-block rounded-2xl bg-white/20 px-10 py-1 text-sm font-semibold text-white md:text-base xl:text-xl"
        >
          Contact Us
        </h2>
        <div class="flex flex-col items-center gap-4 sm:grid sm:grid-cols-2">
          <div
            v-for="contact in contacts"
            :key="contact.id"
            class="flex w-fit items-center rounded-full bg-gray-100 px-4 py-2 text-blue-500 shadow-lg sm:py-1 sm:shadow-sm"
          >
            <component :is="contact.icon" class="mr-2 xl:mr-0" :size="20"></component>
            <p class="font-inter sm:text-xs xl:mx-4 xl:text-lg">{{ contact.value }}</p>
          </div>
        </div>
        <img src="/src/assets/images/footer.png" alt="footer" class="hidden sm:block" />
      </div>
    </div>

    <div
      class="mt-4 flex flex-col items-center justify-center space-y-4 text-white md:flex-row md:gap-40 md:space-y-0"
    >
      <img src="/src/assets/images/logofooter.png" class="w-64" alt="logo" />
      <p class="mt-5 text-sm text-white">"Member of Mount Apollo Hospitals"</p>
    </div>

    <footer class="md:text-xm mb-3 mt-3 text-center text-xs text-white">
      <p>© 2024 House of Vision. All rights Reserved.</p>
    </footer>
  </div>
</template>

<style></style>
