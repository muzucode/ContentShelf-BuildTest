<template>
	<div class="container">
		<!-- Nav -->
		<shelves-nav></shelves-nav>
		<!-- Shelf heading -->
    <ShelfHeading>
      <template v-slot:title>Book Shelf</template>
      <template v-slot:subtitle>My favorite books that I have read or am currently reading</template>
    </ShelfHeading>

		<!-- Books -->
		<div class="row p-4 d-flex justify-content-between" id="itemTable"  v-if="books">
			<div v-for="book in books" :key="book" class="col-2 pl-3 pr-3 text-wrap mb-4" id="itemHolder">
				<router-link :to="'/book/'+ book._id">
					<img class="img-fluid rounded shadow" style="height: 200px" :src="book.imglink"/>
				</router-link>
				<h6 class="mt-2 pt-0 mb-0 pb-0" id="item-title">{{book.title}}</h6>
				<h6 class="mt-1 pt-0 text-muted" id="item-subtitle" >{{book.author}}</h6>
			</div>
		</div>
	</div>
</template>

<script>
import BookDataService from '../../services/BookDataService';
import ShelvesNav from '../../views/Shelves/ShelvesNavView.vue';
import ShelfHeading from '@/components/ShelfHeading';


export default {
	name: 'Book Shelf',
	data: () => {
		return{
			books : [] // Books gotten from database
		}
  },
	components: {
		ShelvesNav,
    ShelfHeading
	},
	methods: {
		getBooksFromDb: function(){
			// Get books from book db
			BookDataService.getAll()
			.then((res) => {
			console.log('(Frontend getBooksFromDb) Fetched items: ');
			console.log(res);
			this.books = res;
			console.log('(Frontend getBooksFromDb) The current items in the instance are: ');
			console.log(this.books);
			});
		}
	},
	created: function(){
		this.getBooksFromDb();
	}
}
</script>

<style>
#item-title{
	font-weight: bold;
}
#item-subtitle{
	font-size:13px;
	font-style: italic;
}
</style>