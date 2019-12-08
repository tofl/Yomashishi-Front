<template>
  <div>
    <h2 class="subscribe-title">Subscribe</h2>
    <form @submit.prevent="subscribe" v-if="!subscribed">
      <input type="email" v-model="email" placeholder="E-mail address" required /><input type="submit" value="Subscribe" />
    </form>
    <p v-else>You are now subscribed to my email list! You can unsubscribe at any moment by simply replying to one of my emails.<br /><span class="subscribe-again" @click="subscribeAgain()">Subscribe again</span></p>

  </div>
</template>

<script>
  export default {
    name: "Subscribe",
    data() {
      return {
        email: "",
        subscribed: false
      }
    },
    methods: {
      subscribe: function() {
        this.email = "";
        this.subscribed = true;
      },
      subscribeAgain: function() {
        this.subscribed = false;
      }
    }
  }
</script>

<style scoped>
  h2 {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 10px;
  }

  form {
    width: 300px;
    border: 2px solid #eaeaea;
    border-radius: 10px;
    background-color: white;
    display: flex;
  }

  input {
    border: none;
    background-color: transparent;
  }

  input[type=email] {
    padding: 0 5px;
    height: 50px;
    font-size: 1em;
    outline: none;
    flex-grow: 2;
  }

  input[type=submit] {
    height: 50px;
    border-left: 1px solid #eaeaea;
    font-size: 0.9em;
    border-radius: 0;
    outline: none;
    flex-grow: 1;
    cursor: pointer;
  }

  .subscribe-again {
    border-bottom: 1px solid black;
    cursor: pointer;
  }
</style>
