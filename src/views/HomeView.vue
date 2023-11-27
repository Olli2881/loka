<script>
import axios from 'axios';
export default {
  data() {
    return {
      name: " Óli Viðar",
      movies: []
    }
  },
  mounted() {
    axios.get('https://grouplimit.co/api/v1/cinema/LFZHAia7t0NjjJ62F2pB')
        .then( (response) => {
          // handle success
          console.log(response);
          this.movies = response.data.data
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        })
        .finally(function () {
          // always executed
        });
  }
}
</script>

<style>

a{
  color: darkblue;
}

body {
  display: grid;
  background-image: url("");
  background-repeat: no-repeat;
  background-size: cover;
  color: black;
}

.home{
  display: inline-block;
  justify-content: center;
  width: auto;
  padding: 15px;
  background-color: darkred;
  border-radius: 20px;
}

.location{
  display: flex;
  flex-direction: column;
  background-color: darkred;
}

.movie_time{
  display: flex;
  flex-direction: column;
  padding-bottom: 2px;
}

.show{
  display: flex;
  flex-direction: column;
  background-color: gray;
  padding-bottom: 3px;
}

.rating{
  display: flex;
  left: auto;
}

h3{
  display: flex;
  left: auto;
  padding-left: 10px;
}

div{
  margin-bottom: 15px;
  padding: 10px;
  background-color: white;
  border-radius: 5px;
  display: inline-block;
  float: left;
  width: auto;
}

img{
  display: inline-block;
  float: left;
  height: 350px;
  width: 250px;
  padding: 10px;
}

main{
  display: flex;
  justify-content: center;
  padding-bottom: 25px;
  color: gold;
}

span{
  display: flex;
  justify-content: left;
}

h1{
  display: flex;
  justify-content: center;
  padding: 10px;
}

</style>

<template>

  <div class="home">

    <main>
      <strong>
        Heima Síðan
      </strong>
    </main>

    <div class="location">

      <div v-for="movie in movies" >

        <img :src="movie.poster">

        <h3><strong> {{ movie["name"] }} ({{ movie.year }})</strong></h3>

        <div class="rating">
          <span>
              <p>
                Imdb raiting: <strong>{{ movie.imdb_rating }}</strong>
              </p>
          </span>
        </div>

        <div v-for="(showtime,name) in movie.showtimes" >

          <h1>
            <strong> {{name}} </strong>
          </h1>

          <div class="show">

            <div class="movie_time" v-for="time in showtime">

              <div>
                {{time.location}} - {{time.time}}
              </div>

            </div>

          </div>

        </div>

      </div>

    </div>

  </div>

</template>

<style>
@media (min-width: 1024px) {
  .home {
    min-height: 100vh;
    display: inline-block;
    align-items: center;
  }
}

@media (min-width: 1024px) {
  .movie_time {
    display: inline-block;
    align-items: center;
  }
}
</style>