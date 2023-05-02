<template>
    <div class="demo-slot">
        <comp-tab title="Tiêu đề của TAB">
            <ul class="tab-header">
                <li v-for="(item,index) in tabsHeader" :key="index" v-on:click="setActiveTab(index)" v-bind:class="{active: tabActive == index}">{{ item.text }}</li>
            </ul>
            <div class="tab-content tab1 " v-if="tabActive === 0">
                <p>TAB 1 Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos tempora, sunt nemo excepturi autem
                    quis, officiis, odit tempore expedita sed praesentium atque repellendus quisquam totam fuga ipsum
                    debitis. Commodi, aliquam!</p>
            </div>
            <div class="tab-content tab2"  v-else-if="tabActive === 1">
                <p>TAB 2 Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur laudantium temporibus neque
                    quidem dolorum tempora dolorem earum sunt, rerum nemo culpa cumque quae veniam autem ea error voluptatem
                    amet nostrum.</p>
            </div>
            <div class="tab-content tab3"  v-else>
                <p>TAB 3 Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis laborum similique, corrupti
                    quibusdam cum in tempora dignissimos est non, autem impedit sed error libero voluptatum reiciendis
                    reprehenderit sunt illum adipisci.</p>
            </div>
        </comp-tab>
    </div>
</template>

<script>
import CompTab from './CompTab.vue';
export default {
    name: 'demo-slots',
    data() {
        return {
            tabsHeader: [
                {
                    id: 1,
                    text: 'tab 1'
                },
                {
                    id: 2,
                    text: 'tab 2'
                },
                {
                    id: 3,
                    text: 'tab 3'
                }
            ],
            tabActive: 0,
        }
    },
    methods:{
        setActiveTab(index){
            this.tabActive = index;

        }
    },
    components: {
        CompTab
    }
}
</script>

<style>

.demo-slot {
    margin-top: 200px;
    padding: 100px 30px;
    border: 1px solid #333;
}
</style>