<script>
export default {

  data() {
    return {
      userInput: "Write something!",
      userInput2: "",
      confirmedInput: "Write something and press enter"
  }
},

methods: {
  showAlert() {
    return alert("You have successfully triggered this alert")
  },

  saveInput(e) {
    this.userInput = e.target.value ? e.target.value : "Write something!";
  },

  saveInput2(e) {
    this.userInput2 = e.target.value
  },

  confirmInput() {
    this.confirmedInput = this.userInput2 ? this.userInput2 : "Write something and press enter";
  }
}



}


</script>


<template>
    <h1>Assignment-2</h1>
    <header>
        <h1>Events</h1>
      </header>
      <section id="assignment">
        <h2>Event Practice</h2>
        <!-- 1) Show an alert (any text of your choice) when the button is pressed -->
        <button @click="showAlert">Show Alert</button>
        <hr />
        <!-- 2) Register the user input on "keydown" and output it in the paragraph (hint: event.target.value helps) -->
        <input @keyup="saveInput" type="text"/>
        <p>{{ userInput }}</p>
        <hr />
        <!-- 3) Repeat 2) but only output the entered value if the ENTER key was pressed -->
        <input @keyup="saveInput2" @keyup.enter="confirmInput" type="text" />
        <p>{{confirmedInput}}</p>
      </section>
</template>


<style scoped>
header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: #1b995e;
  color: white;
  text-align: center;
}

#assignment {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

#assignment h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #1b995e;
  margin: 0 0 1rem 0;
}

#assignment p {
  font-size: 1.25rem;
  font-weight: bold;
  background-color: #8ddba4;
  padding: 0.5rem;
  color: #1f1f1f;
  border-radius: 25px;
}

#assignment input {
  font: inherit;
  border: 1px solid #ccc;
}

#assignment input:focus {
  outline: none;
  border-color: #1b995e;
  background-color: #d7fdeb;
}

#assignment button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

#assignment button:hover,
#assignment button:active {
  background-color: #ec3169;
  border-color: #ec3169;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}

</style>