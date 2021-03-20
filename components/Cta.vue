<template>
  <section
    class="text-gray-600 body-font bg-gradient-to-r from-blue-500 to-indigo-700"
  >
    <div class="container px-5 py-24 mx-auto">
      <div
        class="lg:w-2/3 flex flex-col sm:flex-row sm:items-center items-start mx-auto"
      >
        <h2
          class="flex-grow sm:pr-16 text-2xl font-medium title-font text-white"
        >
          {{ $attrs.data.title }}
        </h2>
        <NuxtLink
          class="flex-shrink-0 text-white bg-white text-indigo-700 border-0 py-2 px-8 focus:outline-none hover:bg-gray-300 rounded text-lg mt-10 sm:mt-0"
          :to="$attrs.data.buttonLink"
        >
          {{ $attrs.data.buttonText }}
        </NuxtLink>
      </div>
    </div>
  </section>
</template>
