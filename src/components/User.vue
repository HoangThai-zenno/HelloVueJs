<template>
    <div class="user">
        <h3> {{ user.name }}</h3>
        <button class="delete" v-on:click="deleteUser">Delete</button>
    </div>
</template>

<script>
export default {
    name: 'user',
    props: {
        user: {
            type: Object,
            default: 'User'
        }
    },
    data() {
        return {

        }
    },
    methods: {
        deleteUser() {
            var data = {
                id: this.user.id
            }
            console.log('deleteUser trong User')
            this.$emit('handleDeleteUser',data);
        }
    }
}
</script>

<style>
.user {
    position: relative;
    padding: 30px;
    margin-bottom: 30px;
    border: 1px solid #333;
    width: calc(33.333% - 20px);
}

.user .delete {
    position: absolute;
    top: 0;
    right: 0;
}
</style>