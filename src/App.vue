<template>
  <div>
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">bind</button>
    <h2 class="underline">Underlined text</h2>
    <h2 class="underline" v-bind:class="status">Status</h2>
    <h1 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h1>
    <h2 v-bind:class="isSoldOut ? 'sold-out':'new' ">Soldout? movie</h2>
    <h2 v-bind:class="['new', 'promoted']">Newly promoted movie</h2>
    <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out':'new']">Array conditional</h2>
     <h2 v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      'sold-out': isSoldOut
     }">Object Conditional movie</h2>
  </div>
</template>

 
<script>
export default {
  name: 'App',
  data(){
    return{
      name:'Iyanu',
      greet:"Hello",
      channel:'codevolution',
      headingId:'heading',
      isDisabled:false,
      status:'danger',
      isPromoted:false,
      isSoldOut:false
    }
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}

.underline{
  text-decoration: underline;

}

.promoted{
  font-style: italic;
}

.new{
  color: crimson;
}
.sold-out {
  color: blue;


}
</style>
