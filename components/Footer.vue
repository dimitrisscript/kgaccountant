<template>
  <footer class="text-gray-600 body-font">
    <div class="bg-gray-100">
      <div
        class="container px-5 py-6 mx-auto flex items-center sm:flex-row flex-col"
      >
        <NuxtLink
          to="/"
          aria-label="home"
          class="flex title-font font-medium items-center md:justify-start justify-center text-gray-900"
        >
          <img
            src="/logo.svg"
            class="h-8"
            alt="kgaccountant logo"
            width="48"
            height="48"
          />
        </NuxtLink>
        <p class="text-sm text-gray-800 sm:ml-6 sm:mt-0 mt-4">
          © 2020 {{ $attrs.data.title }} —
          <span class="text-gray-700 text-xs ml-1">Powered by</span>
          <a
            href="https://dimitris.siakavelis.gr"
            rel="noreferrer"
            class="text-gray-700 text-xs"
            target="_blank"
            >Dimitris Siakavelis</a
          >
        </p>
        <span
          class="inline-flex sm:ml-auto sm:mt-0 mt-4 justify-center sm:justify-start"
        >
          <a
            href="https://www.facebook.com/kgaccountant.tk"
            target="_blank"
            rel="noreferrer"
            aria-label="facebook"
            class="text-gray-500 hover:text-blue-500"
          >
            <svg
              fill="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              class="w-5 h-5"
              viewBox="0 0 24 24"
            >
              <path
                d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"
              ></path>
            </svg>
          </a>
        </span>
      </div>
    </div>
  </footer>
</template>
