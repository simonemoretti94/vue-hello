<script>

export default {
  name: 'app',
  data() {
    return {
      greetings: 'Welcome to vue-hello repo!',
      name: '*',
      surname: '*',
    }
  },
  methods: {

  },
}

</script>

<template>
  <header>

    <h1>{{ greetings }}</h1>

  </header>

  <main>

    <div class="div-type1">
      <label for="name">Name</label>
      <input type="text" v-model="name">
    </div>

    <div class="div-type1">
      <label for="surname">Surname</label>
      <input type="text" v-model="surname">
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
  margin-top: 1rem;
  width: calc((100% / 12)* 8);
  display: flex;
  flex-direction: column;
  justify-content: center;

  & div-type1 {
    margin-top: .5rem;
    display: flex;
    flex-direction: row;
    justify-content: center;
    border: solid 1px white;
    border-radius: 10px;

    & label {
      text-align: center;

    }

    & input {
      text-align: center;
      border-radius: 10px;
    }

  }
}
</style>
