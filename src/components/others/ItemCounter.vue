<template>
  <div class="wrapper">
    <h3 class="has-text-centered">{{ caption }}</h3>
    <div class="number-wrap">
      <span class="digit"><span></span></span>
    </div>
    <div @click="qty++" class="button plus" style="margin-top: -50px" id="plus">
      <div style="margin-top: -6px; font-weight: bold">+</div>
    </div>
    <div
      @click="qty--"
      class="button minus disabled"
      style="margin-top: -50px"
      id="minus"
    >
      <div style="margin-top: -6px; font-weight: bold">-</div>
    </div>
    <p class="has-text-centered">
      {{ currency }}<span>{{ qty }}</span
      >.00
    </p>
  </div>
</template>

<script>
export default {
  name: "CCounter",
  created() {},
  watch: {
    qty() {
      if (this.qty < 0) this.qty = 0;
      this.$emit("qtyChanged", this.qty);
      
    },
  },
  data() {
    return {
      qty: 0,
    };
  },
  props: {
    currency: {
      type: String,
      default: "$",
    },
    caption: {
      type: String,
      default: "Quantity",
    },
  },
  computed: {
    
  },
  methods: {
 
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
  margin: 80px auto;
  width: 100%;
  max-width: 120px;
  border-radius: 5px;
  background: #fff;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 25px;
  position: relative;
}

.wrapper h3,
.wrapper p {
  font-family: "Neucha", cursive;
  padding: 10px;
  border-radius: 5px 0 0 5px;
  font-size: 18px;
  color: #333;
}

.wrapper p {
  color: #666;
  font-size: 16px;
}

.number-wrap {
  height: 50px;
  font-size: 48px;
  width: 100%;
  position: relative;
  overflow: hidden;
  text-align: center;
  display: inline-block;
  padding: 10px 0;
  background: #eaeaea;
}

.digit {
  width: 100%;
  position: absolute;
  left: 0;
  top: 10px;
  -webkit-transition: all 0.2s ease;
  -moz-transition: all 0.2s ease;
  -o-transition: all 0.2s ease;
  -ms-transition: all 0.2s ease;
  transition: all 0.2s ease;
}

.digit span {
  display: block;
}

.button {
  display: inline-block;
  padding: 5px;
  background: #fff;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  font-size: 26px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  position: absolute;
  top: 68%;
  margin-top: -20px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 8px;
  cursor: pointer;
  -webkit-transition: -webkit-transform 0.3s cubic-bezier(0, 0.99, 0.44, 1.4);
  -moz-transition: -moz-transform 0.3s cubic-bezier(0, 0.99, 0.44, 1.4);
  -o-transition: -o-transform 0.3s cubic-bezier(0, 0.99, 0.44, 1.4);
  -ms-transition: -ms-transform 0.3s cubic-bezier(0, 0.99, 0.44, 1.4);
  transition: transform 0.3s cubic-bezier(0, 0.99, 0.44, 1.4);

  -webkit-touch-callout: none; /* iOS Safari */
  -webkit-user-select: none; /* Safari */
  -khtml-user-select: none; /* Konqueror HTML */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* Internet Explorer/Edge */
  user-select: none;
}

.plus {
  right: -20px;
  color: #538ae4;
}

.minus {
  left: -20px;
  color: #e4535a;
}

.disabled {
  color: #ccc;
}

.button:hover {
  -moz-transform: scale(1.2);
  -webkit-transform: scale(1.2);
  -o-transform: scale(1.2);
  -ms-transform: scale(1.2);
  transform: scale(1.2);
}

.button:active {
  -moz-transform: scale(1);
  -webkit-transform: scale(1);
  -o-transform: scale(1);
  -ms-transform: scale(1);
  transform: scale(1);
}
</style>
