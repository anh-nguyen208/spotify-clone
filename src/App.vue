<template>
    <div class="bg-dark h-screen">
      <link href="https://fonts.googleapis.com/css2?family=Material+Icons"
      rel="stylesheet">

      <div class="flex" style="height: 88vh;">
        <div class="w-1/5 xs:w-1/3 bg-black h-full flex-none mb-2">
          <SideNav :pages="pages" :albums="albums"/>
        </div>
        <!-- main content -->
        <div class="w-full h-full relative overflow-y-scroll">
          <Header />
          <Playlist :recents="recents"/>
          <MadeforAccount :customs="customs"/>
        </div>
        <!-- end main content -->
      </div> 

      <Playbar />
    
      

    </div>
</template>

<script>
import SideNav from './components/SideNav.vue'
import MadeforAccount from './components/MadeforAccount.vue'
import Playlist from './components/Playlists.vue'
import Header from './components/Header.vue'
import Playbar from './components/Playbar.vue'
export default {
  name: 'App',
  components: {
    MadeforAccount,
    Playlist,
    SideNav,
    Header,
    Playbar
  },
    data(){
      return{
        pages:[
          {id: 'home', name:'Home', icon: 'home'},
          {id: 'search', name:'Search', icon: 'search'},
          {id: 'library', name:'Library', icon: 'bar_chart'}
        ],
        albums: [
          {name: 'Nature Noise'},
          {name: 'Disney Favorite'},
          {name: 'All new Indie'},
          {name: 'Mellow'},
          {name: 'Classic Road Trip Songs'},
          {name: 'Lana Del Rey'},
        ],
        showDropdown: false,
        recents :[
          {src:'abc', title:'abc1', artist:'abc'},
          {src:'abc', title:'abc2', artist:'abc'},
          {src:'abc', title:'abc3', artist:'abc'},
          {src:'abc', title:'abc4', artist:'abc'},
          {src:'abc', title:'abc5', artist:'abc'},
        ],
        customs:[
          {src:'abc', title:'abc1', artist:'abc'},
          {src:'abc', title:'abc2', artist:'abc'},
          {src:'abc', title:'abc3', artist:'abc'},
          {src:'abc', title:'abc4', artist:'abc'},
          {src:'abc', title:'abc5', artist:'abc'},
          {src:'abc', title:'abc6', artist:'abc'},
        ]
      }
    }
    
}
</script>

<style src="./assets/tailwind.css" />


