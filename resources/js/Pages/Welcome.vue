<template>
  <div class="relative bg-gray-50 overflow-hidden">
    <div
      class="hidden sm:block sm:absolute sm:inset-y-0 sm:h-full sm:w-full"
      aria-hidden="true"
    >
      <div class="relative h-full max-w-7xl mx-auto">
        <svg
          class="absolute right-full transform translate-y-1/4 translate-x-1/4 lg:translate-x-1/2"
          width="404"
          height="784"
          fill="none"
          viewBox="0 0 404 784"
        >
          <defs>
            <pattern
              id="f210dbf6-a58d-4871-961e-36d5016a0f49"
              x="0"
              y="0"
              width="20"
              height="20"
              patternUnits="userSpaceOnUse"
            >
              <rect
                x="0"
                y="0"
                width="4"
                height="4"
                class="text-gray-200"
                fill="currentColor"
              />
            </pattern>
          </defs>
          <rect
            width="404"
            height="784"
            fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)"
          />
        </svg>
        <svg
          class="absolute left-full transform -translate-y-3/4 -translate-x-1/4 md:-translate-y-1/2 lg:-translate-x-1/2"
          width="404"
          height="784"
          fill="none"
          viewBox="0 0 404 784"
        >
          <defs>
            <pattern
              id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b"
              x="0"
              y="0"
              width="20"
              height="20"
              patternUnits="userSpaceOnUse"
            >
              <rect
                x="0"
                y="0"
                width="4"
                height="4"
                class="text-gray-200"
                fill="currentColor"
              />
            </pattern>
          </defs>
          <rect
            width="404"
            height="784"
            fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)"
          />
        </svg>
      </div>
    </div>

    <div class="relative pt-6 pb-16 sm:pb-24">
      <div class="max-w-7xl mx-auto px-4 sm:px-6">
        <nav
          class="relative flex items-center justify-between sm:h-10 md:justify-center"
          aria-label="Global"
        >
          <div
            class="flex items-center flex-1 md:absolute md:inset-y-0 md:left-0"
          >
            <div class="flex items-center justify-between w-full md:w-auto">
              <a href="#">
                <span class="sr-only">Workflow</span>
                <img
                  class="h-8 w-auto sm:h-10"
                  src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
                  alt=""
                />
              </a>
            </div>
          </div>
          <div
            class="md:absolute md:flex md:items-center md:justify-end md:inset-y-0 md:right-0"
          >
            <span class="inline-flex rounded-md shadow">
              <a
                v-if="canLogin"
                :href="route('login')"
                class="inline-flex items-center px-4 py-2 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50"
              >
                Log in
              </a>
            </span>
          </div>
        </nav>
      </div>

      <!--
      Mobile menu, show/hide based on menu open state.

      Entering: "duration-150 ease-out"
        From: "opacity-0 scale-95"
        To: "opacity-100 scale-100"
      Leaving: "duration-100 ease-in"
        From: "opacity-100 scale-100"
        To: "opacity-0 scale-95"
    -->

      <main class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24">
        <div class="text-center">
          <h1
            class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl"
          >
            <span class="block xl:inline">Having a hard time finding a </span>
            <span class="block text-indigo-600 xl:inline"
              >vaccine appointment?</span
            >
          </h1>
          <p
            class="mt-3 max-w-md mx-auto text-base text-gray-500 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl"
          >
            Create an account to be notified when vaccine appointments become
            available near you. This service is and always will be free.
          </p>
          <div class="mt-5 max-w-md mx-auto sm:flex sm:justify-center md:mt-8">
            <div class="rounded-md shadow">
              <inertia-link
                :href="route('register')"
                class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10"
              >
                Get started
              </inertia-link>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
  <footer class="bg-white">
    <div class="max-w-7xl mx-auto py-12 px-4 overflow-hidden sm:px-6 lg:px-8">
      <nav
        class="-mx-5 -my-2 flex flex-wrap justify-center"
        aria-label="Footer"
      >
        <div class="px-5 py-2">
          <inertia-link
            :href="route('policy.show')"
            class="text-base text-gray-500 hover:text-gray-900"
          >
            Privacy Policy
          </inertia-link>
        </div>

        <div class="px-5 py-2">
          <inertia-link
            :href="route('terms.show')"
            class="text-base text-gray-500 hover:text-gray-900"
          >
            Terms of Use
          </inertia-link>
        </div>
      </nav>
      <p class="mt-8 text-center text-base text-gray-400">&copy; 2021</p>
      <div>
        <p class="mt-8 text-center text-base text-gray-400">
          Thanks to
          <a href="https://www.vaccinespotter.org">vaccinespotter.org</a> for
          providing the data
        </p>
      </div>
    </div>
  </footer>
</template>


<script>
export default {
  props: {
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
  }
}
</script>
