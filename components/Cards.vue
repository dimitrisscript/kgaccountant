<template>
  <section
    class="text-gray-600 body-font bg-gradient-to-r from-indigo-700 to-blue-500"
  >
    <h2 v-if="data.title" class="text-6xl text-center text-white pt-5">
      {{ data.title }}
    </h2>
    <div
      class="container mx-auto"
      :class="[
        data.title === '' ? '' : 'pt-24',
        data.title === '' ? 'pb-24' : '',
      ]"
    >
      <div class="flex flex-wrap -m-4">
        <div class="p-4 lg:w-1/3">
          <div
            class="h-full bg-gray-100 bg-opacity-75 px-8 pt-16 pb-16 rounded-lg overflow-hidden text-center relative"
          >
            <h3
              class="title-font sm:text-2xl text-xl font-medium text-gray-900 mb-3"
            >
              {{ data.card1.title }}
            </h3>
            <p class="leading-relaxed mb-3">
              {{ data.card1.text }}
            </p>
          </div>
        </div>
        <div class="p-4 lg:w-1/3">
          <div
            class="h-full bg-gray-100 bg-opacity-75 px-8 pt-16 pb-16 rounded-lg overflow-hidden text-center relative"
          >
            <h3
              class="title-font sm:text-2xl text-xl font-medium text-gray-900 mb-3"
            >
              {{ data.card2.title }}
            </h3>
            <p class="leading-relaxed mb-3">
              {{ data.card2.text }}
            </p>
          </div>
        </div>
        <div class="p-4 lg:w-1/3">
          <div
            class="h-full bg-gray-100 bg-opacity-75 px-8 pt-16 pb-16 rounded-lg overflow-hidden text-center relative"
          >
            <h3
              class="title-font sm:text-2xl text-xl font-medium text-gray-900 mb-3"
            >
              {{ data.card3.title }}
            </h3>
            <p class="leading-relaxed mb-3">
              {{ data.card3.text }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      required: false,
      default: () => {
        return {
          title: '',
          card1: {
            title: '',
            text: '',
          },
          card2: {
            title: '',
            text: '',
          },
          card3: {
            title: '',
            text: '',
          },
        }
      },
    },
  },
}
</script>
