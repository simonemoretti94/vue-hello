<script>

export default {
  name: 'app',
  data() {
    return {
      greetings: 'Welcome to vue-hello repo!',
      name: '',
      surname: '',
    }
  },
  methods: {
    lengthCalculator(nome, cognome) {
      return nome.length + cognome.length;
    },
    evenOrOdd(nameSurnameLength) {
      if (nameSurnameLength % 2 === 0 && nameSurnameLength !== 0) {
        return 'is even!';
      }
      else if (nameSurnameLength === 0) {
        return 'is null!';
      }
      else {
        return 'is odd!';
      }
    }
  },
  backvariation(id) {
    document.getElementById(`${id}`).style.backgroundColor = 'green';
  }
}

</script>

<template>
  <header>

    <h1>{{ greetings }}</h1>

  </header>

  <main>

    <div id="div-type1">
      <label for="name">Name</label>
      <input type="text" v-model="name">
    </div>

    <div id="div-type1">
      <label for="surname">Surname</label>
      <input type="text" v-model="surname">
    </div>

    <div id="div-type2">
      <p>So you are {{ name + ' ' + surname }}, even {{ lengthCalculator(name, surname) }} characters!</p>
    </div>

    <div id="div-type3">
      <p id="p-output">{{ lengthCalculator(name, surname) }} {{
        evenOrOdd(lengthCalculator(name, surname)) }}</p>
    </div>


  </main>
</template>

<style>
template {
  display: flex;
  flex-direction: column;
  align-items: center;
}

header {
  height: 200px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

  & h1 {
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-style: italic;
    color: white;
    text-shadow: 2px 3px rgb(93, 93, 93);
  }
}

main {
  margin: 1rem auto auto auto;
  width: calc((100% / 12)* 6);
  display: flex;
  flex-direction: column;
  justify-content: center;

  & #div-type1 {
    margin-top: .5rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border: solid 2px white;
    border-radius: 10px;

    & label {
      text-align: center;
      margin-left: .5rem;

    }

    & input {
      text-align: center;
      border-radius: 10px;
    }

  }

  & #div-type2 {
    margin-top: 1rem;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    border: dashed 2px white;
    border-radius: 15px;
  }

  #div-type3 {
    margin-top: 1rem;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    border: groove 2px rgb(95, 191, 254);
    border-radius: 20px;
    box-shadow: 4px 6px rgb(179, 179, 179);
  }
}
</style>
