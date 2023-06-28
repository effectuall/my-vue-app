<template>
    <div class="scene"> 
    <div id="info">
                <a>elements for interactions </a>  
            </div>
       
        <div class="webgl" ref="webgl">
         
        </div>
    </div>
</template>

<script setup>

import { onMounted, ref } from 'vue';
import Experience from '../classes/Experience.js';

const webgl = ref(null)

onMounted(() => {
    initThree()
})

const initThree = () => {
    const webglCanvas = webgl.value
    const experience = new Experience({
        targetElement: webglCanvas
    })
}

</script>

<style scoped>

</style>