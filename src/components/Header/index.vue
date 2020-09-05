<template>
  <view class="container">
    <view class="top">
      <image :source="require('../../assets/images/Nubank_Logo.png')" />
      <text class="title">Paulo</text>
    </view>
    <view class="down-keyboard-arrow">
      <image
        :source="
          require('../../assets/images/baseline_keyboard_arrow_down_white_18dp.png')
        "
      />
    </view>
  </view>
</template>
<script> 
export default {
  name: "Header",
  components: {},
};
</script>
<style>
.container {
  align-items: center;
  padding: 40px 0 30px;
}
.top {
  flex-direction: row;
  align-items: center;
}
.title {
  color: white;
  font-size: 18px;
  font-weight: bold;
  margin-left: 8px;
}
.icon {
  background-color: white;
  color: white;
  height: 30px;
  width: 30px;
}

.down-keyboard-arrow {
  align-items:center;
}
</style>
