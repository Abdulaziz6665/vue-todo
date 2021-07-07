<template>
    <form @submit.prevent>
        <input 
            v-model="many.title" 
            type="text" 
            placeholder="name"
        >
        <input 
            v-model="many.body" 
            type="text" 
            placeholder="surname"
        >
        <button @click="createPost">add</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            many: {
                title: "",
                body: "",
            }
        }
    },

    methods: {
        createPost() {
            this.many.id = Date.now()
            this.$emit("create", this.many)
            this.many = {
                title: "",
                body: "",
            }
        }
    }
}
</script>

<style>

</style>