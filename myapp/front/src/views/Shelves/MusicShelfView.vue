<template>
	<div class="container">
		<!-- Nav -->
		<shelves-nav></shelves-nav>
		<!-- Shelf heading -->
    <ShelfHeading>
      <template v-slot:title>Music Shelf</template>
      <template v-slot:subtitle>Check out my SoundCloud to see what I've been working on!</template>
    </ShelfHeading>

    <a target="_blank" href="https://soundcloud.com/apparitionxxyyzz"><img class="img-fluid w-25 mt-5" src="https://cdn.worldvectorlogo.com/logos/soundcloud-icon-1.svg"/></a>
    <h6 class="mt-4 text-secondary">(Click me!)</h6>
	</div>
</template>

<script>
import ShelvesNav from '../../views/Shelves/ShelvesNavView.vue';
import ShelfHeading from '@/components/ShelfHeading';


export default {
	name: 'Music Shelf',
	data: () => {
		return{
		}
  },
	components: {
		ShelvesNav,
    ShelfHeading
	}
}
</script>