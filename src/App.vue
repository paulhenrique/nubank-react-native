<template>
  <Container>
    <StatusBar barSyle="light-content" backgroundColor="#8b10ae" />
    <view>
      <Header/>
      <Tabs/>
    </view>
  </Container>
</template>
<script>
import { StatusBar } from "react-native";
import Header from "./components/Header";
import Tabs from "./components/Tabs";
import Container from "./components/Container";
export default {
  name: "App",
  components: {
    StatusBar,
    Container,
    Header,
    Tabs
  },
};
</script>
