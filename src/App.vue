<template>
	<div id="app">
		<div class="container">
			<Ref/>
		</div>
	</div>
</template>

<script>
import Ref from './components/Ref.vue'
import listUser from './components/listUser.vue';
import CompHeader from './components/CompHeader.vue';
import CompFooter from './components/CompFooter.vue';
export default {
	name: 'app',
	data() {
		return {
			title: 'Hello world - learning Vuejs!',
			user: [
				{
					id: 1,
					name: 'user1',
					email: 'user1@example.com',
				},
				{
					id: 2,
					name: 'user2',
					email: 'user2@example.com',
				},
				{
					id: 3,
					name: 'user3',
					email: 'user3@example.com',
				},
				{
					id: 4,
					name: 'user4',
					email: 'user4@example.com',
				},
				{
					id: 5,
                    name: 'user5',
                    email: 'user5@example.com',
				},
				{
					id: 6,
                    name: 'user6',
                    email: 'user6@example.com',
				}
			]
		}
	},
	methods: {
		handleChangeTitle() {
			this.title = 'Hello Vuejs is CHANGEEEE!';
		},
		handleDeleteUser(data){
			var indexDelete = -1;
			this.user.forEach((u,idx)=>{
				console.log(u.id, idx, data);
				if(u.id === data.id){
					indexDelete = idx;
				}
			});
			if(indexDelete != -1){
				this.user.splice(indexDelete, 1);
			}
			console.log(indexDelete);
			console.log("delete user in APP", data);
		}
	},
	components: {
		CompHeader,
		CompFooter,
		listUser,
		Ref
	}
}
</script>

<style>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
.container{
	max-width: 1170px;
	margin: 0 auto;
	padding: 0 15px;
	min-height: 3000px;

}
</style>
