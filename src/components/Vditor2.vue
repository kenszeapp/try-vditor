<template>
  <div>
    <div><button @click="btn1_click">Open console and Click here to see the md. </button></div>
    <div id="vditor2" />
  </div>
</template>

<script>

import Vditor from "vditor";
import "vditor/dist/index.css";

export default {
  /* eslint-disable */
  data() {
    return {  }
  },
  name: "editor",
  mounted: function () {
    this.contentEditor = new Vditor("vditor2", {
      height: 660,
      toolbarConfig: {
        pin: true,
      },
      cache: {
        enable: false,
      },
      after: () => {
        this.contentEditor.setValue("Get the md string, Vditor + Vue!");
      },
    });
  },

  methods: {
    btn1_click() {
      let s = this.contentEditor.getValue();
      console.log(s);
    }
  }

};
</script>
