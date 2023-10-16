<script>

export default {
  data() {
    return {
      name: " Óli Viðar",
      movies: ["Blu beatle", "deadpool", "spider-man: no way home", "haunting in venice"]
    }
  }
}
</script>

<style>
html, body{
  height: 100%;
}

body {
  display: grid;
  background-image: url("");
  background-repeat: no-repeat;
  background-size: cover;
}

.about{
  display: flex;
  flex-direction: column;
  justify-content: left;
  padding: 15px;
  margin-left: 50px;
  margin-right: 50px;
  background-color: darkblue;
  border-radius: 6px;
}

main{
  display: flex;
  justify-content: center;
  padding: 20px;
  text-align: left;
}

li{
  margin-bottom: 15px;
  padding: 35px;
  width: 100%;
  background-color: white;
  border-radius: 6px;
}

</style>

<template>
  <div class="about">

    <main>
      Væntanlegt
    </main>

    <ul>
      <li v-for="movie in movies">{{ movie }}</li>
    </ul>

  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>