<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()


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
        <div id="sidebar" class="container"> Sidebar </div>
        <div id="main" class="container"> Text input </div>
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