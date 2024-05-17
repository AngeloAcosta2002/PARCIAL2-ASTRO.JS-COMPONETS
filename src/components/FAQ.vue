<script setup>
import { ref } from 'vue'

const showTheme1 = ref (false)
const showTheme2 = ref (false)
const showTheme3 = ref (false)
const showTheme4 = ref (false)

function showInfo(index) {
    if(index == 1){
        showTheme1.value = true
        showTheme2.value = false
        showTheme3.value = false
        showTheme4.value = false
    }

    if(index == 2){
        showTheme1.value = false
        showTheme2.value = true
        showTheme3.value = false
        showTheme4.value = false
    }

    if(index == 3){
        showTheme1.value = false
        showTheme2.value = false
        showTheme3.value = true
        showTheme4.value = false
    }

    if(index == 4){
        showTheme1.value = false
        showTheme2.value = false
        showTheme3.value = false
        showTheme4.value = true
    }
}
</script>
<template>
    <div class="bg-blue-500 p-1 max-w-60 mx-auto mt-12">
        <div>
            <h1
                @click="showInfo(1)"
                class="select-none hover:cursor-pointer bg-blue-400 text-white px-1 flex justify-between"
            >
                tema1
                <span class="">{{ showTheme1 ? '-' : '+' }}</span>
            </h1>
            <div 
                v-show="showTheme1"
                class="bg-blue-100/50 p-1 mt-2 "
            >
                texto del tema 1
            </div>

            <div>
            <h1
                @click="showInfo(2)"
                class="select-none hover:cursor-pointer bg-blue-400 text-white px-1 flex justify-between"
            >
                tema2
                <span class="">{{ showTheme2 ? '-' : '+' }}</span>
            </h1>
            <div 
                v-show="showTheme2"
                class="bg-blue-100/50 p-1 mt-2 "
            >
                texto del tema 2
            </div>

            <div>
            <h1
                @click="showInfo(3)"
                class="select-none hover:cursor-pointer bg-blue-400 text-white px-1 flex justify-between"
            >
                tema2
                <span class="">{{ showTheme3 ? '-' : '+' }}</span>
            </h1>
            <div 
                v-show="showTheme3"
                class="bg-blue-100/50 p-1 mt-2 "
            >
                texto del tema 3
            </div>

            <div>
            <h1
                @click="showInfo(4)"
                class="select-none hover:cursor-pointer bg-blue-400 text-white px-1 flex justify-between"
            >
                tema4
                <span class="">{{ showTheme4 ? '-' : '+' }}</span>
            </h1>
            <div 
                v-show="showTheme4"
                class="bg-blue-100/50 p-1 mt-2 "
            >
                texto del tema 4
            </div>
            
            </div>
            </div>
         </div>
        </div>
    </div>
</template>