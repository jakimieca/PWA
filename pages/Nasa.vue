<template>
    <div>
      <h1>Nasa</h1>
    
      <div style="display: flex; flex-wrap: wrap; width: 100vw; justify-content: center">
        <img
          :src="value.links[0].href"
          v-for="(value, index) in dataArr"
          :key="index"
          style="width: 100px; height: 100px; object-fit: cover; padding: 5px"/>
      </div>
    
    </div>
    </template>
    
    <script>
    import axios from "axios";
    export default {
      name: "index",
      created() {
        this.fetchData()
      },
      data() {
        return {
          dataArr: []
        }
      },
      methods: {
      async fetchData() {
        await axios.get('https://images-api.nasa.gov/search?q=sun')
          .then(res => {
            // console.log(res.data.collection.items[3].links[0].href)
            this.dataArr = res.data.collection.items;
          })
          .catch(error => {
            console.log(error)
          })
        }
      }
    }
    </script>
    
    <style scoped>
    </style>