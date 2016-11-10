<template>
  <div class="hello">
    <div class="" id="test">

    </div>
    <figure>
      <figcaption>
        半透明边框
      </figcaption>
      <div class="translucent_border" id="tb">
      </div>
      <figcaption>
        <pre>
          background-clip: padding-box;
        </pre>
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created() {
    debugger
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    debugger
    console.log("mounted");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroy() {
    console.log("destroy");
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.translucent_border {
  width: 50px;
  height: 50px;
  border: 10px solid hsla(0, 0%,100%,.5);
  background: green;
  background-clip: padding-box;
}
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
