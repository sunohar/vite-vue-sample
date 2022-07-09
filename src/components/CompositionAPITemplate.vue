<template>
    <div>
        <h1>
            Vue + Vite -- Composition API
        </h1>
        <button @click="count++"> count 1: {{ count }}</button>
        <button @click="incCount2"> count 2: {{ count2 }}</button>
        <div>
            <h3>
                Product of counts: {{ product }}
            </h3>
        </div>
    </div>
</template>
<script setup>
    import { ref, computed } from 'vue'
    import { onMounted, onBeforeMount, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from 'vue'

    const count = ref(1);
    const count2 = ref(1);

    function incCount2() {
        return count2.value++ ;
    }

    const product = computed(() => {
        return count2.value * count2.value;
    })


    // LifeCycle Hooks
    //use setup() for beforeCreate and created lifecycle hooks in composition API
    // https://learnvue.co/tutorials/vue-lifecycle-hooks-guide
    onBeforeMount(() => {
        console.log('onBeforeMount in the composition api!')    
    })
    onMounted(() => {
        console.log('onMounted in the composition api!')    
    })
    onBeforeUpdate(() => {
        console.log('onBeforeUpdate in the composition api!')    
    })
    onUpdated(() => {
        console.log('onUpdated in the composition api!')    
    })
    onBeforeUnmount(() => {
        console.log('onBeforeUnmount in the composition api!')    
    })
    onUnmounted(() => {
        console.log('onUnmounted in the composition api!')    
    })
</script>
<style scoped>
    h1 {
        background-color: chartreuse;
    }
</style>