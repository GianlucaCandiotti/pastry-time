<template>
  <div>
    what
    <ul>
      <li v-for="user in users">
        {{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script>
import firebase from 'firebase';
import firebaseConf from 'root/firebaserc.js';

const firebaseApp = firebase.initializeApp(firebaseConf);

const db = firebaseApp.database();

export default {
  firebase: {
    users: db.ref('users'),
  },
};
</script>

<style lang="sass" src="./scss/index.scss"></style>
