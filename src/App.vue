<template>
  <nav class="flex flex-row max-w-full mx-auto justify-between items-center h-14 bg-black sticky top-0 z-10">
    <div class="w-full flex justify-between">
      <h1 class="text-2xl ml-5">LOGO</h1>
      <button @click="ToggleMenu" class="w-[130px] h-[30px] border rounded-lg mr-5 block md:hidden">
        Menu
      </button>
    </div>
    <ul class="hidden flex-row justify-between font-bold w-[240px] md:flex">
      <li class="w-[80px] h-[25px] text-center">
        <router-link to="/">Home</router-link>
      </li>
      <li class="w-[80px] h-[25px] text-center">
        <router-link to="/about">About</router-link>
      </li>
      <li class="w-[80px] h-[25px] text-center">
        <router-link to="/about">Contact</router-link>
      </li>
    </ul>
  </nav>
  <router-view/>
</template>

<style>
  @import url('./assets/main.css');
  body{
    color: white;
    text-align: center;
  }
</style>

<script>
  export default{
    name:"App",
    data(){
      return{
        menu : false
      }
    },
    methods: {
      ToggleMenu(){
        this.menu = !this.menu
      }
    },
    created(){
      console.log(this.menu)
    }
  }
</script>