<template>
    <header>
        <h1>{{ title }}</h1>
        <button v-on:click="changeTitle">Click to Change Title</button>
        <h3 v-for="user in listUser" :key="user.id">{{ user.email }}</h3>
    </header>
</template>

<script>
export default {
    name: 'comp-header',
    props: {
        title: String,
        listUser: {
            type: Array,
            default: 'Danh sách User'
        }
    },
    data() {
        return {
        }
    },
    methods: {
        changeTitle() {
            this.$emit('changeTitle')
        }
    }
}
</script>

<style></style>
