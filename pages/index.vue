<script setup lang="ts">
import { useCounterStore } from '~~/store/counter';
const store = useCounterStore()
</script>
<template>
    <div>
        <div class="grid place-items-center mt-10">
            <p class="font-bold text-xl">Counter: {{store.counter}}</p>
           <div>
                <button @click="store.increment" class="mt-2 rounded-md shadow-md font-bold py-2 px-5 bg-white hover:bg-green-400 hover:text-white border border-green-500 hover:border-green-600 m-2">Increment</button>
                <button @click="store.decrement" class="mt-2 rounded-md shadow-md font-bold py-2 px-5 bg-white hover:bg-red-400 hover:text-white border border-red-500 hover:border-red-600 m-2">Decrement</button>
                <button @click="store.reset" class="mt-2 rounded-md shadow-md font-bold py-2 px-5 bg-white hover:bg-orange-400 hover:text-white border border-orange-500 hover:border-orange-600">Reset</button>
           </div>
        </div>
        <div>
             <NuxtWelcome/>
        </div>
    </div>
</template>