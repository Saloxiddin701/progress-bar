<template>
  <div id="app">
    <main>
      <div class="navigation">
        <header>
          <h1>Sayfuddinov Saloxiddin</h1>
        </header>
        <nav>
          <a href="#">About Us</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <progress-bar :progress="progress" />
      <post @progressUpdate="setProgress"/>
    </main>
  </div>

</template>

<script>
  import post from "@/components/post";
  import progressBar from "@/components/progressBar";

  export default {
    name: 'App',
    components: {
      post,
      progressBar
    },
    data() {
      return  {
        progress: 0
      }
    },
    methods: {
      setProgress(progress) {
        this.progress = progress
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'monospace', sans-serif;
  }
  main {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    overflow: hidden;
  }
  .navigation {
    width: 100%;
    height: 10vh;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #000;
    padding: 30px;
  }
  header h1 {
    color: #fff;
    font-size: 32px;
  }
  nav a {
    text-transform: uppercase;
    text-decoration: none;
    color: #ffffff;
    font-size: 18px;
    margin: 0 20px;
  }
</style>
