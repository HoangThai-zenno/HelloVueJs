<template>
    <div class="comp-tabs">
        <div class="tab-title">
            <span>{{ title }}</span>
        </div>
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'comp-tabs',
    data() {
        return {

        }
    },
    props: {
        title: String
    }

}
</script>

<style>

.tab-title {
    display: flex;
    justify-content: space-between;
    padding: 15px 30px;
    border: 2px solid #333;
}

.tab-content {
    border: 2px solid blue;
    text-align: left;
    padding: 10px 10px;
}

.tab-header {
    list-style: none;
    margin: 4px 0;
    border: 2px solid #333;
    padding: 0;
    display: flex;

}

.tab-header li {
    padding: 8px 15px;
    background-color: #333;
    color: #fff;
    cursor: pointer;
    transition: all 0.5s ease;
}
.tab-header li.active{
    background-color: green;
}
.tab-header li:hover {
    background-color: #fff;
    color: #333;
}</style>