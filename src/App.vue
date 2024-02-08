<template>
  <form>
    <div>
      <pre>
        {{JSON.stringify(formValues, null,2)}}
      </pre>
    </div>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary" />
    </div>


    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.joblocation">
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no"/>
      <label for="remoteWork">Open to remote work</label>
    </div>

    <div>
      <label>Skill set</label>
      <input type="checkbox" id="html" value="html"/>

      <label for="html">HTML</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet"/>
      <label for="css">Css</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet" />
      <label>Javascript</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet"/>
    </div>
  </form>
 
</template>



<script>
export default {
  name: "App",
  data() {
    return {
      formValues:{
        name:'',
        profileSummary:'',
        country: '',
        joblocation:[],
        remoteWork:"no",
        skillSet:[],
        
      }
         
    };
  },
  methods:{
   
   
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}
label{
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label{
  font-weight: bold;
  display: flex;
  margin-right: 5px;
  
}
input[type='text'],
textarea,
select{
  display: block;
  width:400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: hotpink;
  background-color: pink ;
  background-image: none;

}
</style>
