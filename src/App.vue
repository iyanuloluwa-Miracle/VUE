<template>
  <div>
    <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">bind</button>
    <h2 class="underline">Underlined text</h2>
    <h2 class="underline" :class="status">Status</h2>
    <h1 :class="{ promoted: isPromoted }">Promoted Movie</h1>
    <h2 :class="isSoldOut ? 'sold-out' : 'new'">Soldout? movie</h2>
    <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
    <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">
      Array conditional
    </h2>
    <h2 :class="{ promoted: isPromoted, new: !isSoldOut, 'sold-out': isSoldOut }">
      Object Conditional movie
    </h2>

    <h2 :style="{ color: highlightColor, 'font-size': headerSize + 'px', padding: '20px' }">
      Inline Style
    </h2>
    <h3 :style="headerStyleObject">Style Objects</h3>
    <div :style="[baseStyleObject, sucessStyleObject]">Success Style</div>
    <div :style="[baseStyleObject, dangerStyleObject]">Danger</div>
  </div>
</template>


<script>
export default {
  name: "App",
  data() {
    return {
      name: "Iyanu",
      greet: "Hello",
      channel: "codevolution",
      headingId: "heading",
      isDisabled: false,
      status: "danger",
      isPromoted: false,
      isSoldOut: false,
      highlightColor: "orange",
      headerSize:40,
      headerStyleObject: {
        color:'orange',
        fontSize:'50px',
        padding:'20px'

      },
      baseStyleObject:{
        fontSize:'50px',
        padding:'10px',
        textAlign:'center',
        
      },
      sucessStyleObject:{
        color:'#800000',
        backgroundColor:'#C71585',
        border:'1px solid #FAFAD2',
        textAlign:'center',
       
      },
      dangerStyleObject:{
        color:'#800000',
        backgroundColor:'red',
        border:'1px solid #FAFAD2',
        textAlign:'center',
       
      }
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: crimson;
}
.sold-out {
  color: blue;
}
</style>
