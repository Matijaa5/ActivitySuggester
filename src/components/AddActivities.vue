<template>
  <div class="main">
      
   <form>
       <h2> Activity Suggester</h2>
       <p id="description">Tell us how do You feel and we will suggest an activty!</p>
     
            <input class="selection" type="button" value="Bored" @click="handleTerrible">
            <input class="selection" type="button" value="Stressed" @click="handleBad">
            <input class="selection" type="button" value="Producitve" @click="handleMeh">
            <input class="selection" type="button" value="Lonely" @click="handleGood">
            <input class="selection" type="button" value="Full of energy" @click="handleGreat">
          
        
      
   </form>
   <h3> Chosen activity:</h3>
   <div class="display">
        <div  id="terribleId" v-if="terrible" v-bind:style="{backgroundColor:backgroundColor,}" >
            <p>Something useful you can do<br/>

        <p v-bind:style="{color:textColor}">Change color to end boredom</p><br/><br/>
            Text color: <input type="color" v-model="textColor"><br>
            Background color:<input type="color" v-model="backgroundColor"><br>
            Type a color:<input type="text" v-model="backgroundColor"><br>    
        </div>
        <div id="badId" v-if="bad">
            <p>Feeling stressed?</p> <br/>
            Here are some ways to reduce stress.<br/>
            <a href="https://www.healthline.com/nutrition/16-ways-relieve-stress-anxiety">Stress solutions</a>
        </div>
        <div id="mehId" v-if="meh">
            Learn a new skill. No matter where you are in your life, there's always room to learn new skills!<br/>
        </div>
        <div id="goodId" v-if="good">
            Call a friend and hangout!
              
        </div>
        <div id="greatId" v-if="great">
             Go for a walk! <br/>
             Start working out! <br/>
             Play sports!
            
        </div>
             
    </div>
       

  </div>
</template>

<script>
export default {
    data(){
        return{
      terrible:false,
      bad:false,
      meh:false,
      good:false,
      great:false,

      textColor:"#000000",
      backgroundColor:"white"
        }
    },
      methods: {
    handleTerrible(){
      console.log("Terrible"),
       this.terrible=true;
       this.bad=false;
       this.meh=false;
       this.good=false;
       this.great=false;
      
    },
    handleBad(){
      console.log("Bad"),
       this.terrible=false;
       this.bad=true;
       this.meh=false;
       this.good=false;
       this.great=false;
    },
    handleMeh(){
      console.log("Meh"),
       this.terrible=false;
       this.bad=false;
       this.meh=true;
       this.good=false;
       this.great=false;
    },
    handleGood(){
      console.log("Good"),
       this.terrible=false;
       this.bad=false;
       this.meh=false;
       this.good=true;
       this.great=false;
    },
    handleGreat(){
      console.log("Great"),
       this.terrible=false;
       this.bad=false;
       this.meh=false;
       this.good=false;
       this.great=true;
       
    },

    
  },
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


/*input{
 /*   all:unset;
    border: 1px solid lightgray;
    padding:12px;
    text-align: left;
    background-color: lightgray;
    border-radius:10px;
}*/



button{
    all:unset;
    background:black;
    color:white;
    padding:12px;
    margin-left: 15px;
    text-align: left;
    border-radius: 10px;
}

.selection:hover{
    background-color:lightgray; 
  color: rgb(0, 0, 0);
}


input:hover {
  background-color:lightblue; 
  color: white;
}

.main{
   background: rgb(113,107,251);
   
   background: linear-gradient(180deg, rgba(113,107,251,1) 0%, rgba(153,131,247,1) 54%, rgba(255,241,245,1) 100%);
  
    min-height:450px;
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
    background-color: white;
    margin:75px auto;
    color:black;
}
input[type="button"]{
    all:unset;
    color:white;
    border: none;
    padding:12px;
    text-align: left;
    background-color: black;
    border-radius:10px;
    margin:5px;
}


</style>