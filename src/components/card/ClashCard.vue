<template>
  <div class="slide-container">
    <div class="wrapper">
      <div class="clash-card barbarian">
        <div class="clash-card__image clash-card__image--barbarian">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/barbarian.png"
            alt="barbarian"
          />
        </div>
        <div class="clash-card__level clash-card__level--barbarian">
          Level 4
        </div>
        <div class="clash-card__unit-name">The Barbarian</div>
        <div class="clash-card__unit-description">
          The Barbarian is a kilt-clad Scottish warrior with an angry,
          battle-ready expression, hungry for destruction. He has Killer yellow
          horseshoe mustache.
        </div>

        <div
          class="clash-card__unit-stats clash-card__unit-stats--barbarian clearfix"
        >
          <div class="one-third">
            <div class="stat">20<sup>S</sup></div>
            <div class="stat-value">Training</div>
          </div>

          <div class="one-third">
            <div class="stat">16</div>
            <div class="stat-value">Speed</div>
          </div>

          <div class="one-third no-border">
            <div class="stat">150</div>
            <div class="stat-value">Cost</div>
          </div>
        </div>
      </div>
      <!-- end clash-card barbarian-->
    </div>
    <!-- end wrapper -->

    <div class="wrapper">
      <div class="clash-card archer">
        <div class="clash-card__image clash-card__image--archer">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/archer.png"
            alt="archer"
          />
        </div>
        <div class="clash-card__level clash-card__level--archer">Level 5</div>
        <div class="clash-card__unit-name">The Archer</div>
        <div class="clash-card__unit-description">
          The Archer is a female warrior with sharp eyes. She wears a short,
          light green dress, a hooded cape, a leather belt and an attached small
          pouch.
        </div>

        <div
          class="clash-card__unit-stats clash-card__unit-stats--archer clearfix"
        >
          <div class="one-third">
            <div class="stat">25<sup>S</sup></div>
            <div class="stat-value">Training</div>
          </div>

          <div class="one-third">
            <div class="stat">24</div>
            <div class="stat-value">Speed</div>
          </div>

          <div class="one-third no-border">
            <div class="stat">300</div>
            <div class="stat-value">Cost</div>
          </div>
        </div>
      </div>
      <!-- end clash-card archer-->
    </div>
    <!-- end wrapper -->

    <div class="wrapper">
      <div class="clash-card giant">
        <div class="clash-card__image clash-card__image--giant">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/giant.png"
            alt="giant"
          />
        </div>
        <div class="clash-card__level clash-card__level--giant">Level 5</div>
        <div class="clash-card__unit-name">The Giant</div>
        <div class="clash-card__unit-description">
          Slow, steady and powerful, Giants are massive warriors that soak up
          huge amounts of damage. Show them a turret or cannon and you'll see
          their fury unleashed!
        </div>

        <div
          class="clash-card__unit-stats clash-card__unit-stats--giant clearfix"
        >
          <div class="one-third">
            <div class="stat">2<sup>M</sup></div>
            <div class="stat-value">Training</div>
          </div>

          <div class="one-third">
            <div class="stat">12</div>
            <div class="stat-value">Speed</div>
          </div>

          <div class="one-third no-border">
            <div class="stat">2250</div>
            <div class="stat-value">Cost</div>
          </div>
        </div>
      </div>
      <!-- end clash-card giant-->
    </div>
    <!-- end wrapper -->

    <div class="wrapper">
      <div class="clash-card goblin">
        <div class="clash-card__image clash-card__image--goblin">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/goblin.png"
            alt="goblin"
          />
        </div>
        <div class="clash-card__level clash-card__level--goblin">Level 5</div>
        <div class="clash-card__unit-name">The Goblin</div>
        <div class="clash-card__unit-description">
          These pesky little creatures only have eyes for one thing: LOOT! They
          are faster than a Spring Trap, and their hunger for resources is
          limitless.
        </div>

        <div
          class="clash-card__unit-stats clash-card__unit-stats--goblin clearfix"
        >
          <div class="one-third">
            <div class="stat">30<sup>S</sup></div>
            <div class="stat-value">Training</div>
          </div>

          <div class="one-third">
            <div class="stat">32</div>
            <div class="stat-value">Speed</div>
          </div>

          <div class="one-third no-border">
            <div class="stat">100</div>
            <div class="stat-value">Cost</div>
          </div>
        </div>
      </div>
      <!-- end clash-card goblin-->
    </div>
    <!-- end wrapper -->

    <div class="wrapper">
      <div class="clash-card wizard">
        <div class="clash-card__image clash-card__image--wizard">
          <img
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/wizard.png"
            alt="wizard"
          />
        </div>
        <div class="clash-card__level clash-card__level--wizard">Level 6</div>
        <div class="clash-card__unit-name">The Wizard</div>
        <div class="clash-card__unit-description">
          The Wizard is a terrifying presence on the battlefield. Pair him up
          with some of his fellows and cast concentrated blasts of destruction
          on anything, land or sky!
        </div>

        <div
          class="clash-card__unit-stats clash-card__unit-stats--wizard clearfix"
        >
          <div class="one-third">
            <div class="stat">5<sup>M</sup></div>
            <div class="stat-value">Training</div>
          </div>

          <div class="one-third">
            <div class="stat">16</div>
            <div class="stat-value">Speed</div>
          </div>

          <div class="one-third no-border">
            <div class="stat">4000</div>
            <div class="stat-value">Cost</div>
          </div>
        </div>
      </div>
      <!-- end clash-card wizard-->
    </div>
    <!-- end wrapper -->
  </div>
  <!-- end container -->
