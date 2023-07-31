<script setup>
import {ref,reactive} from 'vue'
const blueColor="bg-blue-500 hover:bg-blue-700"
const greyColor="bg-gray-500 hover:bg-gray-700"

const lights=reactive(
  [
    {
      title:'Light 1',
      lightOn:'//img.icons8.com/?size=512&id=12244&format=png',
      lightOff:'//img.icons8.com/?size=512&id=75&format=png',
      isOn:'true'
    },
    {
      title:'Light 2',
      lightOn:'//img.icons8.com/?size=512&id=12244&format=png',
      lightOff:'//img.icons8.com/?size=512&id=75&format=png',
      isOn:'true'
    },
    {
      title:'Light 3',
      lightOn:'//img.icons8.com/?size=512&id=12244&format=png',
      lightOff:'//img.icons8.com/?size=512&id=75&format=png',
      isOn:'true'
    }
  ]
)

</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Assignment</h1>
        <p class="p-5">Make These Buttons Work</p>
        <div class="flex justify-between space-x-6">
            <div class="p-10 border w-96 flex flex-col space-y-5">
                <button @click="light.isOn=!light.isOn" :class="light.isOn? blueColor : greyColor" v-for="light,index in lights" :key="index" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                    {{light.title}} 
                </button>
                
            </div>
            <div class="p-10 border w-96 flex flex-col space-y-5">
                <img class="w-20" :src="light.isOn? light.lightOn :light.lightOff" v-for="light,index in lights" :key="index" alt="">
                
            </div>
        </div>
    </section>
</template>

<style scoped>

</style>


