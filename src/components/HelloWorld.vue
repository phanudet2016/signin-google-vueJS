<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="google()">google login</button>
  </div>
</template>

<script>
import { FIREBASE_AUTH, PROVIDER_AUTH } from './firebase'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Signin with Google'
    }
  },
  methods: {
    google () {
      FIREBASE_AUTH.signInWithPopup(PROVIDER_AUTH).then((result) => {
        console.log(result) // เอาไปทำไรก็เเล้วเเต่เลยนะครับ
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
