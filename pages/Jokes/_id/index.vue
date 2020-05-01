<template>
    
<div>
  <button><nuxt-link to="/jokes"> Back to Jokes</nuxt-link></button><br/><br/>
  <table border="1">
      <tr>
          <th>Joke ID </th>
          <th>Joke </th>
      </tr>
      <tr>
          <td>{{ $route.params.id }}</td>
           <td>{{ joke }}</td>

      </tr>
      
  </table>
  
</div>
</template>

<script>
import axios from 'axios';
export default {
    data(){
        return{
            joke:{}
        }
    },
   async created(){
        const config = {
            headers: {
                'Accept':'application/json'
            }
        }
       
           try {
               
                 const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`,config)
                    
                    this.joke = res.data.joke;
                    console.log(this.joke)
           } catch (error) {
               console.log(error);
           }
    },
    head(){
        return {
            title: this.joke
    }

}
}
</script>

<style>


</style>