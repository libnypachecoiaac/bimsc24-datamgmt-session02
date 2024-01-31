<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()

let text = ref("Fact # 01: Cows moo.")


// create a function that plays the sound of a cow mooing
function playSound() {
    let audio = new Audio("/moo.mp3")
    audio.play()
}

function doSomething() {

    // create a paragraph element
    let p = document.createElement("p")

    // fill that p element with some text
    let inputText = input.value
    p.innerHTML += inputText
    console.log(inputText)

    // append that element to main
    main.appendChild(p)

}


function Refresh() {
    // delete all the p elements
    let p = document.querySelectorAll("p")
    for (let i = 0; i < p.length; i++) {
        p[i].remove()
    }
    
}


</script>



<!-- the template is where the html code goes -->
<template>


    <div id="navbar" class="container">  
        <div id="title">That Vegan Cow!</div>
        <div id="logo">
            <img src="/cow.jpg" alt="macad cow">
        </div>
    </div>

    <div id="flex">
        <div id="sidebar" class="container">
            <input type="text" id="input" placeholder="Enter text here"> 
            <button @click="doSomething">Add</button>
            <button @click="Refresh">Refresh</button>



        </div>
        <div id="main" class="container"> {{text}} </div>
    </div>


</template>



<!-- style is where the css code goes -->
<style scoped>

html{
    
    background-color: rgb(59, 59, 59); 
    color: white;
}

body{

    margin:0;
}

div{

    /* put the borders in the inside of container */
    box-sizing: border-box;
}

img{

    height: 100%;
    width: auto;

}

button{

    font-size: 20px;
    background-color: rgb(8, 33, 5);
    color: white;
    border-radius: 1px;
    padding: 5px;
    margin: 5px;
    cursor: pointer;
    transition-duration: 0.4s;
    font-family: 'Courier New', Courier, monospace;
    font-style: italic;
    font-weight: bold;
    /* change color when hovering with mouse pointer */
    &:hover{
        background-color: rgb(235, 233, 213);
        color: rgb(235, 233, 213);
    }

}

#navbar{

    height: 50px;
    background-color: rgb(8, 33, 5);
    /* add shadow */
    box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.315);
    /* bring to front */
    position: relative;

}

#flex{
    
    display: flex;
    height: calc(100vh - 50px);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 20px;
    text-decoration: underline;
}

#sidebar{
    
    width:30%;
    box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.315);
    position: relative;
    

}

#main{
    width:70%;
    background-color: rgb(235, 233, 213);

}

#title{
    width: 70%;
    float:left;
    font-family: 'Courier New', Courier, monospace;
    font-style: italic;
    font-size: 40px;
    font-weight: bold;
    color: rgb(255, 255, 255);
    text-align: center;
}

#logo{
    width: 30%;
    height: 100%;
    float:right;
    text-align: right;

}

.container{

    /* border-style: dotted; */
    border-width: 1px;
    /* change font size */
    font-size: 30px;
    

}

</style>