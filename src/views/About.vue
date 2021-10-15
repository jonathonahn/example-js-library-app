<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div id="picker"></div>
  </div>
</template>

<script>
/* global iro */
export default {
  data: function () {
    return { pickerColorString: "blahblah" };
  },
  mounted: function () {
    // COLORPICKER (iro.js) STUFF
    var colorPicker = new iro.ColorPicker("#picker");
    console.log(colorPicker);
    colorPicker.on("color:change", function (color) {
      // log the current color as a HEX string
      console.log(color.hexString);
    });
  },
  methods: {},
};
</script>
