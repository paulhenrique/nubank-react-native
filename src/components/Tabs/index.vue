<template>
  <view class="container">
    <ScrollView
      class="tabsContainer"
      :contentContainerStyle="{
        paddingLeft: 10,
        paddingRight: 20,
      }"
      :horizontal="true"
      :showHorizontalScrollIndicator="true"
    >
      <view class="tabItem">
        <image
          class="icon"
          :source="require('../../assets/images/baseline_person_add_white_18dp.png')"
        />
        <text class="tabText">Indicar Amigos</text>
      </view>
      <view class="tabItem">
        <image
          class="icon"
          :source="require('../../assets/images/baseline_chat_bubble_outline_white_18dp.png')"
        />
        <text class="tabText">Cobrar</text>
      </view>
      <view class="tabItem">
        <image
          class="icon"
          :source="require('../../assets/images/baseline_arrow_downward_white_18dp.png')"
        />
        <text class="tabText">Depositar</text>
      </view>
      <view class="tabItem">
        <image
          class="icon"
          :source="require('../../assets/images/baseline_arrow_upward_white_18dp.png')"
        />
        <text class="tabText">Transferir</text>
      </view>
      <view class="tabItem">
        <image
          class="icon"
          :source="require('../../assets/images/baseline_lock_white_18dp.png')"
        />
        <text class="tabText">Bloquear cartão</text>
      </view>
    </ScrollView>
  </view>
</template>
<script>
import { ScrollView } from "react-native";
export default {
  name: "Tabs",
  components: {
    ScrollView,
  },
};
</script>
<style scoped>
.container {
  height: 100px;
  z-index: 5;
  /* margin-top: 20px; */
}
.tabItem {
  width: 100px;
  height: 100px;
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 3px;
  margin-left: 10px;
  padding: 10px;
  justify-content: space-between;
}
.tabText {
  font-size: 13px;
  color: white;
}
</style>
