<template>
  <div>
    <div class="container mt-0">
      <nav class="navbar px-2 mt-0  navbar-expand-lg navbar-light bg-light neo-shadow">
        <a class="ml-3 navbar-brand" href="#">Navbar</a>
        <button
          class="navbar-toggler d-lg-none"
          type="button"
          data-toggle="collapse"
          data-target="#collapsibleNavId"
          aria-controls="collapsibleNavId"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse " id="collapsibleNavId">
          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
            <li class="nav-item active">
              <a class="nav-link" href="#"
                >Home <span class="sr-only"></span></a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Link</a>
            </li>

          </ul>
		  <div class="mr-auto">
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
		  </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: "Header",
  setup(){
	  const search = ref("");
	  const movies = ref([]);

	  const searchMovies=()=>{
		  if (search.value !== '') {
			  console.log(search.value);
		  }
	  }

	  return {
		  search,
		  movies,
		  searchMovies
	  }
  }
}
// eslint-disable-next-line
</script>

<style scoped>
.btn{
border-radius: 5px !important;
}
.neo-shadow{
border: 0 !important;
background-color: #e0e5ec !important;
box-shadow: -7px -7px 20px 0px #fff9, -4px -4px 5px 0px #fff9, 7px 7px 20px 0px #0002, 4px 4px 5px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001;
border-radius: 15px;
/* padding: 20px 0px!important; */
}
.mr-auto{
	float:right;
}.navbar {
    padding: 20px 0px!important;
}
div.navbar-collapse{
    justify-content: center;
}
.navbar-nav .nav-link {
    padding-right: 1rem !important;
    padding-left: 1rem !important;
    text-align: center;
    color: #212529 !important;
    border-radius: .5rem;
    box-shadow: -7px -7px 20px 0px #fff9, -4px -4px 5px 0px #fff9, 7px 7px 20px 0px #0002, 4px 4px 5px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001;
    margin-bottom: 2%!important;
}
.navbar-nav .nav-item {
    margin: 0 .5rem;
}
.navbar-nav .nav-link:hover {
    box-shadow: inset 7px 7px 9px rgb(0 0 0 / 15%), inset -7px -7px 9px rgb(255 255 255 / 65%);
}
.line-height{
	line-height: 0%;
}
</style>
