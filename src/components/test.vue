<template>

<div>
    <h3>add a student</h3>
    <label> Name </label>
    <input type="text" v-model="name"><br>
    <label> Age </label>
    <input type="text" v-model="age"><br>
    <label> Gender </label>
    <select v-model="gender">
        <option value="male"> Male </option>
        <option value="female"> Female </option>
    </select><br>
    <input type="submit" value=" +ADD" @click="add_students()">
    <hr>
    <h3> students </h3>
    <ul>
        <li v-for="student in students" :key="student">
        name: {{student.name}} age : {{student.age}} Gender: {{student.gender}} 
        </li>
    </ul>
    
</div> 

</template>

<script>
export default {
    data() {
        return {
            name:"",
            age: "",
            gender:"",
            error:"",
            students : [
                {name: "mohamed", age: 20, gender: "male"},
                {name: "fatma", age: 23, gender: "female"},
                {name: "yaseen", age: 20, gender: "male"},
                {name: "Gueen", age: 20, gender: "female"},
            ]

        }
    },
    methods: {
        add_student: function() {
            if (this.name === "" | this.gender === "" | this.age === ""){
                this.error = "please fill all the cardentials";
            }
            else{
                this.new_stud = {name:this.name, age:this.age, gender:this.gender};
                this.students.push(this.new_stud);
                this.name = "";
                this.age = "";
                this.gender = "";
                this.error = "";
            }
        }

        },
    }
</script>