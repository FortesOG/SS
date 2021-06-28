<template>
  <div id="app">
    <h1>SoccerStat
      
    </h1>
    
    <hr>

    
   <h2>
     Что такое SoccerStat?
   </h2>
   <p>SoccerStat - это приложение, с помощью которого можно отслеживать всю статистику ведущих европейский турниров по футболу</p>
   <hr>
    
    <h1> Актуально  </h1>

    <InfoPage
     v-bind:pageinfo="pageinfo"
     @go-to="goToo"
     
     
     />
     <hr>
    

  </div>


</template>


<script>
import InfoPage from '@/components/info.vue'


export default {
  name: 'App',
  data()
  {
    return {
      pageinfo: [
        {id: 1, title:'Список лиги',completed: true},
        {id: 2, title:'Список команд',completed: false},
        {id: 3, title:'Календарь лиг',completed: false},
        {id: 4, title:'Календарь команд',completed: false}
      ]
    }
  },
  methods:{
    goToo(id)
    {
      this.pageinfo= this.pageinfo.filter(t =>t.id!==id)
    }
  },
  components:
  {
    InfoPage
  }
  
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}


</style>


