<script setup>
import {ref,reactive} from 'vue'

const location=reactive({
  name:'Dhaka',
  weather:'Sunny'
})

function ChangeLocation(newlocation,newweather){
  location.name=newlocation
  location.weather=newweather

}
</script>

<template>
 <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events & Reactivity in Vue.js</h1>
        <div class="container mx-auto flex space-x-5 justify-center m-5">
            <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="ChangeLocation('Dhaka','Sunny')">
                Dhaka
            </button>
            <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="ChangeLocation('Rajshahi','Rainy')">
                Rajshahi
            </button>
            <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="ChangeLocation('Coxs Bazar','cloudy')">
                Cox's Bazar
            </button>
        </div>
        <h1 class="text-2xl m-10">Current Location is {{ location.name }}</h1>
        <h5 class="text-2xl m-10">Current Location Weather is {{ location.weather }}</h5>
    </section>
</template>

<style scoped>

</style>
