<template>
  <!-- header -->
        <div class="full sticky top-0 py-3 px-5 flex items-center justify-between">
            <div class="flex items-center">
              <button class="text-white w-8 h-8 bg-black rounded-full mx-2">
                <i class="material-icons">keyboard_arrow_left</i>
              </button>
              <button class="text-white w-8 h-8 bg-black rounded-full ">
                <i class="material-icons">keyboard_arrow_right</i>
              </button>
            </div>

            <div class="rounded-full relative">
              <button @click="showDropdown = true" class="bg-light rounded-full px-2 py-1 focus: outline-none flex items-center">
                <i class="material-icons rounded-full w-6 h-6 mx-1">account_circle</i>
                <p class="text-white font-semibold text-xs mx-1">Account</p>
                <i v-if="showDropdown === false" class="material-icons text-white">keyboard_arrow_down</i> 
                <i v-if="showDropdown === true" class="material-icons text-white">keyboard_arrow_up </i> 
              </button>
              <div v-if="showDropdown === true" class="absolute bg-light w-full mt-1">
                <button @click="showDropdown = false" class="w-full focus:outline-none text-sm text-lightest py-2 hover text-white border-b border-lightest opacity-75 hover:opacity-100">Account</button>
                <button @click="showDropdown = false" class="w-full focus:outline-none text-sm text-lightest py-2 hover text-white border-b border-lightest opacity-75 hover:opacity-100">Log out</button>
              </div>
            </div>
          </div>
  <!-- end header -->
</template>

<script>
export default {
    name: 'Header',
    data(){
        return{
            showDropdown: false,
        }
    }
}
</script>

<style>

</style>