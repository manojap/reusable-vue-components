<template>
  <div class="container">
    <div class="coast">
      <div class="wave-rel-wrap">
        <div class="wave"></div>
      </div>
    </div>
    <div class="coast delay">
      <div class="wave-rel-wrap">
        <div class="wave delay"></div>
      </div>
    </div>
    <div>
      <div class="text text-a">{{txt[0] }}</div>
      <div class="text text-v">{{txt[1]}}</div>
      <div class="text text-e">{{txt[2]}}</div>
    </div>

    <!-- </di <div class="text t{xt-a">a</div>
  <div class="text text-v">v</div>
  <div class="text text-e">e</div>v> -->
    <!-- <div class="text text-w">{{text}}</div> -->
    <!-- <div class="text text-a">a</div>
  <div class="text text-v">v</div>
  <div class="text text-e">e</div> -->
  </div>
</template>

<script>
export default {
  name: "LWave",
  created() {},
  data() {
    return {};
  },
  computed: {
    txt() {
      return this.text.split("");
    },
  },
  props: {
    text: {
      type: String,
      default: "Vuejs",
    },
  },
  methods: {},
};
</script>

<style lang="css" scoped>
@import url("https://fonts.googleapis.com/css?family=Muli");
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html,
body {
  font-size: 62.5%;
  background-color: #00091b;
  font-family: "Muli", Helvetica, sans-serif;
}

.container {
  /* position: absolute; */
  width: 17rem;
  height: 10rem;
  /* left: 50%; */
  /* top: 50%; */
  transform: translate(-50%, -50%);
}

.text {
  /* color: #fff; */
  font-size: 6rem;
  font-weight: 900;
  display: inline-block;
  position: absolute;
  bottom: 0;
  -webkit-animation: text 1050ms ease-in infinite;
  animation: text 1050ms ease-in infinite;
  transform: translatez(0);
}
.text-w {
  left: 0rem;
  transform: translate3d(0, -4rem, 0);
  -webkit-animation: text-w 1050ms ease-in infinite;
  animation: text-w 1050ms ease-in infinite;
}
.text-a {
  left: 5.4rem;
  -webkit-animation-delay: 150ms;
  animation-delay: 150ms;
}
.text-v {
  left: 9.6rem;
  -webkit-animation-delay: 230ms;
  animation-delay: 230ms;
}
.text-e {
  left: 13rem;
  -webkit-animation-delay: 310ms;
  animation-delay: 310ms;
}

.coast {
  position: absolute;
  left: 1.3rem;
  bottom: 1.7rem;
  width: 6.2rem;
  height: 2.2rem;
  display: inline-block;
  -webkit-animation: coast 2100ms linear infinite;
  animation: coast 2100ms linear infinite;
  transform: translateZ(0);
}

.wave-rel-wrap {
  position: relative;
  width: 100%;
  height: 100%;
  perspective: 3rem;
  perspective-origin: 0%, 50%;
}

.wave {
  position: absolute;
  width: 6.2rem;
  height: 2.2rem;
  border-radius: 1.1rem;
  background: radial-gradient(ellipse at center, #74f1fc 0%, #32e6ff 73%, #15c7fa 100%);
  display: inline-block;
  -webkit-animation: wave 2100ms linear infinite;
  animation: wave 2100ms linear infinite;
  will-change: width;
  transform: translateZ(0) scale(0);
}

.delay {
  -webkit-animation-delay: 1050ms;
  animation-delay: 1050ms;
}

@-webkit-keyframes text {
  0% {
    transform: translate3d(0, 0, 0);
  }
  30% {
    transform: translate3d(0, 0, 0);
  }
  45% {
    transform: translate3d(0, -4rem, 0);
  }
  100% {
    transform: translate3d(0, 0, 0);
  }
}

@keyframes text {
  0% {
    transform: translate3d(0, 0, 0);
  }
  30% {
    transform: translate3d(0, 0, 0);
  }
  45% {
    transform: translate3d(0, -4rem, 0);
  }
  100% {
    transform: translate3d(0, 0, 0);
  }
}
@-webkit-keyframes text-w {
  0% {
    transform: translate3d(0, -4rem, 0);
  }
  38% {
    transform: translate3d(0, -4rem, 0);
  }
  69% {
    transform: translate3d(0, 0, 0);
  }
  100% {
    transform: translate3d(0, -4rem, 0);
  }
}
@keyframes text-w {
  0% {
    transform: translate3d(0, -4rem, 0);
  }
  38% {
    transform: translate3d(0, -4rem, 0);
  }
  69% {
    transform: translate3d(0, 0, 0);
  }
  100% {
    transform: translate3d(0, -4rem, 0);
  }
}
@-webkit-keyframes coast {
  0% {
    transform: translate3d(0, 0, 0);
  }
  23% {
    transform: translate3d(0, 0, 0);
  }
  50% {
    transform: translate3d(16rem, 0, 0);
  }
  100% {
    transform: translate3d(16rem, 0, 0);
  }
}
@keyframes coast {
  0% {
    transform: translate3d(0, 0, 0);
  }
  23% {
    transform: translate3d(0, 0, 0);
  }
  50% {
    transform: translate3d(16rem, 0, 0);
  }
  100% {
    transform: translate3d(16rem, 0, 0);
  }
}
@-webkit-keyframes wave {
  0% {
    transform: scale(0);
    width: 2.2rem;
  }
  10% {
    transform: scale(1);
  }
  23% {
    width: 2.2rem;
  }
  32% {
    width: 6.1rem;
  }
  42% {
    width: 5rem;
    transform: rotateY(0deg) scale(1, 1);
  }
  51% {
    transform: rotateY(90deg) scale(0.6, 0.2);
  }
  52% {
    transform: rotateY(90deg) scale(0);
  }
  100% {
    transform: rotateY(90deg) scale(0);
  }
}
@keyframes wave {
  0% {
    transform: scale(0);
    width: 2.2rem;
  }
  10% {
    transform: scale(1);
  }
  23% {
    width: 2.2rem;
  }
  32% {
    width: 6.1rem;
  }
  42% {
    width: 5rem;
    transform: rotateY(0deg) scale(1, 1);
  }
  51% {
    transform: rotateY(90deg) scale(0.6, 0.2);
  }
  52% {
    transform: rotateY(90deg) scale(0);
  }
  100% {
    transform: rotateY(90deg) scale(0);
  }
}
</style>
