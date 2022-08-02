<template>
  <div>
    <div>
      <button
        @click="showSlots"
        class="bg-lime-400 border-2 p-2 border-black rounded-md ml-20 mb-5 hover:bg-lime-500"
      >
        showSlots
      </button>
    </div>
    <div class="flex flex-wrap justify-between gap-4">
      <div
        class="bg-fuchsia-300 border-4 border-black w-1/4"
        v-for="(item, i) in timeSlots"
        v-bind:id="i"
      >
        <div class="font-bold text-xl p-5">Start Time {{ item.startTime }}</div>
        <div class="font-bold text-xl p-5">End Time {{ item.endTime }}</div>
        <div>
          <button
            @click="book(i)"
            class="bg-lime-400 border-2 p-2 border-black rounded-md ml-20 mb-5 hover:bg-lime-500"
          >
            Book Now
          </button>
        </div>
      </div>
    </div>

    <div id="hide">
      <label for="name">name : <input type="text" id="name" required /></label>
      <label for="phone">mobail: <input required type="number" /></label>
      <button @click="booked()" class="border-2 border-black rounded-md hover:bg-red-700">
        save</button
      ><button @click="cancel" class="border-2 border-black rounded-md hover:bg-red-700">
        cancel
      </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      timeSlots: [],
      valis: false,
    };
  },
  methods: {
    cancel() {
      document.getElementById("hide").style = "display:none";
    },

    booked() {
      document.getElementById("hide").style = "display:none";
      this.valis = true;
    },
    showSlots() {
      document.getElementById("hide").style = "display:none";
      var d;
      var e;

      d = new Date("2022-08-01 08:50:00");
      e = new Date("2022-08-01 09:50:00");
      for (let i = 1; i <= 20; i++) {
        d.setMinutes(d.getMinutes() + 10);
        e.setMinutes(d.getMinutes() + 10);
        this.timeSlots.push({
          startTime: d.toLocaleTimeString(),
          endTime: e.toLocaleTimeString(),
        });
      }
    },
    book(i) {
      document.getElementById("hide").style = " visibility: visible;";
      var s = document.getElementById(i);
      s.style = " background-color: rgb(97, 222, 222)";
    },
  },
};
</script>
<style scoped>
#hide {
  position: absolute;
  top: 30px;
  left: 10px;
}
</style>