</template>

<script>
export default {
  name: "ClashCard",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {}
};
</script>

<style scoped>
@import url(https://fonts.googleapis.com/css?family=Lato:400, 700, 900);
*,
*:before,
*:after {
  box-sizing: border-box;
}

body {
  background: linear-gradient(to bottom, #8c7a7a 0%, #af877c 65%, #af877c 100%)
    fixed;
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/coc-background.jpg")
    no-repeat center center fixed;
  background-size: cover;
  font: 14px/20px "Lato", Arial, sans-serif;
  color: #9e9e9e;
  margin-top: 30px;
}

.slide-container {
  margin: auto;
  width: 600px;
  text-align: center;
}

.wrapper {
  padding-top: 40px;
  padding-bottom: 40px;
}
.wrapper:focus {
  outline: 0;
}

.clash-card {
  background: white;
  width: 300px;
  display: inline-block;
  margin: auto;
  border-radius: 19px;
  position: relative;
  text-align: center;
  box-shadow: -1px 15px 30px -12px black;
  z-index: 9999;
}

.clash-card__image {
  position: relative;
  height: 230px;
  margin-bottom: 35px;
  border-top-left-radius: 14px;
  border-top-right-radius: 14px;
}

.clash-card__image--barbarian {
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/barbarian-bg.jpg");
}
.clash-card__image--barbarian img {
  width: 400px;
  position: absolute;
  top: -65px;
  left: -70px;
}

.clash-card__image--archer {
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/archer-bg.jpg");
}
.clash-card__image--archer img {
  width: 400px;
  position: absolute;
  top: -34px;
  left: -37px;
}

.clash-card__image--giant {
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/giant-bg.jpg");
}
.clash-card__image--giant img {
  width: 340px;
  position: absolute;
  top: -30px;
  left: -25px;
}

.clash-card__image--goblin {
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/goblin-bg.jpg");
}
.clash-card__image--goblin img {
  width: 370px;
  position: absolute;
  top: -21px;
  left: -37px;
}

.clash-card__image--wizard {
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/wizard-bg.jpg");
}
.clash-card__image--wizard img {
  width: 345px;
  position: absolute;
  top: -28px;
  left: -10px;
}

.clash-card__level {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 700;
  margin-bottom: 3px;
}

.clash-card__level--barbarian {
  color: #ec9b3b;
}

.clash-card__level--archer {
  color: #ee5487;
}

.clash-card__level--giant {
  color: #f6901a;
}

.clash-card__level--goblin {
  color: #82bb30;
}

.clash-card__level--wizard {
  color: #4facff;
}

.clash-card__unit-name {
  font-size: 26px;
  color: black;
  font-weight: 900;
  margin-bottom: 5px;
}

.clash-card__unit-description {
  padding: 20px;
  margin-bottom: 10px;
}

.clash-card__unit-stats--barbarian {
  background: #ec9b3b;
}
.clash-card__unit-stats--barbarian .one-third {
  border-right: 1px solid #bd7c2f;
}

.clash-card__unit-stats--archer {
  background: #ee5487;
}
.clash-card__unit-stats--archer .one-third {
  border-right: 1px solid #d04976;
}

.clash-card__unit-stats--giant {
  background: #f6901a;
}
.clash-card__unit-stats--giant .one-third {
  border-right: 1px solid #de7b09;
}

.clash-card__unit-stats--goblin {
  background: #82bb30;
}
.clash-card__unit-stats--goblin .one-third {
  border-right: 1px solid #71a32a;
}

.clash-card__unit-stats--wizard {
  background: #4facff;
}
.clash-card__unit-stats--wizard .one-third {
  border-right: 1px solid #309eff;
}

.clash-card__unit-stats {
  color: white;
  font-weight: 700;
  border-bottom-left-radius: 14px;
  border-bottom-right-radius: 14px;
}
.clash-card__unit-stats .one-third {
  width: 33%;
  float: left;
  padding: 20px 15px;
}
.clash-card__unit-stats sup {
  position: absolute;
  bottom: 4px;
  font-size: 45%;
  margin-left: 2px;
}
.clash-card__unit-stats .stat {
  position: relative;
  font-size: 24px;
  margin-bottom: 10px;
}
.clash-card__unit-stats .stat-value {
  text-transform: uppercase;
  font-weight: 400;
  font-size: 12px;
}
.clash-card__unit-stats .no-border {
  border-right: none;
}

.clearfix:after {
  visibility: hidden;
  display: block;
  font-size: 0;
  content: " ";
  clear: both;
  height: 0;
}

.slick-prev {
  left: 100px;
  z-index: 999;
}

.slick-next {
  right: 100px;
  z-index: 999;
}
</style>
