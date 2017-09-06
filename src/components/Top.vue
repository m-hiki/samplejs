

<template>
    <!--<canvas v-attr="width:w, height:h"></canvas>-->
    <canvas></canvas>
</template>


<script>
// import createjs from 'createjs'
export default {
  name: 'top',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      w: 608,
      h: 602
    }
  },
  created: function () {
    console.log('hoge')
    /*
    var canvas = document.getElementById('canvas')
    this.stage = new createjs.Stage(canvas)
    var ctx = canvas.getContext('2d')
    ctx.scale(2, 2)
    this.stage.removeAllChildren()
    this.stage.clear()
    this.stage.enableMouseOver()
    this.isInit = true
    // this.loadPicture()
    // this.initManager()
    this.stage.update()
    this.canPendingView = true
    */
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
