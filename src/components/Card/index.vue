<template>
  <view class="content">
    <view class="card">
      <view class="cardHeader">
        <image
          class="icon"
          :source="
            require('../../assets/images/baseline_visibility_off_black_18.png')
          "
        />
        <image
          class="icon"
          :source="
            require('../../assets/images/baseline_visibility_off_black_18.png')
          "
        />
      </view>
      <view class="cardContent">
        <text class="cardTitle">Saldo disponível</text>
        <text class="cardDescription">R$ 257.354,64</text>
      </view>
      <view class="cardFooter">
        <text class="cardAnnotation"
          >Transferência de R$ 53,00 recebida de Paulo Henrique Vieira hoje às
          06:00h</text
        >
      </view>
    </view>
  </view>
</template>
<script>
export default {
  name: "Card",
};
</script>
<style>
.content {
  flex: 1;
  max-height: 400px;
  min-height: 300px;
  justify-content: center;
  z-index: 5;
  padding-left: 10px;
  padding-right: 10px;
}

.card {
  flex: 1;
  background-color: white;
  border-radius: 4px;
  margin: 0 20px;
  height: 100%;
  position:absolute;
  left:0;
  right: 0;
  top:320px;
  
}

.cardHeader {
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
}
.cardContent {
  flex: 1;
  padding-left: 30px;
  padding-right: 30px;
  justify-content: center;
}
.cardTitle {
  font-size: 13px;
  color: #999999;
}

.cardDescription {
  font-size: 32px;
  margin-top: 3px;
  color: #333;
}

.cardFooter {
  padding: 30px;
  background-color: #eeeeee;
  border-radius: 4px;
}

.cardAnnotation {
  font-size: 12px;
  color: #333333;
}
</style>
