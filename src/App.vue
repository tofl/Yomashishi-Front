<template>
  <div id="app">

    <div id="intro">
      <div class="page">
        <div class="header-text">
          <p class="headline">
            Get that weight off your shoulders
          </p>
          <p class="description">
            Yomashishi is a <strong>minimalist</strong> & <strong>simplistic</strong> task planner, built wit Electron ⚛. It sits right in your menu bar, letting you stay on top of your day.
          </p>
          <p class="link">👉 <a href="#" class="download">Download Yomashishi</a><span class="link-smaller"> *</span></p>
          <p class="its-free"><span class="link-smaller">* it's free</span></p>
        </div>
        <p class="screenshot"><img src="./assets/capture.png" alt="Yomashishi - Simple task planner" /></p>
      </div>
    </div>

    <div id="description">
      <div class="page">
        <p class="title">Stay tuned 🔔</p>
        <p class="send-email-description">
          I'm Tom, an independent developer. This is a really basic MVP, and I intend to keep working on it. Lots of new features are coming up!
          <br /><br />
          Feel free to subscribe to my mailing list to stay up to date on the latest features (promise I won't give you address to anyone).
        </p>
        <Subscribe></Subscribe>
      </div>
    </div>

  </div>
</template>

<script>
import Subscribe from './components/Subscribe'

export default {
  name: 'app',
  components: {
    Subscribe

  }
}
</script>

<style>
  @font-face {
    font-family: Montserrat;
    src: url("/assets/Montserrat.ttf");
  }
  @font-face {
    font-family: Hind;
    src: url("/assets/Hind.ttf");
  }

  * {
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Hind, sans-serif;
    color: #292929;
  }

  .page {
    max-width: 600px;
    margin: auto;
  }

  #intro {
    text-align: center;
    min-height: 100vh;
    background-color: #e1eefc;
  }

  #description {
    min-height: 100vh;
    background-color: #e0fcee;
  }

  .headline {
    font-family: Montserrat, sans-serif;
    font-weight: bold;
    font-size: 3em;
    margin-bottom: 20px;
  }

  .description {
    max-width: 85%;
    margin: auto auto 20px;
  }

  .link {
    margin-bottom: 10px;
  }

  .download {
    font-size: 1.5em;
    text-decoration: none;
    color: #2267ff;
    font-weight: bold;
    border-bottom: 2px solid #2267ff;
  }
  .download:active {
    position: relative;
    top:2px;
  }

  .link-smaller {
    font-size: 1.1em;
    color: #5b5b5b;
  }

  .its-free {
    margin: auto;
    width: 80%;
    text-align: left;
  }

  .screenshot img {
    width: 80%;
    min-width: 300px;
  }

  .title {
    font-size: 1.4em;
    font-weight: bold;
    font-family: Montserrat, sans-serif;
    padding: 20px 10px;
  }

  .send-email-description {
    padding: 10px;
    text-align: justify;
    line-height: 25px;
    font-size: 1.2em;
  }
</style>
