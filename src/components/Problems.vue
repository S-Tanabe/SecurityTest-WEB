<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <div id="table">
      <table>
        <thead>hogehoge</thead>
        <tbody>
          <tr>
            <th>ID</th>
            <th>TITLE</th>
            <th>CONTENT</th>
            <th>POINT</th>
          </tr>
          <tr v-for="problem in problems">
            <td>{{ problem.id }}</td>
            <td>{{ problem.title }}</td>
            <td>{{ problem.content }}</td>
            <td>{{ problem.point }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',

  created: function () {
    axios.get('http://13.114.78.37:8888/problems')
      .then(response => {
        this.problems = response.data
        console.log(response.data) // mockData
        console.log(response.status) // 200
      })
  },

  data () {
    return {
      msg: 'Problems',
      problems: []
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
