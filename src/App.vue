<template>
  <Container>
    <StatusBar barSyle="light-content" backgroundColor="#8b10ae" />
    <view class="container">
      <Header />
      <Menu />
      <PanGestureHandler
        :onGestureEvent="onGestureEventOcurred"
        :onHandleStateChage="onHandleStateChaged"
      >
        <view class="card">
          <view class="cardHeader">
            <view class="cardHeaderLeftText">
              <image
                class="icon"
                :source="
                  require('./assets/images/baseline_visibility_off_black_18.png')
                "
              />
              <text class="cardHeaderText">Conta</text>
            </view>
            <image
              class="icon"
              :source="
                require('./assets/images/baseline_visibility_off_black_18.png')
              "
            />
          </view>
          <view class="cardContent">
            <text class="cardTitle">Saldo disponível</text>
            <text class="cardDescription">R$ 257.354,64</text>
          </view>
          <view class="cardFooter">
            <image
              class="iconCardFooter"
              :source="
                require('./assets/images/baseline_help_outline_black_24dp.png')
              "
            />
            <text class="cardAnnotation"
              >Transferência de R$ 53,00 recebida em 24 JUL</text
            >
            <image
              class="iconCardFooter"
              :source="
                require('./assets/images/baseline_help_outline_black_24dp.png')
              "
            />
          </view>
        </view>
      </PanGestureHandler>
      <Tabs />
    </view>
  </Container>
</template>
<script>
import { Animated } from "react-native";
import { PanGestureHandler, State } from "react-native-gesture-handler";
import { StatusBar } from "react-native";
import Header from "./components/Header";
import Tabs from "./components/Tabs";
import Container from "./components/Container";
import Menu from "./components/Menu";
export default {
  name: "App",
  components: {
    StatusBar,
    Container,
    Header,
    Tabs,
    Menu,
    PanGestureHandler,
    State,
    Animated,
  },
  computed:{
    animatedEvent(){
      return new Animated.Value(0);
    },
    animatedEvent(){
      return new Animated.Value(0);
    }
  },
  data: function () {
    return {
      handleChanged: false,
    };
  },
  methods: {
    onHandleStateChaged: function () {
      this.handleChanged = true;
    },
    onGestureEventOcurred: function () {},
  },
};
</script>
<style scoped>
.container {
  flex: 1;
  max-height: 330px;
  z-index: 5;
}

.card {
  flex: 1;
  background-color: #fff;
  border-radius: 4px;
  margin: 20px;
  height: 100%;
  position: absolute;
  left: 0;
  right: 0;
  top: 100px;
}

.cardHeader {
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
}
.cardHeaderLeftText {
  flex-direction: row;
  align-items: center;
}
.cardHeaderText {
  margin-left: 10px;
  font-size: 15px;
  color: #696969;
}

.cardContent {
  flex: 1;
  padding-left: 30px;
  padding-right: 30px;
  justify-content: center;
}
.cardTitle {
  font-size: 15px;
  color: #696969;
}

.cardDescription {
  font-size: 32px;
  margin-top: 3px;
  color: #060606;
  font-weight: bold;
}

.cardFooter {
  padding: 30px;
  background-color: #eeeeee;
  border-radius: 4px;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.cardAnnotation {
  font-size: 13px;
  color: #696969;
  width: 70%;
}
</style>
