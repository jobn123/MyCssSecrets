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
    <figure class="c1">
      <figcaption>
        边框内圆角
      </figcaption>
      <div class="c1-out-div">
        <div class="c1-inner-div">
          边框内圆角
        </div>
      </div>
    </figure>
    <figure class="c2">
      <figcaption>
        条纹背景
      </figcaption>
      <div class="c2-out-div">

      </div>
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
.c1 {
  width: 100%;
}
.c1-out-div {
  background: #655;
  padding: .8em;
  width: 200px;
  margin: 0 auto;
}
.c1-inner-div {
  background: tan;
  border-radius: .8em;
  padding: 1em;
}
.c2-out-div {
  width: 100%;
  height: 100px;
  background: -webkit-linear-gradient(#fb3 50%, #58a 50%);
  background-size: 100% 20px
}
</style>
