<template>
  <div>
    <div class="bg-lime-500 w-1/3 m-auto mt-20">
      <table>
        <tr>
          <td>
            <label for="user" class="m-5 p-5">User</label>
          </td>
          <td>
            <select id="user" class="bg-lime-500 m-5 p-5">
              <option disabled>Select User</option>
              <option value="Admin">Admin</option>
              <option value="Staf">Staff</option>
            </select>
          </td>
        </tr>
        <tr>
          <td><label for="userName" class="m-5 p-5">UserName</label></td>
          <td>
            <input
              type="text"
              autocomplete="off"
              class="bg-lime-500 m-5 p-5"
              id="userName"
              v-model.lazys="loginDetails.userName"
              placeholder="UserName"
            />
          </td>
        </tr>
        <tr>
          <td><label class="m-5 p-5" for="pass">Password</label></td>
          <td>
            <input
              autocomplete="off"
              class="bg-lime-500 m-5 p-5"
              type="passowrd"
              v-model="loginDetails.pass"
              id="pass"
              placeholder="Enter the password"
            />
          </td>
        </tr>
      </table>
      <!-- <p>{{loginDetails.userName}}</p> -->
      <button
        class="ml-28 mb-7 p-5 w-1/2 bottom-2 border border-gray-900 rounded-md hover:bg-lime-700"
        @click="login"
      >
        Login
      </button>
    </div>
  </div>
</template>
<script setup>
const loginDetails = reactive({
  userName: "",
  pass: "",
});
function login() {
  if (loginDetails.userName == "swapnil" && loginDetails.pass == "swapnil") {
    alert("Login Successfull");
    location.href = "http://localhost:3000/Home";
  } else {
    alert("plz Enter User= swapnil  pass= swapnil");
  }
}
</script>
