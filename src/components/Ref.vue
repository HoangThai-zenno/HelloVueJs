<template>
    <div class="demo-ref">
        <h1>DEMO REF</h1>
        <button class="avata" v-on:click="handleChaneAvata">Thay đổi avata</button>
        <input type="file" ref="changeAvata" class="inputDefault">
    </div>
</template>

<script>
export default {
    name: 'ref-demo',
    methods:{
        handleChaneAvata(){
            this.$refs.changeAvata.click()
        }
    }
}
</script>

<style>
    .demo-ref {
        margin-top: 200px;
        padding: 100px 30px;
        border: 1px solid #333;
    }
    .demo-ref .avata {
        margin-top: 10px;
        padding: 10px;
        color: #fff;
        background-color: #333;
        border: 1px solid #333;
        transition: all 0.5s ease;
        cursor: pointer;
        font-size: 32px;
    }
    .demo-ref .avata:hover{
        background-color: #fff;
        color: #333;
        border: 5px dotted red;
    }
    .demo-ref .inputDefault{
        display: none;
    }
</style>