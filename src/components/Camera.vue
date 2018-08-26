<template>
  <div class="">
      <video autoplay playsinline muted id="webcam" width="250" height="250"></video>
  </div>
</template>

<script>
import {Webcam} from '../assets/webcam'

export default {
  name: "Camera",
  data: function(){
      return {
          webcam: null,
      }
  },
  mounted: function(){
      this.loadWebcam();
  },
  methods: {
      loadWebcam: function(){
          this.webcam = new Webcam(document.getElementById('webcam'));
          this.webcam.setup();
      }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
