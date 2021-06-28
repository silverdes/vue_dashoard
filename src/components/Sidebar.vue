<template>
  <div class="flex flex-row justify-between bg-gray-100 px-20">
    <div class="flex items-center space-x-20 h-16 w-1/2">
      <div class="flex justify-center items-center px-10">Logo</div>
      <div class="flex justify-between items-center">
        <ul class="flex justify-between items-center space-x-6">
          <li class="group">
            <a
              href="#"
              class="
                text-gray-800
                duration-300
                ease-in-out
                transition-all
                font-pro
                hover:text-blue-dark
              "
              >Home</a
            >
            <div
              class="
                h-0.5
                w-11
                opacity-0
                bg-blue-dark
                absolute
                group-hover:opacity-100
                duration-300
                ease-in-out
                transition-all
              "
            ></div>
          </li>
          <li class="group">
            <a
              href="#"
              class="
                text-gray-800
                duration-300
                ease-in-out
                transition-all
                hover:text-blue-dark
                font-pro
              "
              >Buy</a
            >
            <div
              class="
                h-0.5
                w-7
                rounded-lg
                opacity-0
                bg-blue-dark
                absolute
                group-hover:opacity-100
                duration-300
                ease-in-out
                transition-all
              "
            ></div>
          </li>
          <li class="group">
            <a
              href="#"
              class="
                text-gray-800
                duration-300
                ease-in-out
                transition-all
                hover:text-blue-dark
                font-pro
              "
              >Rent</a
            >
            <div
              class="
                h-0.5
                w-9
                opacity-0
                bg-blue-dark
                absolute
                group-hover:opacity-100
                duration-300
                ease-in-out
                transition-all
              "
            ></div>
          </li>
        </ul>
      </div>
    </div>
    <div class="flex items-center justify-end space-x-10 px-10 h-16 w-1/2">
      <dropdown>
        <template v-slot:icon>
          <svg
            class="text-gray-500"
            xmlns="http://www.w3.org/2000/svg"
            height="24px"
            viewBox="0 0 24 24"
            width="24px"
            fill="currentcolor"
          >
            <path d="M0 0h24v24H0V0z" fill="none" />
            <path
              d="M12 22c1.1 0 2-.9 2-2h-4c0 1.1.9 2 2 2zm6-6v-5c0-3.07-1.63-5.64-4.5-6.32V4c0-.83-.67-1.5-1.5-1.5s-1.5.67-1.5 1.5v.68C7.64 5.36 6 7.92 6 11v5l-2 2v1h16v-1l-2-2zm-2 1H8v-6c0-2.48 1.51-4.5 4-4.5s4 2.02 4 4.5v6z"
            />
          </svg>
        </template>
        <template v-slot:info>
          <div
            class="
              w-3
              h-3
              bg-red-500
              rounded-full
              absolute
              top-0
              right-2
              border-2 border-white
              shadow
            "
          ></div>
        </template>
        <template v-slot:dropdown>
          <ul class="flex w-52">
            <li class="flex flex-grow">
              <div class="px-4 py-3">
                <span class="text-sm">
                  <a href="#" class="font-semibold hover:text-green-light"
                    >John Doe</a
                  >
                  liked your post</span
                >
              </div>
            </li>
          </ul>
        </template>
      </dropdown>
      <dropdown>
        <template v-slot:icon>
          <img
            class="w-8 h-8 object-cover rounded-full"
            src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80"
            alt=""
          />
        </template>
        <template v-slot:info>
          <p class="text-sm font-semibold">{{ user.name }}</p>
        </template>
        <template v-slot:rank>
          <span class="text-xs text-gray-600 font-pro">{{ user.rank }}</span>
        </template>
        <template v-slot:dropdown>
          <ul class="flex w-48">
            <li class="flex flex-1 flex-col">
              <div class="flex space-x-2 group hover:bg-gray-50 px-4 py-3">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4 group-hover:text-green-light"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z"
                    clip-rule="evenodd"
                  />
                </svg>
                <a href="#" class="text-sm group-hover:text-green-light"
                  >Dashboard</a
                >
              </div>
              <div class="flex space-x-2 group hover:bg-gray-50 px-4 py-3">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4 group-hover:text-green-light"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
                    clip-rule="evenodd"
                  />
                </svg>
                <a href="#" class="text-sm group-hover:text-green-light"
                  >Favourite</a
                >
              </div>
              <div class="flex space-x-2 group hover:bg-gray-50 px-4 py-3">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4 group-hover:text-green-light"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"
                  />
                </svg>
                <a href="#" class="text-sm group-hover:text-green-light"
                  >Logout</a
                >
              </div>
            </li>
          </ul>
        </template>
      </dropdown>
    </div>
  </div>
</template>

<script>
import Dropdown from "./Dropdown.vue";
import { CheckIcon, SelectorIcon } from "@heroicons/vue/solid";
export default {
  components: {
    dropdown: Dropdown,
    CheckIcon,
    SelectorIcon,
  },
  data() {
    return {
      user: {
        name: "Jullien Babtiste",
        rank: "Administrator",
      },
    };
  },
  methods: {},
};
</script>

<style scoped></style>
