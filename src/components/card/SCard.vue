<template>
  <div class="container">
    <img
      src="https://s5.postimg.cc/n8uucy6qv/strawberryx300n.png"
      alt="Strawberry"
      class="img-fruit"
    />
    <h3>Strawberries</h3>
    <div class="control-btn">
      <span class="prev">
        <i class="fa fa-long-arrow-left"></i>
      </span>
      <span class="next">
        <i class="fa fa-long-arrow-right"></i>
      </span>
    </div>
    <p>
      The garden strawberry is a widely grown hybrid species of the genus
      Fragaria. It is cultivated worldwide for its fruit.
    </p>
    <div class="properties">
      <div class="qty">
        <h4>Quantity</h4>
        <i class="fa fa-minus"></i>
        <span class="number">1</span>
        <i class="fa fa-plus"></i>
      </div>
      <div class="price">
        <h4>Total Price</h4>
        <span class="price-inr">
          <i class="fa fa-inr"></i>
          <span class="amount">7</span>
        </span>
      </div>
      <div class="delivery">
        <h4>Delivery</h4>
        <i class="fa fa-fighter-jet"></i>
        <span class="time">In 60 mins</span>
      </div>
    </div>
    <input class="ip-add-cart" type="button" value="Add to cart" />
  </div>
</template>

<script>
export default {
  name: "Test",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {}
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  outline: none;
}

html {
  height: 100%;
}

