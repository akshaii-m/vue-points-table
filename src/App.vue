<template>
  <div id="app">
    <pointsTable :info="info" />
  </div>
</template>

<script>
import pointsTable from "./components/pointsTable.vue";


export default {
  name: "App",
  components: {
    pointsTable,
  },
  data() {
    return {
      info: [],
    };
  },
 
  created() {
    fetch("./data.json")
      .then((res) => res.json())
      .then((data) => this.info =
      data.standings.stages.stage[0].group[0].entities.entity)
    
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}



</style>
