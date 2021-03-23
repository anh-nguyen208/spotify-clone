<template>
        <!-- playbar -->
        <div class="w-full flex items-center justify-between px-3 bg-light" style="height:12vh;">
            <div class="w-1/3 flex items-center justify-start">
              <div class="flex items-center justify-between">
                <img src="./playing.jpg" alt="" class="w-14 h-14 mr-4">
                <div class="flex flex-col">
                  <h2 class="text-white font-semibold text-lg tracking-wide">The lazy song</h2>
                  <h4 class="text-lightest font-bold text-sm ">Bruno Mars</h4>
                </div>
                <div class="mx-4">
                <i class="text-sm material-icons text-lightest hover:text-white">picture_in_picture_alt</i>
                </div>
              </div>
            </div>
            
            <div class="w-1/3 flex flex-col px-auto">
              <div class="px-auto py-2 flex items-center justify-center">
                <button class="text-lg text-lightest hover:text-white focus:outline-none mx-3"><i class="material-icons">shuffle</i></button>
                <button class="text-lg text-lightest hover:text-white focus:outline-none"><i class="material-icons">skip_previous</i></button>
                <button class="text-xl text-lightest hover:text-white focus:outline-none mx-3"><i class="material-icons">play_circle</i></button>
                <button class="text-lg text-lightest hover:text-white focus:outline-none"><i class="material-icons">skip_next</i></button>
                <button class="text-lg text-lightest hover:text-white focus:outline-none mx-3"><i class="material-icons">repeat</i></button>
              </div>

              <div class="w-full h-1 bg-lightest rounded-full mt-4">
                <div class="w-1/3 h-1 bg-green rounded-full">
                </div>
              </div>
              

            </div>

            <div class="w-1/3 px-auto py-2 flex items-center justify-end">
              <button class="text-xs text-lightest hover:text-white focus:outline-none mx-2"><i class="material-icons">playlist_play</i></button>
              <button class="text-xs text-lightest hover:text-white focus:outline-none"><i class="material-icons">important_devices</i></button>
              <button class="text-xs text-lightest hover:text-white focus:outline-none mx-2"><i class="material-icons">volume_up</i></button>
              <div class="w-20 h-1 bg-lightest rounded-full">
                <div class="w-1/3 h-1 bg-green rounded-full"></div>
              </div>
            </div>
          
        </div>
        <!-- end playbar -->
</template>

<script>
export default {
    name: 'Playbar'
}
</script>

<style>

</style>