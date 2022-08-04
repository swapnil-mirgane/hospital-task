<template>
  <div id="hide">
    <div class="flex flex-col w-1/2 m-auto">
      <label class="m-5" for="valisName"
        >name : <input type="text" id="valisName" v-model.lazy="cName" required
      /></label>
      <label class="m-5" for="num"
        >mobail:
        <input type="number" id="num" v-model.lazy="cNum" maxlength="10" required
      /></label>
      <div class="flex">
        <button
          @click="booked()"
          class="w-1/3 border-2 m-1 border-black rounded-md hover:bg-red-700"
        >
          save</button
        ><button
          @click="cancel"
          class="w-1/3 border-2 m-1 border-black rounded-md hover:bg-red-700"
        >
          cancel
        </button>
      </div>
    </div>
  </div>
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
        class="bg-green-700 border-4 border-black w-1/4"
        v-for="(item, i) in timeSlots"
        v-bind:id="i"
      >
        <div class="font-bold text-xl p-5">Start Time {{ item.startTime }}</div>
        <div class="font-bold text-xl p-5">End Time {{ item.endTime }}</div>

        <button
          @click="book(i)"
          class="bg-lime-400 border-2 p-2 border-black rounded-md ml-20 mb-5 hover:bg-lime-500"
        >
          BookNow
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      timeSlots: [],
      valis: false,
      cName: "",
      cnum: "",
    };
  },
  methods: {
    cancel() {
      document.getElementById("hide").style = "display:none";
    },

    booked() {
      var s = document.getElementById("valisName").value;
      var cn = document.getElementById("num").value;
      if (s == "" && cn == "") {
        alert("name should not empty");
        this.valis = false;
      }
      this.cName = s;
      this.cnum = cn;
      document.getElementById("hide").style = "display:none";
      this.valis = true;
    },
    book(i) {
      var s = document.getElementById(i);
      document.getElementById("hide").style = " visibility: visible;";
      var s = document.getElementById(i);
      if (this.valis == true) {
        s.style = " background-color: rgb(238, 15, 15);";
        s.lastElementChild.innerHTML = `<button @click="book">EditSlot</button>`;
        s.firstElementChild.innerHTML += `<h1> name:${this.cName}</h1><br><h1>Number:${this.cnum}</h1>`;
        location.href = "#hide";
        this.cName = "";
        this.cnum = "";
      }
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
  },
};
</script>
