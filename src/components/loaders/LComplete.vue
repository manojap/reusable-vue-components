<template>
<div>
   
 <div class="['circle-loader',{'load-complete':isCompleted}]">
  <div :class="[{checkmark:!isCompleted}, draw]"></div>
</div>

<p><button id="toggle" @click="isCompleted=!isCompleted" type="button" class="btn btn-success">Toggle Completed</button></p>
<!-- partial -->
</div>
</template>

<script>
export default {
  name: "CLoader",
  created() {},
  data() {
    return {
    };
  },
  props: {
    isCompleted:{
      trype:Boolean,
      default:false
    }
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
 body {
  padding: 5em;
  text-align: center;
}

h1 {
  margin-bottom: 1em;
}

.circle-loader {
  margin-bottom: 3.5em;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-left-color: #5cb85c;
  animation: loader-spin 1.2s infinite linear;
  position: relative;
  display: inline-block;
  vertical-align: top;
  border-radius: 50%;
  width: 7em;
  height: 7em;
}

.load-complete {
  -webkit-animation: none;
  animation: none;
  border-color: #5cb85c;
  transition: border 500ms ease-out;
}

.checkmark {
  display: none;
}
.checkmark.draw:after {
  animation-duration: 800ms;
  animation-timing-function: ease;
  animation-name: checkmark;
  transform: scaleX(-1) rotate(135deg);
}
.checkmark:after {
  opacity: 1;
  height: 3.5em;
  width: 1.75em;
  transform-origin: left top;
  border-right: 3px solid #5cb85c;
  border-top: 3px solid #5cb85c;
  content: "";
  left: 1.75em;
  top: 3.5em;
  position: absolute;
}

@keyframes loader-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes checkmark {
  0% {
    height: 0;
    width: 0;
    opacity: 1;
  }
  20% {
    height: 0;
    width: 1.75em;
    opacity: 1;
  }
  40% {
    height: 3.5em;
    width: 1.75em;
    opacity: 1;
  }
  100% {
    height: 3.5em;
    width: 1.75em;
    opacity: 1;
  }
}
</style>