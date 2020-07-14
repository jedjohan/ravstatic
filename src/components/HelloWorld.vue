<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    Här hämtar vi lite data {{fromfa}} från ett API. I detta fall en Azure Function som läser upp lite text från en textfil i en blobcontainer
    <h5>fast det funkar inte ännu</h5>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  fromfa?: any = null;

  async created() {
    console.log("hjj")
  }
}
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