<template>
  <div id="app">
    <div>
      <input
        type="checkbox"
        id="showBorder"
        name="showBorder"
        v-model="showBorder"
      />
      <label for="showBorder">Show border</label><br />
    </div>
    <div>
      <input type="checkbox" id="boldFont" name="boldFont" v-model="boldFont" />
      <label for="boldFont">Bold font</label><br />
    </div>
    <div>
      <input
        type="checkbox"
        id="italicFont"
        name="italicFont"
        v-model="italicFont"
      />
      <label for="italicFont">Italic font</label><br />
    </div>
    <div>
      <input
        type="checkbox"
        id="showPadding"
        name="showPadding"
        v-model="showPadding"
      />
      <label for="showPadding">Show padding</label><br />
    </div>
    <div>
      <input
        type="checkbox"
        id="showBackground"
        name="showBackground"
        v-model="showBackground"
      />
      <label for="showBackground">Show background</label><br />
    </div>
    <div class="np-preview-container">
      <div class="np-preview-title">Preview</div>
      <div>
        <div
          v-bind:class="[
            'np-button',
            showBorder ? 'np-button__border' : '',
            italicFont ? 'np-button__italic' : '',
            boldFont ? 'np-button__bold' : '',
            showPadding ? 'np-button__padding' : '',
            showBackground ? 'np-button__background' : '',
          ]"
        >
          Some button
        </div>
      </div>
    </div>
    <div class="np-credits">www.nightprogrammer.com</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      showBorder: false,
      boldFont: false,
      italicFont: false,
      showPadding: false,
      showBackground: false,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 8px;
}
.np-preview-title {
  font-weight: 600;
}
.np-preview-container {
  margin-top: 16px;
}
.np-button {
  margin-top: 10px;
  width: 130px;
  text-align: center;
}
.np-button__padding {
  padding: 4px;
}
.np-button__background {
  background: #eee;
}
.np-button__border {
  border: 1px solid hsl(0, 0%, 61%);
}
.np-button__italic {
  font-style: italic;
}
.np-button__bold {
  font-weight: bold;
}
.np-credits {
  font-size: 12px;
  margin-top: 24px;
}
</style>