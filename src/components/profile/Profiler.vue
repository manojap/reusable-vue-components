<template>
  <div>
    <div class="background"></div>
    <div id="curve" class="card">
      <div class="footer">
        <div class="connections">
          <div class="connection facebook">  <a href="#"> <v-icon name="md-facebook" scale="1.5"/></a></div>
          <div class="connection twitter">   <a href="#"> <v-icon name="bi-twitter" scale="1.5"/></a></div>
          <div class="connection behance">  <a href="#"> <v-icon name="oi-octoface" scale="1.5"/></a></div>
        </div>
        <svg id="curve">
          <path
            id="p"
            d="M0,200 Q80,100 400,200 V150 H0 V50"
            transform="translate(0 300)"
          />
          <rect id="dummyRect" x="0" y="0" height="450" width="400" fill="transparent" />
          <!-- slide up-->
          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,50 Q80,100 400,50 V150 H0 V50"
            fill="freeze"
            begin="dummyRect.mouseover"
            end="dummyRect.mouseout"
            dur="0.1s"
            id="bounce1"
          />
          <!-- slide up and curve in -->
          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,50 Q80,0 400,50 V150 H0 V50"
            fill="freeze"
            begin="bounce1.end"
            end="dummyRect.mouseout"
            dur="0.15s"
            id="bounce2"
          />
          <!-- slide down and curve in -->
          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,50 Q80,80 400,50 V150 H0 V50"
            fill="freeze"
            begin="bounce2.end"
            end="dummyRect.mouseout"
            dur="0.15s"
            id="bounce3"
          />
          <!-- slide down and curve out -->
          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,50 Q80,45 400,50 V150 H0 V50"
            fill="freeze"
            begin="bounce3.end"
            end="dummyRect.mouseout"
            dur="0.1s"
            id="bounce4"
          />
          <!-- curve in -->
          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,50 Q80,50 400,50 V150 H0 V50"
            fill="freeze"
            begin="bounce4.end"
            end="dummyRect.mouseout"
            dur="0.05s"
            id="bounce5"
          />

          <animate
            xlink:href="#p"
            attributeName="d"
            to="M0,200 Q80,100 400,200 V150 H0 V50"
            fill="freeze"
            begin="dummyRect.mouseout"
            dur="0.15s"
            id="bounceOut"
          />
        </svg>
        <div class="info">
          <div class="name">Filan Fisteku</div>
          <div class="job">Architect Manager</div>
        </div>
      </div>
      <div class="card-blur"></div>
    </div>
  </div>
</template>

<script>
import OhVueIcon from "oh-vue-icons";

import {
  FaFlag,
  RiZhihuFill,
  MdFacebook,
  OiOctoface,
  BiTwitter,
  FaWordpress,
} from "oh-vue-icons/icons";

OhVueIcon.add(FaFlag, RiZhihuFill, MdFacebook, OiOctoface, BiTwitter, FaWordpress);

export default {
  name: "Profiler",
  created() {},
  components: {
    "v-icon": OhVueIcon,
  },
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style scoped>
html,
body {
  height: 100%;
  width: 100%;
}

.background {
  position: absolute;
  top: -40px;
  left: -40px;
  height: 120%;
  width: 120%;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  -webkit-filter: blur(30px);
  filter: blur(30px);
}

.card {
  /* position: absolute; */
  border-radius: 8px;
  height: 450px;
  width: 400px;
  /* top: 0;
    right: 0;
    left: 0;
    bottom: 0; */
  margin: auto;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  box-shadow: 0 0 80px -10px black;
  overflow: hidden;
}

.card-blur {
  position: absolute;
  height: 100%;
  width: calc(100% + 1px);
  background-color: black;
  opacity: 0;
  transition: opacity 0.15s ease-in;
}

.card:hover .card-blur {
  opacity: 0.6;
}

.footer {
  z-index: 1;
  position: absolute;
  height: 80px;
  width: 100%;
  bottom: 0;
}

svg#curve {
  position: absolute;
  fill: white;
  left: 0;
  bottom: 0;
  width: 400px;
  height: 450px;
}

.connections {
  height: 80px;
  width: 400px;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 100px;
  margin: auto;
}

.connection {
  height: 25px;
  width: 25px;
  border-radius: 100%;
  background-color: white;
  display: inline-block;
  padding: 5px;
  margin-right: 25px;
  transform: translateY(200px);

  transition: transform 1s cubic-bezier(0.46, 1.48, 0.18, 0.81);
}

.card:hover .connection {
  transform: translateY(0px);
}

.info {
  font-family: Inconsolata;
  padding-left: 20px;
  transform: translateY(250px);

  transition: transform 1s cubic-bezier(0.31, 1.21, 0.64, 1.02);
}

.card:hover .info {
  transform: translateY(0px);
}

.name {
  font-weight: bolder;
  padding-top: 5px;
}

.job {
  margin-top: 10px;
}

.connection.facebook {
  height: 35px;
  width: 35px;
  margin-left: 20px;
  padding: 0px;
  border-radius: 100%;
  overflow: hidden;
}

.connection.twitter {
  transition-delay: 0.06s;
}

.connection.behance {
  transition-delay: 0.12s;
}

.connection.facebook .icon {
  height: 100%;
  width: 100%;
  background-position: center;
  background-size: cover;
  background-color: black;
}

.connection.twitter .icon {
  height: 18px;
  width: 18px;
  margin-top: 1px;
  margin-left: 1px;
  background-position: center;
  background-size: cover;
}

.connection.behance .icon {
  height: 18px;
  width: 18px;
  margin-top: 3px;
  margin-left: 4px;
  background-position: center;
  background-size: cover;
}

.connection.facebook .icon {
}
.connection.twitter .icon {
}
.connection.behance .icon {
}

.card {
  background-image: url("background-image: url(`${https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/barbarian.png}`)");
}

.background {
  background-image: url("background-image: url(`${https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/barbarian.png0}`)");
}
</style>
