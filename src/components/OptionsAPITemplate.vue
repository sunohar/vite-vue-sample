<template>
    <div>
        <h1>
            Vue + Vite -- Options API
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
<script>
export default {
    data() {
        return {
            count: 1,
            count2: 1
        }
    },
    computed: {
        product() {
            return this.count * this.count2
        }
    },
    methods: {
        incCount2() {
            return this.count2++
        }
    },
    // LifeCycle Hooks
    beforeCreate() {
      console.log("BEFORE CREATE!!!!")
    },
    created() {
      console.log("CREATED!!!!")
    },
    beforeMount() {
      console.log("BEFORE MOUNT!!!!")
    },
    mounted() {
      console.log("MOUNTED!!!!") 
      // this.getData()
    },
    beforeUpdate() {
      console.log("BEFORE UPDATE!!!!")
    },
    updated() {
      console.log("UPDATED!!!!")
    },
    beforeUnmount() {
      console.log("BEFORE UNMOUNT!!!!")
    },
    unmounted() {
      console.log("UNMOUNTED!!!!")
    }
}
</script>
<style scoped>
    h1 {
        background-color: aqua;
    }
</style>