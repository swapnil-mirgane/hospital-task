<template>
  <div>
    <h2 class="align-middle">Welcome Make our Apporment</h2>
    <div class="flex flex-wrap justify-around gap-5">
      <Cart id="a1" startTime="9:00:00 AM" endTime="9:10:00 AM"></Cart>
      <Cart id="a2" startTime="9:10:00 AM" endTime="9:20:00 AM"></Cart>
      <Cart id="a3" startTime="9:20:00 AM" endTime="9:30:00 AM"></Cart>
      <Cart id="a4" startTime="9:30:00 AM" endTime="9:40:00 AM"></Cart>
      <Cart id="a5" startTime="9:40:00 AM" endTime="9:50:00 AM"></Cart>

      <Cart id="a6" startTime="9:50:00 AM" endTime="10:00:00 AM"></Cart>
      <Cart id="a7" startTime="10:00:00 AM" endTime="10:10:00 AM"></Cart>
      <Cart id="a8" startTime="10:10:00 AM" endTime="10:20:00 AM"></Cart>
      <Cart id="a9" startTime="10:20:00 AM" endTime="10:30:00 AM"></Cart>
      <Cart id="a10" startTime="10:30:00 AM" endTime="10:40:00 AM"></Cart>

      <Cart id="a11" startTime="10:40:00 AM" endTime="10:50:00 AM"></Cart>
      <Cart id="a12" startTime="10:50:00 AM" endTime="11:00:00 AM"></Cart>
      <Cart id="a13" startTime="11:00:00 AM" endTime="11:10:00 AM"></Cart>
      <Cart id="a14" startTime="11:10:00 AM" endTime="11:20:00 AM"></Cart>
      <Cart id="a15" startTime="11:20:00 AM" endTime="11:30:00 AM"></Cart>

      <Cart id="a16" startTime="11:30:00 AM" endTime="11:40:00 AM"></Cart>
      <Cart id="a17" startTime="11:40:00 AM" endTime="11:50:00 AM"></Cart>
      <Cart id="a18" startTime="11:50:00 AM" endTime="12:00:00 PM"></Cart>
      <Cart id="a19" startTime="12:00:00 AM" endTime="12:10:00 PM"></Cart>
      <Cart id="a20" startTime="12:10:00 AM" endTime="12:20:00 PM"></Cart>

      <Cart id="a21" startTime="12:20:00 AM" endTime="12:30:00 PM"></Cart>
      <Cart id="a22" startTime="12:30:00 AM" endTime="12:40:00 PM"></Cart>
      <Cart id="a23" startTime="12:40:00 AM" endTime="12:50:00 PM"></Cart>
      <Cart id="a24" startTime="12:50:00 AM" endTime="1:00:00 PM"></Cart>
      <Cart id="a25" startTime="1:00:00 AM" endTime="1:10:00 PM"></Cart>
    </div>
  </div>
</template>
<script>
import Cart from "../components/Cart.vue";

export default {
  components: {
    Cart,
  },
};
</script>
