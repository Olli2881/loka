<script>

export default {
  data() {
    return {
      name: " Óli Viðar",
      movies: ["Blu beatle", "deadpool", "spider-man: no way home", "haunting in venice"],
      times: ["19:00", "20:00", "21:00"]
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
  color: darkblue;
}

.home{
  display: flex;
  flex-direction: column;
  padding: 15px;
  margin-left: 50px;
  margin-right: 50px;
  background-color: #8B0000;
  border-radius: 6px;
}

main{
  display: flex;
  justify-content: center;
  padding: 20px;
  text-align: left;
  color: white;
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

  <div class="home">

    <main>
      Heima síða
    </main>

    <ul>
      <li>Mynd 1</li>
      <li>Mynd 2</li>
      <li>Mynd 3</li>
      <li>Mynd 4</li>
    </ul>

  </div>

</template>

<style>
@media (min-width: 1024px) {
  .home {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>