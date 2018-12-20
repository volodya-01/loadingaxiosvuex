<template>
  <div class="hello">
    <div>
      <loading/>
    </div>
  
  </div>
</template>

<script>
import loading from "@/components/loading";
import api from './../axios/api.js'
export default {
  name: "HelloWorld",
  data() {
    return {
     
    };
  },
  components: {
    loading
  },
  mounted() {
    api.fzaxios("https://112.64.170.158:8190/Service1.svc/GetWaterworks")
      .then(res => {
        console.log(res);
       
      });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
