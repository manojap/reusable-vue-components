<template>
 
    <nav class="menu-wrapper">
      <button
        v-if="hasMenuClicked === false"
        @click="(hasMenuClicked = true), (hasCloseClicked = false)"
        :class="['menu-btn', { clicked: hasMenuClicked }]"
      >
        <i></i>
        <i></i>
        <i></i>
        <span class="ripple"></span>
      </button>
      <button
        v-if="hasMenuClicked === true"
        @click="(hasMenuClicked = false), (hasCloseClicked = true)"
        :class="['menu-btn', { 'clicked': hasMenuClicked }]"
      >
        <i></i>
        <i></i>
        <i></i>
        <span class="ripple"></span>
      </button>

     
      <ul :class="['menu', { 'open': hasMenuClicked }]">
        
        <li class="menuitem-wrapper" >
        
          <div :class="['menuitem-wrapper',{'spin':hasMIClicked}]" @click="hasMIClicked=true">
          <slot name="icon1">
            <a href="#" class="menu-item">
              <oh-s-icon class="mt-1" name="oi-octoface" scale="1.5" />
            </a>
          </slot>
          </div>
          <svg class="circle-holder">
            <circle r="88" cx="80%" cy="50%" fill="none"></circle>
          </svg>
        </li>

        <li :class="['menuitem-wrapper',{'spin':hasMIClicked}]" @click="hasMIClicked=true">
          <div class="icon-holder">
          <slot name="icon2">
            <a href="#" class="menu-item">
              <oh-s-icon class="mt-1" name="bi-twitter" scale="1.5" />
            </a>
            </slot>
          </div>
          <svg class="circle-holder">
            <circle r="88" cx="50%" cy="50%" fill="none"></circle>
          </svg>
        </li>
        <li :class="['menuitem-wrapper',{'spin':hasMIClicked}]" @click="hasMIClicked=true">
          <div class="icon-holder">
            <slot name="icon3">
            <a href="#" class="menu-item">
               <oh-s-icon class="mt-1" name="fa-wordpress" scale="1.5" />
            </a>
            </slot>
          </div>
          <svg class="circle-holder">
            <circle r="88" cx="50%" cy="50%" fill="none"></circle>
          </svg>
        </li>
        <li :class="['menuitem-wrapper',{'spin':hasMIClicked}]" @click="hasMIClicked=true">
          <div class="icon-holder">
          <slot name="icon4">
            <a href="#" class="menu-item">
             <oh-s-icon class="mt-1" name="fa-home" scale="1.5" />
            </a>
            </slot>
          </div>
          <svg class="circle-holder">
            <circle r="88" cx="50%" cy="50%" fill="grey"></circle>
          </svg>
        </li>
        <li :class="['menuitem-wrapper',{'spin':hasMIClicked}]" @click="hasMIClicked=true">
          <div class="icon-holder">
           <slot name="icon5">
            <a href="#" class="menu-item">
              <oh-s-icon class="mt-1" name="fa-flag" scale="1.5" />
            </a>
            </slot>
          </div>
          <svg class="circle-holder">
            <circle r="88" cx="50%" cy="50%" fill="none"></circle>
          </svg>
        </li>
      </ul>
    </nav>
  
</template>

<script>
export default {
  name: "CMenu",
  created() {},
  data() {
    return {
      hasMenuClicked: false,
      hasCloseClicked: false,
      hasMIClicked:false
    };
  },
  watch: {
    hasMenuClicked(){
      // if(this.hasMenuClicked){ }else{this.hasMIClicked=true; }
     this.hasMIClicked=false;
      // this.hasMenuClicked=false;
      this.hasCloseClicked= false ;
    
    },
     hasMIClicked(){
       setTimeout(() => {
         this.hasMenuClicked=false;

       }, 800);
    //       // this.hasMIClicked=false; 
    //   this.hasMenuClicked=false;
    //   // this.hasCloseClicked= false ;
    }
  },
  props: {},
  methods: {
    mi_click(){
     this.hasMIClicked=true; 
    //  setInterval(() => {
    //    this.hasMenuClicked=false;  this.hasCloseClicked=false;
    //  }, 900);
      //  
      // 
    
    }
  },
};
</script>

<style lang="css" scoped>
*,
*:before,
*:after {
  box-sizing: inherit;
}

a {
  color: white;
  text-decoration: none;
}

