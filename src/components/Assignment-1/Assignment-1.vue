<script setup>

const name = "Deniss";
let age = 36;
const yearsToAdd = 5;
const vueLogoUrl = "https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png";


const randomNumber = () => {
    return  Math.random();
}

const agePlus = () => { 
    return age + yearsToAdd;
}



</script>


<template>
    <h1>Assignment-1</h1>
    <section id="assignment">
          <!-- 1) Output your name -->
          <h2>{{ name }}</h2>
          <!-- 2) Output your age -->
          <p>{{ age }}</p>
          <!-- 3) Output your age + 5 -->
          <p>I will be age {{ agePlus()}} after {{ yearsToAdd }} years </p>
          <!-- 4) Output a random number (0 to 1) -->
          <p >Favorite Number: {{randomNumber()}}</p>
          <div>
            <!-- 5) Display some image you found via Google -->
            <img v-bind:src="vueLogoUrl"/>
          </div>
          <!-- 6) Prepopulate the input field with your name via the "value" attribute -->
          <input type="text" v-bind:value="name"/>
        </section>
</template>


<style scoped>

section {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #970076;
  margin: 0 0 1rem 0;
}

p {
  font-size: 1.25rem;
  font-weight: bold;
  background-color: #970076;
  padding: 0.5rem;
  color: white;
  border-radius: 25px;
}

input {
  font: inherit;
  border: 1px solid #ccc;
}

input:focus {
  outline: none;
  border-color: #1b995e;
  background-color: #d7fdeb;
}

button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

button:hover,
button:active {
  background-color: #ec3169;
  border-color: #ec3169;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}

img {
    width: 100px;
}


</style>