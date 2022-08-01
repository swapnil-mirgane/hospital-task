<template>
  <main class="flex justify-center w-full h-screen">
    <div>
      <form
        @submit="formSubmit"
        class="bg-gray-100 border-red-400 rounded-lg border-2 px-12 bg-gradient-to-r from-red-300 to-blue-200"
      >
        <table>
          <h2 class="pt-6">Admin Form</h2>
          <hr />
          <br />
          <label class="pt-10 py-10" for="firstname">Name:</label
          ><br />
          <input
            type="text"
            v-model="user.firstname"
            id="firstname"
            name="firstname"
            placeholder="Enter your Name"
          /><br /><br />
          <label for="number">Contact Number: </label
          ><br />
          <input
            type="number"
            v-model="user.number"
            id="number"
            name="number"
            placeholder="Enter your number"
          />
          <br /><br />
          <div>
            <button
              class="py-1 px-5 mr-5 bg-black hover:bg-cyan-500 shadow-lg shadow-cyan-500/50 text-white font-bold text-center rounded-md mb-3"
              type="submit"
              @click="formSubmit"
              id="btnsub"
            >
              Submit
            </button>
            <button
              class="py-1 px-5 bg-black hover:bg-cyan-500 shadow-lg shadow-cyan-500/50 text-white font-bold text-center rounded-md mb-3"
              type="reset"
            >
              Reset
            </button>
          </div>
        </table>
      </form>
    </div>
  </main>
</template>
<script>
export default {
  data() {
    return {
      isEdit: false,
      indexEdit: -1,
      users: [],
      user: {
        firstname: "",
        number: "",
      },
    };
  },
  methods: {
    formSubmit(event) {
      event.preventDefault();
      var name = document.getElementById("firstname").value;
      var contact = document.getElementById("number").value;
      alert(name + contact);
      location.href = "http://localhost:3000/Home";
    },
    onReset(event) {
      event.preventDefault();
      this.form.name = "";
      this.form.contact = "";
    },
  },
};
</script>
