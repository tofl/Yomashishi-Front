<template>
  <div>
    <span>Subscribe</span>
    <form @submit.prevent="">
      <input type="email" v-model="email" placeholder="E-mail address" /><input type="submit" value="Subscribe !" />
    </form>
  </div>
</template>

<script>
  export default {
    name: "Subscribe",
    data() {
      return {
        email: "tom.flitterman@hotmail.fr"
      }
    }
  }
</script>

<style scoped>
  span {
    font-size: 1.2em;
    font-weight: bold;
  }

  input {
    margin: 0;
    background-color: white;
    border-top: 2px solid #eaeaea;
    border-bottom: 2px solid #eaeaea;
  }

  input[type=email] {
    padding: 0 5px;
    width: 200px;
    height: 50px;
    border-left: 2px solid #eaeaea;
    border-right: none;
    border-radius: 10px 0 0 10px;
    font-size: 1em;
    outline: none;
  }

  input[type=submit] {
    width: 100px;
    height: 54px;
    border-right: 2px solid #eaeaea;
    border-left: 1px solid #eaeaea;
    border-radius: 0 10px 10px 0;
    font-size: 0.9em;
    outline: none;
  }
</style>
