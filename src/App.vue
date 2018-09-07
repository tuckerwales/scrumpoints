<template>
  <div id="app">
    <img class="logo" alt="Scrum Master" src="./assets/logo.png">
    <h1>Scrum Points</h1>
    <label for="velocity">Team Velocity</label>
    <input id="velocity" type="text" v-model="velocity">
    <label for="hours">Number of hours</label>
    <input id="hours" type="text" v-model="hours">
    <label for="people">Number of people</label>
    <input id="people" type="text" v-model="people">
    <h2 class="points">That's {{ Math.round((velocity / 7.5) * hours * people) }} point(s)</h2>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      velocity: 10,
      hours: 1,
      people: 1,
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
.logo {
  width: calc(100vh * 0.4);
}
label {
  display: block;
}
input + label {
  margin-top: 20px;
}
.points {
  margin-top: 30px;
}
</style>