body {
  background: #ccc;
  font-family: "Libre Franklin", sans-serif;
  background-repeat: no-repeat;
  background-color: #d2eaea;
  *zoom: 1;
  filter: progid:DXImageTransform.Microsoft.gradient(gradientType=1, startColorstr='#FFD2EAEA', endColorstr='#FFF7EEC3');
  background-image: url("data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4gPHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJncmFkIiBncmFkaWVudFVuaXRzPSJvYmplY3RCb3VuZGluZ0JveCIgeDE9IjAuMCIgeTE9IjEuMCIgeDI9IjEuMCIgeTI9IjAuMCI+PHN0b3Agb2Zmc2V0PSIwJSIgc3RvcC1jb2xvcj0iI2QyZWFlYSIvPjxzdG9wIG9mZnNldD0iNDklIiBzdG9wLWNvbG9yPSIjZjlmOWY5Ii8+PHN0b3Agb2Zmc2V0PSI0OSUiIHN0b3AtY29sb3I9IiNmOWY5ZjkiLz48c3RvcCBvZmZzZXQ9IjEwMCUiIHN0b3AtY29sb3I9IiNmN2VlYzMiLz48L2xpbmVhckdyYWRpZW50PjwvZGVmcz48cmVjdCB4PSIwIiB5PSIwIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSJ1cmwoI2dyYWQpIiAvPjwvc3ZnPiA=");
  background-size: 100%;
  background-image: -webkit-gradient(
    linear,
    0% 100%,
    100% 0%,
    color-stop(0%, #d2eaea),
    color-stop(49%, #f9f9f9),
    color-stop(49%, #f9f9f9),
    color-stop(100%, #f7eec3)
  );
  background-image: -moz-linear-gradient(
    left bottom,
    #d2eaea 0%,
    #f9f9f9 49%,
    #f9f9f9 49%,
    #f7eec3 100%
  );
  background-image: -webkit-linear-gradient(
    left bottom,
    #d2eaea 0%,
    #f9f9f9 49%,
    #f9f9f9 49%,
    #f7eec3 100%
  );
  background-image: linear-gradient(
    to right top,
    #d2eaea 0%,
    #f9f9f9 49%,
    #f9f9f9 49%,
    #f7eec3 100%
  );
}

div.container {
  position: relative;
  margin: 70px auto;
  width: 350px;
  height: 470px;
  text-align: center;
  background: #fff;
  -moz-box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.1),
    0px 60px 75px -25px rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.1),
    0px 60px 75px -25px rgba(0, 0, 0, 0.2);
  box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.1),
    0px 60px 75px -25px rgba(0, 0, 0, 0.2);
  cursor: default;
}
div.container img.img-fruit {
  width: 290px;
  margin-top: -60px;
}
div.container div.control-btn span {
  position: absolute;
  margin-top: 20px;
  width: 35px;
  height: 35px;
  background: #f22d34;
  color: #fff;
  font-size: 13px;
  display: inline-block;
  line-height: 36px;
  cursor: pointer;
  -moz-border-radius: 100%;
  -webkit-border-radius: 100%;
  border-radius: 100%;
  -moz-box-shadow: 0px 2px 7px rgba(241, 44, 51, 0.7);
  -webkit-box-shadow: 0px 2px 7px rgba(241, 44, 51, 0.7);
  box-shadow: 0px 2px 7px rgba(241, 44, 51, 0.7);
  -moz-transition: background 0.3s ease-in;
  -o-transition: background 0.3s ease-in;
  -webkit-transition: background 0.3s ease-in;
  transition: background 0.3s ease-in;
}
div.container div.control-btn span:hover {
  background: #de2128;
}
div.container span.prev {
  left: -17.5px;
}
div.container span.next {
  right: -17.5px;
}
div.container h3 {
  font-size: 30px;
  letter-spacing: 3px;
  margin-top: 35px;
  color: #ea1d24;
}
div.container p {
  font-size: 11px;
  padding: 15px 45px;
  color: #878787;
  line-height: 22px;
}
div.container div.properties {
  margin-top: 20px;
  height: 130px;
}
div.container div.properties:before,
div.container div.properties:after {
  content: " ";
  display: inline-block;
}
div.container div.properties:after {
  clear: both;
}
div.container div.properties div {
  display: inline-block;
  text-align: center;
  width: 33.33%;
  float: left;
}
div.container div.properties div h4 {
  font-size: 14px;
  color: #757575;
  padding: 25px 0px;
}
div.container div.properties .qty .fa {
  font-size: 7px;
  color: #757575;
  background: #dfdfdf;
  -moz-border-radius: 100%;
  -webkit-border-radius: 100%;
  border-radius: 100%;
  padding: 4px;
  cursor: pointer;
}
div.container div.properties .qty .number {
  font-size: 11px;
  color: #757575;
  padding: 5px;
}
div.container div.properties .price .fa {
  font-size: 18px;
  color: #757575;
}
div.container div.properties .price .amount {
  color: #646363;
  font-size: 18px;
  padding: 0 5px;
}
div.container div.properties .delivery .fa {
  font-size: 15px;
  color: #757575;
}
div.container div.properties .delivery .time {
  display: inline-block;
  color: #757575;
  font-size: 11px;
}
div.container .ip-add-cart {
  border: none;
  padding: 12px 50px;
  background: #f22d34;
  color: #fff;
  font-size: 12px;
  text-transform: uppercase;
  font-weight: bold;
  -moz-border-radius: 25px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
  -moz-box-shadow: 0px 15px 45px rgba(242, 45, 52, 0.5);
  -webkit-box-shadow: 0px 15px 45px rgba(242, 45, 52, 0.5);
  box-shadow: 0px 15px 45px rgba(242, 45, 52, 0.5);
  cursor: pointer;
  -moz-transition: background 0.3s ease-in;
  -o-transition: background 0.3s ease-in;
  -webkit-transition: background 0.3s ease-in;
  transition: background 0.3s ease-in;
}
div.container .ip-add-cart:hover {
  background: #da1920;
}

/* Start Credit Style */
div.credit {
  position: absolute;
  padding: 0px 10px;
  padding-bottom: 8px;
  height: 15px;
  right: 10px;
  top: 10px;
  display: inline-block;
  background: rgba(255, 255, 255, 0.7);
  font-size: 7px;
  font-weight: bold;
  color: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-shadow: 0px 10px 15px -15px rgba(0, 0, 0, 0.3);
  cursor: default;
}
div.credit:hover {
  border: 1px solid rgba(0, 0, 0, 0.2);
}
div.credit img {
  position: relative;
  width: 14px;
  margin-left: 3px;
  top: 4px;
}

/* End Credit Style */
</style>
