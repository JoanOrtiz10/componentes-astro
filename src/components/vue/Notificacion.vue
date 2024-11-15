<script setup>
import {ref} from 'vue'
let qty= ref(0);
function add(){
  qty.value++
  
}
function rest(){
  qty.value--
  
}
</script>

<template>
    <div class="  max-w-80 mx-auto p-6 bg-purple-300 rounded ">
        <div v-if="qty>0"   
            :class="[{'bg-orange-500' : qty>3},{'text-blue-500' : qty>10}]"
            
            
        class=" mx-auto bg-red-500 h-[50px] w-[50px] text-white size-8 rounded-full font-medium flex  justify-center  items-center">
        
            {{ qty }}
        </div>
        <div v-else-if="qty==0" class=" mx-auto bg-red-500 h-[50px] w-[50px] text-white size-8 rounded-full font-medium flex  justify-center  items-center">
            {{qty}}
        </div>
        <div @click="add()"
        class=" bg-blue-300 cursor-pointer select-none text-white rounded size-6 flex mt-[10px] justify-center items-center"
        >
            +
        </div>
        <div v-if="qty>0"
        
        @click="rest()"
        class=" bg-blue-300 cursor-pointer select-none text-white rounded size-6 flex mt-[10px] justify-center items-center"
        >
            -
        </div>
    </div>
</template>