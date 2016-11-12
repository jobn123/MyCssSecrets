<template>
  <div class="hello">
    <div class="" id="test">

    </div>
    <figure class="tb_container">
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
    <figure class="mb_container">
      <figcaption>
        多重边框
      </figcaption>
      <div class="multiple_border" id="tb">
      </div>
      <figcaption style="margin-top:20px;text-align:center">
        box-shadow支持逗号分隔，可以创建任意数量投影
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
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
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
.tb_container {
  background: gray;
}
.mb_container {
  background: white;
}
.translucent_border {
  width: 50px;
  height: 50px;
  border: 10px solid hsla(0, 0%,100%,.5);
  background: green;
  background-clip: padding-box;
}
.multiple_border {
  width: 50px;
  height: 50px;
  background: yellowgreen;
  box-shadow: 0 0 0 10px #655,
              0 0 0 15px deeppink,
              0 2px 15px 15px rgba(0, 0, 0, 0.6);
  margin: 0 auto;
}
</style>
