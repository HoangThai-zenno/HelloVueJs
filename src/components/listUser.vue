<template>
    <div class="list-user">
        
        <user v-for="user in listUser" :key="user.id" v-bind:user = "user" v-on:handleDeleteUser="deleteUser"/>
    </div>
</template>

<script>
import User from './User.vue';
export default {
    name: 'list-user',
    props: {
        listUser: {
            type: Array,
            default: 'Danh sách User'
        }
    },
    data() {
        return {

        }
    },
    components: {
        User
    },
    methods:{
        deleteUser(data) {
            console.log('deleteUser trong list user', data)
            this.$emit('deleteUserEven', data)
        }
    }
}
</script>

<style>
    .list-user{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
</style>