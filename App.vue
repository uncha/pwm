<template>
    <web-view
        :source="{uri:'http://pwm.cafe24app.com'}"
        :style="{marginTop: 40}"
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
