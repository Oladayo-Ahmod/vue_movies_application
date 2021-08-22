<template>
  <header>
	  <Header v-on:searchMovies="searchMovies()" />
	  <!-- <div class="mr-auto">
			<form @submit.prevent="searchMovies()" class="form-inline mr-auto my-2 d-flex justify-content-center my-lg-0">
				<input
				class="form-control line-height mr-sm-2 mr-md-2"
				type="text"
				placeholder="Search any movie"
				v-model="search"
				/>
				<button  class="btn btn-md line-height btn-outline-success my-2 ml-2 my-sm-0" type="submit">
					Search
				</button>
			</form>
		  </div> -->
  </header>
  <footer>
	  <Footer />
  </footer>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
	Header,
	Footer,
  }
}
</script>
