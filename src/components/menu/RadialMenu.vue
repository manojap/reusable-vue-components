<template>
  <div>
   <div class="base">
   <div class="menu">
      <div class="icon">
         <div class="bar"></div>
      </div>
   </div>
   <div class="icons">
      <i class="fa fa-user" aria-hidden="true"></i>
      <i class="fa fa-calendar-o" aria-hidden="true"></i>
      <i class="fa fa-tachometer" aria-hidden="true"></i>
   </div>
   <div class="section">
      <div class="cover1">
         <div class="cover2">
            <a class="content" href="#calender"></a>
         </div>
      </div>
   </div>
   <a class="section-static top" href="#profile"></a>
   <a class="section-static bottom" href="#dashboard"></a>
</div>
  </div>
</template>

<script>
export default {
  name: "RMenu",
  created() {},
  data() {
    return {
      isClicked: false,
      isClosed: false,

      isOpened: false,
    };
  },
  watch: {
    isClicked() {
      this.isClosed = true;
    },
  },
  props: {},
  mounted() {
     let externalScript = document.createElement('script')
    externalScript.setAttribute('src', 'https://codepen.io/z-/pen/a8e37caf2a04602ea5815e5acedab458.js')
    document.head.appendChild(externalScript)

 let externalScript1 = document.createElement('script')
    externalScript1.setAttribute('src', 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js')
    document.head.appendChild(externalScript1)

let externalScript11 = document.createElement('script')
    externalScript11.setAttribute('src', 'https://codepen.io/z-/pen/2677821722cd9e02c2c882a17c5b2072.js')
    document.head.appendChild(externalScript11)

 let externalScript12 = document.createElement('script')
    externalScript12.setAttribute('src', 'https://codepen.io/z-/pen/0a1bedbb8ca05b9afd329264fca7b921')
    document.head.appendChild(externalScript12)


    
  },
  methods: {
    clicked() {
      
      setTimeout(() => {
      this.isClicked=true;
      if (this.isOpened == true) {
        this.isOpened = false;
        this.isClosed = true;

      } else {
        this.isClosed = false;
        this.isOpened = true;

      }  
      }, 100);
      
    },
  },
};
</script>

<style lang="css" scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css");

body {
  background-color: #21264b;
  overflow-x: hidden;
}
body .base {
  z-index: 90;
  position: fixed;
  top: 0px;
  left: 0px;
  background-color: #ffffff;
  width: 98px;
  height: 98px;
  transition: all 1s cubic-bezier(0.5, -0.75, 0.05, 1);
  border-bottom-right-radius: 100%;
}
body .base .menu {
  z-index: 100;
  background-color: #ffffff;
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100px;
  height: 100px;
  border-bottom-right-radius: 200px;
  cursor: pointer;
  transition: all 1s cubic-bezier(0.5, -0.75, 0.05, 1), background-color 1s ease;
}
body .base .menu .icon {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 50%;
  left: 50%;
  transform: translate(-100%, -100%);
}
body .base .menu .icon:before,
body .base .menu .icon:after {
  content: "";
  transform: rotate(0deg);
  transition: top 0.5s ease 0.5s, transform 0.5s ease, background-color 0.75s ease 0.25s;
}
body .base .menu .icon .bar,
body .base .menu .icon:before,
body .base .menu .icon:after {
  position: absolute;
  height: 5px;
  left: 0px;
  right: 0px;
  border-radius: 5px;
  background-color: #21264b;
}
body .base .menu .icon .bar {
  transition: opacity 0s linear 0.5s, background-color 0.75s ease 0.25s;
  opacity: 1;
  top: 10px;
}
body .base .menu .icon:before {
  top: 0px;
}
body .base .menu .icon:after {
  top: initial;
  top: 20px;
}
body .base .icons {
  z-index: 98;
  position: absolute;
  top: 0px;
  left: 0px;
}
body .base .icons > * {
  position: absolute;
  font-size: 40px;
  color: #21264b;
  transition: 0.3s cubic-bezier(0.5, -0.25, 0.05, 1);
}
body .base .icons .fa-user {
  top: 35px;
  left: 0px;
  transition-delay: 0.2s;
}
body .base .icons .fa-calendar-o {
  top: 0px;
  left: 0px;
  color: #f1e99c;
  transition-delay: 0.1s;
}
body .base .icons .fa-tachometer {
  top: 0px;
  left: 35px;
}
body .base .section {
  z-index: 96;
  position: absolute;
  top: 0px;
  left: 0px;
  height: 0px;
  width: 0px;
  transform-origin: 100% 100%;
  transform: rotate(135deg);
}
body .base .section .cover1 {
  transform-origin: 100% 100%;
}
body .base .section .cover1,
body .base .section .cover1 .cover2,
body .base .section .cover1 .cover2 .content {
  position: absolute;
  width: 600px;
  height: 600px;
}
body .base .section .cover1,
body .base .section .cover1 .cover2 {
  top: 50%;
  left: 50%;
  transform: translate(-100%, -100%) rotate(4deg);
  overflow: hidden;
  pointer-events: none;
  transition: transform 0.5s ease-in;
}
body .base .section .cover1 .cover2 {
  transform: translate(50%, -50%) rotate(-8deg);
  transform-origin: 0% 100%;
}
body .base .section .cover1 .cover2 .content {
  width: 150px;
  height: 150px;
  border-radius: 100%;
  background-color: #ee1b59;
  top: 100%;
  left: 0%;
  transform: translate(-50%, -50%);
  transition: background-color 0s, width 1.5s cubic-bezier(0.5, -0.5, 0.05, 1) 0s,
    height 1.5s cubic-bezier(0.5, -0.5, 0.05, 1) 0s;
  pointer-events: auto;
}
body .base .section-static {
  z-index: 94;
  width: 100px;
  height: 100px;
  position: absolute;
  top: 0px;
  left: 0px;
  transform-origin: 0% 0%;
  transition: width 1s cubic-bezier(0.5, -0.75, 0.05, 1),
    height 1s cubic-bezier(0.5, -0.75, 0.05, 1);
}
body .base .section-static:hover {
  background-color: #eaeaea;
}
body .base .section-static.top {
  transform: rotate(-45deg);
  border-bottom-right-radius: 400px;
}
body .base .section-static.bottom {
  transform: rotate(45deg);
  border-bottom-right-radius: 400px;
}
body .base.close {
  width: 300px;
  height: 300px;
  transition: all 1.25s cubic-bezier(0.5, 0, 0.05, 1.75);
}
body .base.close .menu {
  width: 150px;
  height: 150px;
  transition: all 1s cubic-bezier(0.5, 0, 0.05, 1.75), background-color 1s ease;
  background-color: #21264b;
}
body .base.close .menu .icon .bar,
body .base.close .menu .icon:before,
body .base.close .menu .icon:after {
  background-color: #ffffff;
}
body .base.close .menu .icon .bar {
  opacity: 0;
}
body .base.close .menu .icon:before,
body .base.close .menu .icon:after {
  transition: top 0.5s linear, transform 0.5s ease 0.5s, background-color 0.75s ease 0.25s;
}
body .base.close .menu .icon:before {
  top: 10px;
  transform: rotate(-45deg);
}
body .base.close .menu .icon:after {
  top: 10px;
  transform: rotate(45deg);
}
body .base.close .icons {
  position: absolute;
  top: 0px;
  left: 0px;
}
body .base.close .icons > * {
  position: absolute;
  font-size: 40px;
  color: #21264b;
  transition: 0.3s cubic-bezier(0.5, 0, 0.05, 1.75) 0.7s;
  pointer-events: none;
}
body .base.close .icons .fa-user {
  top: 35px;
  left: 200px;
}
body .base.close .icons .fa-calendar-o {
  top: 141px;
  left: 141px;
  color: #fff;
  transition-delay: 0.65s;
}
body .base.close .icons .fa-tachometer {
  top: 200px;
  left: 35px;
  transition-delay: 0.8s;
}
body .base.close .section .cover1 {
  transform-origin: 100% 100%;
}
body .base.close .section .cover1,
body .base.close .section .cover1 .cover2,
body .base.close .section .cover1 .cover2 .content {
  position: absolute;
  width: 600px;
  height: 600px;
}
body .base.close .section .cover1,
body .base.close .section .cover1 .cover2 {
  top: 50%;
  left: 50%;
  transform: translate(-100%, -100%) rotate(16deg);
  overflow: hidden;
  transition: transform 0.5s ease-in 0.5s;
}
body .base.close .section .cover1 .cover2 {
  transform: translate(50%, -50%) rotate(-32deg);
  transform-origin: 0% 100%;
}
body .base.close .section .cover1 .cover2 .content {
  border-radius: 100%;
  background-color: #ee1b59;
  top: 100%;
  left: 0%;
  transform: translate(-50%, -50%);
  transition: background-color 0s, width 1.1s cubic-bezier(0.5, 0, 0.05, 1.75) 0.25s,
    height 1.1s cubic-bezier(0.5, 0, 0.05, 2) 0.25s;
}
body .base.close .section .cover1 .cover2 .content:hover {
  background-color: #dd1350;
}
body .base.close .section-static {
  width: 300px;
  height: 300px;
  transition: width 1.25s cubic-bezier(0.5, 0, 0.05, 2),
    height 1.25s cubic-bezier(0.5, 0, 0.05, 2);
}
</style>
