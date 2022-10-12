<template>
  <div id="app">
    <HeaderVue v-if='showHeader' v-bind:header="headerTxt" />
    <HeaderVue v-else header="Second Header" />
    <img alt="Vue logo" src="./assets/logo.png">
    <GoodComponent msg='hello'/>
    <RightPart number= 10 />
    <LeftPart image = '../assets/logo/png'></LeftPart>
    <ContactsList v-bind:phoneNumbers='phoneNumbers'/>
    <div className = 'button-container'>
      <button @click="hideWallets">Hide Wallets</button>
      <button @click="showWallets">Show Wallets</button>
    </div>
    <div class="container">
      <div class="card" :key="item.id" v-for="item in wallets">
        <div class="card-header">
          <h3>{{ item.address }}</h3>
          <p>{{ item.balance }} BTC</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GoodComponent from './components/GoodComponent.vue';
import RightPart from './components/RightPart.vue'
import LeftPart from './components/LeftPart.vue'
import HeaderVue from './components/HeaderVue.vue'
import ContactsList from './components/ContactsList.vue'
import wallets from './wallets.json'

export default {
  name: 'App',
  components: {
    RightPart,
    GoodComponent,
    LeftPart,
    HeaderVue,
    ContactsList
},
  data: ()=>({
    wallets:[],
    headerTxt: 'My Header',
    showHeader: false,
    phoneNumbers: [
  {
    "createdAt": "2021-05-02T21:30:25.793Z",
    "phoneNumber": "584-685-9289",
    "id": "1"
  },
  {
    "createdAt": "2021-07-21T09:20:27.068Z",
    "phoneNumber": "(300) 472-7336",
    "id": "2"
  },
  {
    "createdAt": "2021-05-07T08:39:49.178Z",
    "phoneNumber": "287-308-1738",
    "id": "3"
  },
  {
    "createdAt": "2020-12-22T00:36:24.078Z",
    "phoneNumber": "(842) 660-8761",
    "id": "4"
  }
]
  }),
  methods:{
    showWallets(){
      this.wallets = wallets
    },
    hideWallets(){
      this.wallets = []
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
button {
  padding: 0.6em 1em;
  margin: 0 1em;
  border: none;
  background-color: #41b883;
  font-size: 1.1rem;
  border-radius: 4px;
  cursor: pointer;
}

.card {
  border: 2px solid rgba(0, 0, 0, 0.2);
  border-radius: 6px;
  margin: 1em;
  min-width: 400px;
  background: #2c3e50;
  color: #fff;
}
</style>