.menu-wrapper {
  position: absolute;
  top: 50%;
  left: 50%;
  display: block;
  width: 30rem;
  height: 30rem;
  margin-top: -15rem;
  margin-left: -15rem;
}

.menu {
  width: 100%;
  height: 100%;
  transform: scale(0);
  transform-origin: center;
  transition: all 0.08s ease-in-out;
}
.menu li {
  position: absolute;
  top: 50%;
  left: 50%;
  display: inline-block;
  width: 4rem;
  height: 80%;
  margin-top: -12rem;
  margin-left: -2rem;
  text-align: center;
}
.menu li.spin {
  z-index: 1;
}
.menu li.spin .icon-holder {
  -webkit-animation: spin 0.7s linear forwards;
  animation: spin 0.7s linear forwards;
}
.menu li.spin .circle-holder {
  display: block;
}
.menu li.spin .circle-holder circle {
  -webkit-animation: dash 0.7s linear forwards;
  animation: dash 0.7s linear forwards;
}
.menu a {
  position: relative;
  display: inline-block;
  width: 4rem;
  height: 4rem;
  margin-top: 4.5rem;
  padding: 1rem;
  border-radius: 100%;
  transform: scale(1, 1);
}
.menu a i {
  display: inline-block;
  vertical-align: middle;
  line-height: 1.2;
}
.menu.open {
  transform: scale(1);
}

.icon-holder {
  position: relative;
  z-index: 1;
  display: inline-block;
  width: 4rem;
  height: 100%;
}

.circle-holder {
  position: absolute;
  top: 50%;
  left: 50%;
  z-index: 0;
  display: none;
  width: 24rem;
  height: 24rem;
  margin: -12rem;
  padding: 1rem;
  transform: rotate(-90deg);
}
.circle-holder circle {
  width: 100%;
  height: 100%;
  stroke-width: 14rem;
  stroke-dasharray: 560;
  stroke-dashoffset: 560;
  stroke-linecap: round;
}

.menu-btn {
  position: absolute;
  top: 50%;
  left: 50%;
  z-index: 10;
  display: block;
  width: 4rem;
  height: 4rem;
  margin: -2rem;
  padding: 1.3rem;
  background: white;
  border: none;
  box-shadow: none;
  border-radius: 100%;
  text-align: center;
  line-height: 1;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  outline: none;
  cursor: pointer;
  font-size: 0;
}
.menu-btn i {
  position: relative;
  z-index: 11;
  display: inline-block;
  vertical-align: middle;
  width: 100%;
  height: 0.1rem;
  margin: 0 auto;
  background: #2c3e50;
}
.menu-btn i:nth-child(2) {
  margin: 0.34rem auto;
}

.clicked.menu-btn {
  -webkit-animation: buttonactive ease-in 0.2s forwards 1;
  animation: buttonactive ease-in 0.2s forwards 1;
}
.clicked.menu-btn i:first-child {
  -webkit-animation: top-down ease-in 0.2s forwards 1;
  animation: top-down ease-in 0.2s forwards 1;
}
.clicked.menu-btn i:nth-child(2) {
  -webkit-animation: middle ease-in 0.01s forwards 1;
  animation: middle ease-in 0.01s forwards 1;
}
.clicked.menu-btn i:nth-child(3) {
  -webkit-animation: down-top ease-in 0.2s forwards 1;
  animation: down-top ease-in 0.2s forwards 1;
}
.clicked .ripple {
  -webkit-animation: ripples ease-in 0.35s forwards 1;
  animation: ripples ease-in 0.35s forwards 1;
}

.ripple {
  position: absolute;
  top: -1rem;
  left: -1rem;
  z-index: 10;
  display: block;
  width: 6rem;
  height: 6rem;
  transform: scale(0.5);
  opacity: 0;
  border: 2rem solid white;
  border-radius: 100%;
}

.menu li:nth-child(1) {
  transform: rotate(0deg);
}
.menu li:nth-child(1) a {
  transform: rotate(-0deg);
  background: #2980b9;
}
.menu li:nth-child(1) circle {
  stroke: #2980b9;
}

.bg-0 {
  background: #2980b9;
}

.menu li:nth-child(2) {
  transform: rotate(71.5deg);
}
.menu li:nth-child(2) a {
  transform: rotate(-71.5deg);
  background: #c0392b;
}
.menu li:nth-child(2) circle {
  stroke: #c0392b;
}

