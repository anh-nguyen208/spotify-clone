<template>
          <div>
          <img src="./logo.png" alt="Logo" class="object-contain w-full h-16" />
          </div>

          <div class="mx-2 mb-5">
            <button v-for="page in pages" :key="page.id" @click="setID = page.id" :class="`w-full focus:outline-none text-base font-semibold rounded px-3 py-2 flex items-center justify-start text-white ${setID === page.id ? 'bg-light text-white' : 'text-lightest'}`">
              <i class="material-icons mr-3 ">{{page.icon}}</i>
              <p>{{page.name}}</p>
            </button>
          </div>

          <div class="mx-5">
            <h1 class="text-lg font-bold text-lightest tracking-widest uppercase mb-5">Playlists</h1>
            <button class="w-full rounded text-md px-2 py-1 flex items-center justify-start text-lightest opacity-75 hover: opacity-100 focus:outline-none mb-2">
              <i class="material-icons mr-3 ">add_box</i>
              <p class=" font-semibold hover:text-white">Create Playlists</p>
            </button>

            <button class="w-full rounded text-md px-2 py-1 flex items-center justify-start text-lightest opacity-75 hover: opacity-100 focus:outline-none mb-4">
              <i class="material-icons mr-3 text-purple-900">favorite</i>
              <p class=" font-semibold hover:text-white">Liked Songs</p>
            </button>
          </div>

          <div class="h-px w-full bg-light my-3"> </div>

          <div class="mx-5">
            <div class="w-full h-10 overflow-y-auto py-2 mb-5">
              <p v-for="album in albums" :key="album.name"
              class="text-lightest hover:text-white text-base py-1">
                  {{album.name}}
              </p>
            </div>
              <div>
                <img src="./playing.jpg" alt="" class="object-fit w-full h-24">
              </div>
            <button class="w-full p-0.5 focus:outline-none flex items-center justify-start text-lightest opacity-75 hover:opacity-100 text-white">
              <i class="material-icons mr-3 rounded-full border border-lightest">arrow_downward</i>
              <p class="text-white font-semibold">Install App</p>
            </button>
          </div>

         
</template>

<script>
export default {
    name: 'SideNav',
    props:{
        pages: Array,
        albums: Array
    },
    data(){
        return{
            setID: 'home',
        }
    }
}
</script>

<style>

</style>