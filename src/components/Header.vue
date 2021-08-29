<template>
  <header>
	 <div class="container mt-0">
      <nav class="navbar px-2 mt-0  navbar-expand-lg navbar-light bg-light neo-shadow">
        <router-link class="ml-3 navbar-brand text-primary" to="/">  Movies App</router-link>
		<router-view/>
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
              <router-link class="nav-link" to="/"
                >Home <span class="sr-only"></span></router-link
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
		  <!-- <div class="movies_list" v-for="movie in movies" :key="movie.imdbID">
			  {{movie.Title}}
		  </div> -->
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
	name : 'Header',
	props : ['search','movies','searchMovies']
}
</script>

<style>

</style>