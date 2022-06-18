<template>
<pre>
  {{ JSON.stringify(formValues, null , 2)}}
</pre>
<form @submit="submitForm">
<div>
  <label for="name">Name</label>
  <input type="text" id="name" v-model.trim.lazy="formValues.name" />
</div>

<div>
  <label for="profile">Profile</label>
  <textarea  id="profile" v-model="formValues.profile" ></textarea>
</div>
<div>
  <label for="country">Country</label>
  <select id="country" v-model="formValues.country">
    <option value="">Select Country</option>
    <option value="Nepal">Nepal</option>
    <option value="India">India</option>
    <option value="China">China</option>
  </select>
</div>
<div>
  <label for="job-location">Job Locatioin</label>
  <select id="job-location" multiple v-model="formValues.jobLocation">
    <option value="Nepal">Nepal</option>
    <option value="India">India</option>
    <option value="China">China</option>
  </select>
</div>
<div>
  <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
  <label for="remoteWork">Open To Remote Work</label>
</div>
<div>
  <label>Skill Set</label>
  <input type="checkbox" id="html" value="html" v-model="formValues.skillSet">
  <label for="html">HTML</label>
  <input type="checkbox" id="css" value="css" v-model="formValues.skillSet">
  <label for="css">CSS</label>
  <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
  <label for="javascript">JavaScript</label>
</div>
<div>
  <label>Year Of Experience</label>
  <input type="radio" id="0-2" value="0-2" v-model="formValues.yoe"><label for="0-2">0-2</label>
  <input type="radio" id="2-4" value="2-4" v-model="formValues.yoe"><label for="2-4">2-4</label>
  <input type="radio" id="4-6" value="4-6" v-model="formValues.yoe"><label for="4-6">4-6</label>
</div>
<button>Submit</button>
</form>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      formValues:{
        name: '',
        profile:'',
        country:'',
        jobLocation:[],
        remoteWork: "no",
        skillSet: [],
        yoe:''
      }
      
      };
  },
  methods:{
    add(){
      return 3*10+20;
    },
    fullName(firstName, LastName){
        return firstName +" "+ LastName;
    },

    changeName(){
       this.name = "Sujata";
    },
    increment(){
      this.count +=1;
    },
    decrement(){
      this.count -=1;
    },
    submitForm(event){
      event.preventDefault();
      console.log('Form Values: ', this.formValues);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
div{
  display: block;
  width: 70%;
  margin: 0 auto;
  margin-top: 25px;
}

label{
  font-weight: bold;
  font-size: 16px;
  display: inline;
}
input[type='text'],
select, textarea{
  width: 100%;
  padding: 10px;
  display: block;
}


</style>
