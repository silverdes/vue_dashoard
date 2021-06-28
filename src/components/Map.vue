<template>
<div class="w-1/2 mx-28">
  <div class="flex justify-between space-x-10 items-center">
    <div class="w-1/2">
      <div class="flex items-center relative">
          <svg xmlns="http://www.w3.org/2000/svg" class="text-gray-dark h-5 w-5 absolute left-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
          <input type="text" class="py-2 pl-8 pr-5 border rounded-lg w-full focus:outline-none focus:border-green-300" placeholder=":349 Washignton,DC" />
      </div>
    </div>
    <div class="flex space-x-2 w-1/2">
      <div class="flex justify-between items-center bg-yellow-100 w-24 px-3 py-2 border border-yellow-300 rounded-xl">
        Rent
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
        </svg>
      </div>
      <div class="flex justify-between items-center bg-yellow-100 w-26 px-3 py-2 border border-yellow-300 rounded-xl">
        2 Rooms
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
        </svg>
      </div>
      <div class="flex justify-between items-center bg-green-100 w-26 px-3 py-2 border border-green-300 rounded-xl">
        <button @click="toggle" class="focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4" />
        </svg>
        </button>
      </div>
    </div>
  </div>
  <div class="mt-10 w-full">
    <transition name="slide-fade">
      <div v-if="show" class="flex flex-col space-y-5 border shadow-sm p-5">
        <span>More filters</span>
        <div class="flex justify-between">
          <div class="flex flex-col space-y-5">
          <div class="flex">
            <div class="flex space-x-10 w-full">
              <div class="w-1/2">Floor</div>
              <div class="flex space-x-5 items-center">
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">-</button>
                <span class="font-semibold">3</span>
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">+</button>
              </div>
            </div>
          </div>
          <div class="flex">
            <div class="flex space-x-10 w-full">
              <div class=" w-1/2">bathrooms</div>
              <div class="flex space-x-5 items-center w-1/2">
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">-</button>
                <span class="font-semibold">2</span>
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">+</button>
              </div>
            </div>
          </div>
          <div class="flex">
            <div class="flex space-x-10 w-full">
              <div class=" w-1/2">Bedrooms</div>
              <div class="flex space-x-5 items-center w-1/2">
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">-</button>
                <span class="font-semibold">0</span>
                <button class="flex rounded-md justify-center items-center w-6 h-5 bg-gray-100 focus:outline-none">+</button>
              </div>
            </div>
          </div>
          </div>
          <div>Features</div>
        </div>
      </div>
    </transition>
  </div>
  <div>
    Products
  </div>
</div>
 
</template>

<script>
export default {
  data(){
    return{
      show:false
    }
  },
  methods:{
    toggle(){
      this.show = !this.show
    }
  }
}
</script>

<style scoped>
.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>