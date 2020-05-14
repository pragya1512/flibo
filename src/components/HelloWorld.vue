<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <br />
    <label>Input</label>
    <br />
    <input type="text" name="input" id="i" placeholder="Enter Numeric Value" />
    <br />
    <input type="button" name="b1" id="b1" value="CUBE" @click="handleClick" />
    <br />
    <span id="Span">{{ message }}</span>
  </div>
</template>

<script const Vue="window.vue">
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  methods: {
    handleClick: function() {
      var num = document.getElementById("i").value;
      var pattern = /^[0-9]{1,}$/;
      if (pattern.test(num)) {
        document.getElementById("Span").innerText = num * num * num;
      } else {
        alert("Enter only numeric value");
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello label {
  color: rgb(47, 83, 6);
  font-family: "Times New Roman", Times, serif;
  font-size: xx-large;
  font-weight: bold;
  position: absolute;
  margin: 10px 0px 0px 0px;
  left: 48%;
}

.hello input[type="text"] {
  background-color: whitesmoke;
  display: inline-block;
  position: absolute;
  margin: 35px 0px 16px 0px;
  font-size: large;
  padding: 20px;
  width: 270px;
  height: 30px;
  color: rgb(20, 17, 17);
  border: 5px solid rgb(172, 201, 6);
  resize: vertical;
  box-sizing: border-box;
  text-align: center;
  left: 41%;
}
.hello input[type="button"] {
  background-color: rgb(38, 99, 9);
  color: white;
  position: relative;
  margin: 20px 0px 0px 0px;
  font-weight: bolder;
  cursor: pointer;
  height: 35px;
  width: 270px;
  left: 1%;
  top: 55px;
  margin-bottom: 10px;
  text-align: center;
  font-size: 20px;
  padding: 10px 20px;
  border: none;
}

#Span {
  color: rgb(10, 9, 9);
  background-color: whitesmoke;
  display: inline-block;
  position: relative;
  margin: 55px 0px 16px 0px;
  margin-bottom: 70px;
  font-size: large;
  padding: 25px;
  border: 5px solid rgb(172, 201, 6);
  resize: vertical;
  box-sizing: border-box;
  text-align: center;
  left: 1%;
  width: 270px;
  height: 30px;
  font-family: "Times New Roman", Times, serif;
}
</style>
