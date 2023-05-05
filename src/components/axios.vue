<template>
  <div>
    <p v-for="manu in manufacturer" :key="menu.Id">
      {{ menu.Id }} - {{ menu.Title }}
    </p>
  </div>
</template>

<script>
import axios from "axios"
export default {
  data() {
    return {
      text: "test",
      manufacturer: [{ Id: 1, Title: "test1" }],
    };
  },
created() {

}
  methods: {
    get(){
      axios.get("https://localhost:7032/api/manufacturers".then((response)
        .then.manufacturer = response.data; 
    };
  },
};
</script>