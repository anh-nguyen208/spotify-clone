<template>
  <!-- Made For account -->
          <div class="w-full h-24 bg-dark px-6 py-2">
            <h1 class="pl-2 mb-2 text-2xl font-semibold text-white tracking-wider hover:underline">Made for You</h1>
            <h2 class="pl-2 text-xs text-lightest uppercase tracking-wider mb-3">Get better recommnedations the more you listen</h2>
          </div>

          <div class="w-full flex flex-wrap px-6">
            <div v-for="custom in customs" :key="custom.title" class="p-2 w-44">
              <div class="bg-light w-full h-auto p-5 rounded-lg shadow-md hover:bg-lightest">
                <!-- <img src="`${recent.src}`" class="w-full h-auto shadow mb-2" alt="" /> -->
                <img src="./playing.jpg" class="w-full h-auto shadow mb-2" alt="custom.src" />
                <h1 class="text-xs text-lightest tracking wide">{{custom.title}}</h1>
                <h2 class="text-xs text-lightest tracking wide">{{custom.artist}}</h2>
                <div class="w-full h-full flex items-end justify-end opacity-0 hover:opacity-100">
                  <div class="bg-green rounded-full h-10 w-10 flex items-center justify-center p-1">
                    <i class="material-icons text-white text-2xl">play_arrow</i>
                  </div>
                </div>
              </div>
            </div>
          </div>
    <!-- End Made For account -->
</template>

<script>
export default {
    name: 'MadeforAccount',
    props:{
        customs: Array
    }
}
</script>

<style>

</style>