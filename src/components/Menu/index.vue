<template>
  <animated:view
    class="container"
    :style="{
      opacity: translateY.interpolate({
        inputRange: [0, 150],
        outputRange: [0, 1],
      }),
    }"
  >
    <view class="code">
      <image
        class="qrcode"
        :source="require('../../assets/images/qrcode.png')"
      ></image>
    </view>
    <view class="nav">
      <view class="nav-item">
        <image
          class="icon"
          :source="
            require('../../assets/images/baseline_help_outline_white_24dp.png')
          "
        />
        <text class="nav-text">Me ajuda</text>
      </view>
      <view class="nav-item">
        <image
          class="icon"
          :source="
            require('../../assets/images/outline_person_outline_white_24dp.png')
          "
        />
        <text class="nav-text">Perfil</text>
      </view>
      <view class="nav-item">
        <image
          class="icon"
          :source="
            require('../../assets/images/outline_credit_card_white_24dp.png')
          "
        />
        <text class="nav-text">Configurar cartão</text>
      </view>
      <view class="nav-item">
        <image
          class="icon"
          :source="
            require('../../assets/images/outline_smartphone_white_24dp.png')
          "
        />
        <text class="nav-text">Configurações do app</text>
      </view>
      <TouchableOpacity class="signOutBtn">
        <text class="signOutBtnText">SAIR DO APP</text>
      </TouchableOpacity>
    </view>
  </animated:view>
</template>
<script>
import { Animated } from "react-native";
import { TouchableOpacity } from "react-native";
export default {
  props: {
    translateY: Object,
  },
  name: "Menu",
  components: {
    TouchableOpacity,
  },
};
</script>

<style scoped>
.container {
  margin-left: 20px;
  margin-right: 20px;
  z-index: 4;
}
.code {
  align-items: center;
}
.qrcode {
  width: 80px;
  height: 80px;
}
.nav {
  margin-top: 30px;
  border-top-width: 0.3;
  border-top-color: white;
}
.nav-item {
  flex-direction: row;
  align-items: center;
  padding: 12px;

  border-bottom-width: 0.3;
  border-bottom-color: white;
}
.nav-text {
  color: white;
  margin-left: 20px;
  font-size: 15px;
}
.signOutBtn {
  border-width: 0.3;
  border-color: rgba(255, 255, 255, 0.8);
  border-radius: 4px;
  justify-content: center;
  align-items: center;
  padding: 12px;
  margin-top: 15px;
}

.signOutBtnText {
  color: white;
  font-weight: bold;
  font-size: 13px;
}
</style>
