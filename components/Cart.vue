<template>
  <div id="cartBg" class="bg-fuchsia-300 border-4 border-black w-1/4">
    <div class="font-bold text-xl p-5">Start Time {{ startTime }}</div>
    <div class="font-bold text-xl p-5">End Time {{ endTime }}</div>
    <div>
      <button
        id="btn"
        @click="book()"
        class="bg-lime-400 border-2 p-2 border-black rounded-md ml-20 mb-5 hover:bg-lime-500"
      >
        Book Now
      </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: new Date().toLocaleTimeString(),
    };
  },

  props: {
    startTime: String,
    endTime: String,
    id: String,
  },
  methods: {
    book() {
      document.getElementById("cartBg").style = "border-color:red";
      document.getElementById("btn").innerHTML = "Booked";
      // location.href = "http://localhost:3000/Form";
      document.getElementById("btn").innerHTML = "Booked";
    },
  },
};
</script>
<style scoped></style>
