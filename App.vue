<template>
    <web-view
        :source="{uri:'http://175.116.227.108:9102'}"
        :style="{marginTop: 0}"
    />
</template>

<script>
import { WebView } from "react-native-webview";

export default {
  name: "myComponent",
  components: {
    "web-view": WebView
  }
};
</script>
