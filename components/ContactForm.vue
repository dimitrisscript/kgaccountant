<template>
  <section class="bg-gray-100 pt-10">
    <section
      class="w-full max-w-2xl px-6 mx-auto bg-white rounded-md dark:bg-gray-800 py-24 mb-10"
    >
      <h2
        class="text-3xl font-semibold text-center text-gray-800 dark:text-white"
      >
        {{ $attrs.data.title }}
      </h2>
      <p class="mt-3 text-center text-gray-600 dark:text-gray-400">
        {{ $attrs.data.text }}
      </p>

      <div class="grid grid-cols-1 gap-6 mt-6 sm:grid-cols-2 md:grid-cols-3">
        <a
          href="https://www.google.com/maps?saddr=Current+Location&daddr=Str.+Fragkou+26,+Larisa+412+21,+Greece"
          class="flex flex-col items-center px-4 py-3 text-gray-700 rounded-md dark:text-gray-200 hover:bg-blue-200 dark:hover:bg-indigo-700"
        >
          <svg
            class="w-5 h-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
              clip-rule="evenodd"
            />
          </svg>

          <span class="mt-2">{{ $attrs.data.address }}</span>
        </a>

        <a
          :href="`tel:${$attrs.data.phone}`"
          class="flex flex-col items-center px-4 py-3 text-gray-700 rounded-md dark:text-gray-200 hover:bg-blue-200 dark:hover:bg-indigo-700"
        >
          <svg
            class="w-5 h-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
            />
          </svg>

          <span class="mt-2">{{ $attrs.data.phone }}</span>
        </a>

        <a
          :href="`mailto:${$attrs.data.email}`"
          class="flex flex-col items-center px-4 py-3 text-gray-700 rounded-md dark:text-gray-200 hover:bg-blue-200 dark:hover:bg-indigo-700"
        >
          <svg
            class="w-5 h-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
            />
            <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z" />
          </svg>

          <span class="mt-2">{{ $attrs.data.email }}</span>
        </a>
      </div>
    </section>

    <section class="text-gray-600 body-font relative">
      <div class="absolute inset-0 bg-gray-300">
        <iframe
          width="100%"
          height="100%"
          frameborder="0"
          marginheight="0"
          marginwidth="0"
          title="map"
          scrolling="no"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3072.4317831964545!2d22.422311415710677!3d39.63999611043348!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x135889c37ab4dbef%3A0xcba90a07073ea25a!2zzpPPgc63zrPOv8-Bzq_Ov8-FIM6az47Pg8-EzrHPgiAtIM6bzr_Os865z4PPhM6uz4I!5e0!3m2!1sen!2snl!4v1616004987854!5m2!1sen!2snl&hl=el"
          style="filter: grayscale(0.5) contrast(1.2) opacity(0.8)"
        ></iframe>
      </div>
      <div class="container px-5 py-24 mx-auto flex">
        <div
          class="lg:w-1/3 md:w-1/2 bg-white rounded-lg p-8 flex flex-col md:ml-auto w-full mt-10 md:mt-0 relative z-10 shadow-md"
        >
          <h2 class="text-gray-900 text-lg mb-1 font-medium title-font">
            {{ $attrs.data.contactForm.title }}
          </h2>
          <p class="leading-relaxed mb-5 text-gray-600">
            {{ $attrs.data.contactForm.text }}
          </p>
          <div class="relative mb-4">
            <label for="email" class="leading-7 text-sm text-gray-600"
              >Το Email σας</label
            >
            <input
              id="email"
              v-model="email"
              type="email"
              name="email"
              class="w-full bg-white rounded border border-gray-300 focus:border-indigo-700 focus:ring-2 focus:ring-blue-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
            />
          </div>
          <div class="relative mb-4">
            <label for="message" class="leading-7 text-sm text-gray-600"
              >Το μήνυμά σας</label
            >
            <textarea
              id="message"
              v-model="message"
              name="message"
              class="w-full bg-white rounded border border-gray-300 focus:border-indigo-700 focus:ring-2 focus:ring-blue-200 h-32 text-base outline-none text-gray-700 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"
            ></textarea>
          </div>
          <button
            class="text-white bg-indigo-700 border-0 py-2 px-6 focus:outline-none hover:bg-blue-600 rounded text-lg"
            @click="sendMessage"
          >
            Αποστολή
          </button>
          <p class="text-xs text-gray-500 mt-3">
            {{ $attrs.data.contactForm.footerText }}
          </p>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      message: '',
    }
  },
  methods: {
    async sendMessage() {
      const data = await fetch('https://formcarry.com/s/JjnyzCOOQo', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          Accept: 'application/json',
        },
        body: JSON.stringify({
          email: this.email,
          message: this.message,
        }),
      })
      const response = await data.json()
      if (response.status === 'success') {
        alert('We received your submission, thank you!')
        this.message = ''
        this.email = ''
      } else {
        alert('An error occured: ' + response.message)
      }
    },
  },
}
</script>