.bg-1 {
  background: #c0392b;
}

.menu li:nth-child(3) {
  transform: rotate(143deg);
}
.menu li:nth-child(3) a {
  transform: rotate(-143deg);
  background: #1abc9c;
}
.menu li:nth-child(3) circle {
  stroke: #1abc9c;
}

.bg-2 {
  background: #1abc9c;
}

.menu li:nth-child(4) {
  transform: rotate(214.5deg);
}
.menu li:nth-child(4) a {
  transform: rotate(-214.5deg);
  background: #f39c12;
}
.menu li:nth-child(4) circle {
  stroke: #f39c12;
}

.bg-3 {
  background: #f39c12;
}

.menu li:nth-child(5) {
  transform: rotate(286deg);
}
.menu li:nth-child(5) a {
  transform: rotate(-286deg);
  background: #8e44ad;
}
.menu li:nth-child(5) circle {
  stroke: #8e44ad;
}

.bg-4 {
  background: #8e44ad;
}

@-webkit-keyframes spin {
  0% {
    transform: rotate(0deg);
    opacity: 1;
  }
  80% {
    transform: rotate(360deg);
    opacity: 1;
  }
  100% {
    transform: rotate(360deg);
    opacity: 0;
  }
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
    opacity: 1;
  }
  80% {
    transform: rotate(360deg);
    opacity: 1;
  }
  100% {
    transform: rotate(360deg);
    opacity: 1;
  }
}
@-webkit-keyframes dash {
  0% {
    stroke-dashoffset: 560;
    stroke-width: 4rem;
  }
  80% {
    stroke-dashoffset: 0;
    stroke-width: 4rem;
    opacity: 1;
  }
  100% {
    stroke-dashoffset: 0;
    stroke-width: 6rem;
    opacity: 0;
  }
}
@keyframes dash {
  0% {
    stroke-dashoffset: 560;
    stroke-width: 4rem;
  }
  80% {
    stroke-dashoffset: 0;
    stroke-width: 4rem;
    opacity: 1;
  }
  100% {
    stroke-dashoffset: 0;
    stroke-width: 6rem;
    opacity: 0;
  }
}
@-webkit-keyframes buttonactive {
  0% {
    background: white;
    transform: rotate(0deg);
  }
  100% {
    background: #4f6f8f;
    transform: rotate(-90deg);
  }
}
@keyframes buttonactive {
  0% {
    background: white;
    transform: rotate(0deg);
  }
  100% {
    background: #4f6f8f;
    transform: rotate(-90deg);
  }
}
@-webkit-keyframes middle {
  0% {
    opacity: 1;
    left: 0;
  }
  100% {
    opacity: 0;
    left: -4rem;
  }
}
@keyframes middle {
  0% {
    opacity: 1;
    left: 0;
  }
  100% {
    opacity: 0;
    left: -4rem;
  }
}
@-webkit-keyframes top-down {
  0% {
    top: 0;
    transform: rotate(0);
  }
  100% {
    top: 0.35rem;
    transform: rotate(-45deg);
  }
}
@keyframes top-down {
  0% {
    top: 0;
    transform: rotate(0);
  }
  100% {
    top: 0.35rem;
    transform: rotate(-45deg);
  }
}
@-webkit-keyframes down-top {
  0% {
    top: 0;
    transform: rotate(0);
  }
  100% {
    top: -0.4rem;
    transform: rotate(45deg);
  }
}
@keyframes down-top {
  0% {
    top: 0;
    transform: rotate(0);
  }
  100% {
    top: -0.4rem;
    transform: rotate(45deg);
  }
}
@-webkit-keyframes ripples {
  0% {
    opacity: 1;
    transform: scale(0.5);
    border-width: 3rem;
  }
  100% {
    opacity: 0.5;
    transform: scale(1);
    border-width: 0rem;
  }
}
@keyframes ripples {
  0% {
    opacity: 1;
    transform: scale(0.5);
    border-width: 3rem;
  }
  100% {
    opacity: 0.5;
    transform: scale(1);
    border-width: 0rem;
  }
}
@-webkit-keyframes bouncein {
  to {
    transform: scale(1);
  }
}
@keyframes bouncein {
  to {
    transform: scale(1);
  }
}
</style>
