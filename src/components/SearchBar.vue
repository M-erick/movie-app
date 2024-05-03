<template>
  <div>
    <form @submit.prevent="SearchMovies()" class="search-box">
  <input type="text"  placeholder="search movie" value="" v-model="search">
  <input type="submit" value="Search">
</form>
  </div>
</template>

<script>
export default {
    name:'SearchBar',
    setup(props){
        const SearchMovies = ()=>{
          if (search.value != "") {
        fetch(`http://www.omdbapi.com/?apikey=${env.apikey}&s=${search.value}`)
          .then(response => response.json())
          .then(data => {
            movies.value = data.Search;
            search.value = " ";
          })
          .catch (error=>{ 
    console.error('Error fetching movie data:', error);
          });  
        }
        }
        return{
            SearchMovies,

        }
    }

}
</script>

<style>

</style>