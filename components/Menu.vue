<template>
  <header class="text-gray-800 body-font">
    <div
      class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
    >
      <NuxtLink
        to="/"
        class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0"
      >
        <img src="/logo.svg" class="h-12" />
        <span class="ml-3 text-xl">Κώστας Γρηγορίου</span>
      </NuxtLink>
      <nav
        class="md:ml-auto flex flex-wrap items-center text-base justify-center"
      >
        <NuxtLink to="/" class="mr-5 hover:text-blue-500">Αρχική</NuxtLink>
        <NuxtLink to="/contact" class="mr-5 hover:text-blue-500"
          >Επικοινωνία</NuxtLink
        >
      </nav>
    </div>
  </header>
</template>

<style scoped>
.nuxt-link-exact-active {
  font-weight: bold;
}
</style>
