<template>
    <div class="posts" :key="post" v-for="post in many">
        <div><b>Ism:</b> {{ post.title }}</div>
        <div><b>Familiya:</b> {{ post.body }}</div>
    </div>
</template>

<script>
export default {
    props: {
        many: {
            type: Array,
            required: true,
        }
    },
}
</script>

<style>

</style>