<template>
  <Container>
    <StatusBar barSyle="light-content" backgroundColor="#8b10ae" />
    <view class="container">
      <Header />
      <Menu />
      <Card />
      <Tabs />
    </view>
  </Container>
</template>
<script>
import { StatusBar } from "react-native";
import Header from "./components/Header";
import Card from "./components/Card";
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
    Card,
    Menu
  },
};
</script>
<style scoped>
.container{
  display:flex;
}
</style>