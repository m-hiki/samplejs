

<template>
    <canvas id="canvas" width="608" height="602"></canvas>
</template>


<script>
import createjs from 'createjs'
export default {
  name: 'top',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      w: 608,
      h: 602
    }
  },
  mounted: function () {
    console.log('hoge')
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
    // sample
    var circle = new createjs.Shape()
    circle.graphics.beginFill('Crimson').drawCircle(0, 0, 50)
    circle.x = 100
    circle.y = 100
    this.stage.addChild(circle)
    createjs.Tween.get(circle, {loop: true})
          .to({x: 400}, 1000, createjs.Ease.getPowInOut(4))
          .to({alpha: 0, y: 75}, 500, createjs.Ease.getPowInOut(2))
          .to({alpha: 0, y: 125}, 100)
          .to({alpha: 1, y: 100}, 500, createjs.Ease.getPowInOut(2))
          .to({x: 100}, 800, createjs.Ease.getPowInOut(2))
    createjs.Ticker.setFPS(60)
    createjs.Ticker.addEventListener('tick', this.stage)
    //
    this.stage.update()
    this.canPendingView = true
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
