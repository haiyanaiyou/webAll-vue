<template>
  <div class="hello">
    <!-- <v-input @input="val = arguments[0]" :value='val' /> -->
    <v-form :model='model' :rules='rules'>
      <v-form-item label="用户名" prop="username">
        <v-input v-model="model.username" type="text" />
      </v-form-item>
      <v-form-item label="密码" prop="password">
        <v-input v-model="model.password" type="password" />
      </v-form-item>
    </v-form>
  </div>
</template>

<script>
import VInput from "./Input.vue";
import VFormItem from "./FormItem.vue";
import VForm from "./Form";

export default {
  name: "HelloWorld",
  components: { VInput, VFormItem, VForm },
  provide(){
    return {
      
    }
  },
  data() {
    return {
      val: "",
      model: {},
      rules: {},
    };
  },
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
