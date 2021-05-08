<template>
    <web-view
        :source="{uri:'http://175.116.227.108:9102'}"
        :style="{marginTop: 0}"
    />
</template>

<script>
import { WebView } from "react-native-webview";
import * as Permissions from 'expo-permissions';
import { Camera } from 'expo-camera';

export default {
  name: "myComponent",
  data () {
      return {
          hasCameraPermission: false,
          type: Camera.Constants.Type.back,
      }
  },
  components: {
    "web-view": WebView,
    Camera
  },
  mounted () {
      Permissions.askAsync(Permissions.CAMERA)
     .then(status => {
       hasCameraPermission = status.status == "granted" ? true : false;
     }).catch((err)=>{
        console.log(err);
     });
  },
};
</script>
