<template>
  <div>
    <h1>asyncData</h1>
    <p>{{info.name}}</p>
    <p>{{info.age}}</p>
    <p>{{info.render}}</p>
  </div>
</template>

<script>
  import axios from 'axios'
  
  export default {
    data () {
      return {
        // info: {}
        name:'hello World'
      }
    },
    async asyncData () {
      let {data} = await axios.get('https://api.myjson.com/bins/pgsv2')
      return {
        info: data
      }
    }
  }
</script>