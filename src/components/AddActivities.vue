<template>
  <div class="main">
      
   <form>
       <h2> Activity Suggester</h2>
       <p id="description">Tell us how do You feel and we will suggest an activty!</p>
       <b-field>
            <b-select placeholder="Select">
                <option value='bored' name="bored">Bored</option>
                <option value="chilled" name="chilled">Chilled</option>
                <option value="energy" name="energy">Full of energy</option>
                <option value="lonely" name="lonely">Lonely</option>
            </b-select>
        </b-field>
       <button type="submit">Submit</button>
   </form>
   <h3> Chosen activity:</h3>
   <div class="display">


   </div>
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
form{
    display: block;
    all:unset;
    margin-top: 20px;
    padding-top: 20px;
}


input{
    all:unset;
    border: 1px solid lightgray;
    padding:12px;
    text-align: left;
    background-color: lightgray;
    border-radius:10px;
}

button{
    all:unset;
    background:black;
    color:white;
    padding:12px;
    margin-left: 15px;
    text-align: left;
    border-radius: 10px;
}

.main{
    background: rgb(113,107,251);
    background: linear-gradient(180deg, rgba(113,107,251,1) 0%, rgba(153,131,247,1) 54%, rgba(255,241,245,1) 100%);
    height:450px;
    border-radius: 10px;

}

#input{
    margin-top:30px;
}

h2{
    color:white;
    font-size: 40px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

h3{
    margin-top: 5px;
    color:white;
    font-size: 40px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

#description{
    color:white;
}


.display{
    width:50%;
    border-radius: 10px;
    height: 45px;
    background-color: white;
    margin:75px auto;
    color:black;
}



</style>
