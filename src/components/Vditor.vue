<template>
    <div id="vditor" />    
</template>
<script>

import Vditor from "vditor";
import "vditor/dist/index.css";
 
export default {
  /* eslint-disable */
  name: "editor",
  mounted: function () {
    this.contentEditor = new Vditor("vditor", {
      height: 660,
      toolbarConfig: {
        pin: true,
      },
      cache: {
        enable: false,
      },
      after: () => {
        this.contentEditor.setValue("hello, Vditor + Vue!");
      },
 
    });
  },
};
</script>
