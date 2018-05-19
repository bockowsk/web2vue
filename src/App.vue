<template> 
    <div>
      <p>Twoj e-mail to {{email}}</p>
<!--
        <p><input type="email" v-model="email"/><button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button></p>
        <div v-if="email.length < 10">Ale masz krótki adres!</div>
        <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
        <div v-else>Twój adres e-mail jest stanowczo za długi.</div>
        <p>Witaj w systemie do zapisow na zajeciac</p>
-->
        <p v-if="login == 0"> Zaloguj sie e-maile'em: <input type="login" v-model="wartosc"/><button @click="myToogle()">Wchodze</button></p>
        <p v-if="login == 1"> Zalogowany!<button @click="myToogle()">Wychodze</button></p>
    </div>
    
</template>

<script>
import "milligram";
export default {
  name: "app",
  data() {
    return {
      msg: "Hello World!!!",
      email: "bockowsk@student.agh.edu.pl",
      login: 0
    };
  },
  methods: {
    alertMyEmail() {
      alert(this.email);
    },
    logujSie() {
      this.login = 1;
    },
    wylogujSie() {
      this.login = 0;
    },
    myToogle() {
      this.login=!this.login
    }
    
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
