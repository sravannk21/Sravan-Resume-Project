<template>
<div>
    <!--------------------START PUBLICATIONS-------------------------------------------------->
    <p class="base">Skills</p>
    <div class="flex-container" v-for="(skills,k) in skills" :key="k">
        <!--------------------------Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Name" v-model="skills.name"/>
            <select v-model="skills.level">
                <option>Beginner</option>
                <option>Advanced</option>
                <option>Moderate</option>
            </select>
             <input type="text" placeholder="Keywords" v-model="skills.keyword"/>
             <button @click.prevent="newKeyword(k)">Add</button>
        </div>
        <!--------------------------endSection-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    <button @click.prevent="addSkill(k)">Add</button>
    <button @click.prevent="delSkill(k)" v-show="k || ( !k && skills.length > 1)">Remove</button>
    show: {{skills}}
    <!------------------------------------END SKILLS------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Eight',
    components: {},
    data(){
        return{
            skills:[{
                name:'',
                level:'',
                keyword:''
            }]
        }
    },
    methods:{
        addSkill(){
            this.skills.push({
                name:'',
                level:'',
                keyword:''
            })
        },
        delSkill(k){
            this.skills.splice(k,1)
        }
    }
    }

</script>

<style scoped>
/* BASIC iNPUT STYLE */
input, select {
    background: rgba(255, 255, 255, 0.4);
    border: none;
    border-bottom: 1.5px solid rgb(46, 129, 207);
    width: 400px;
    height: 30p;
    margin: 15px;
    padding: 10px;
    color: #333;
}

input:hover,select:hover {
    -webkit-box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
    box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
}
/* END BASIC iNPUT STYLE */

/* LAYOUT*/
.flex-container {
    display: grid;
}

.flex-container>div {
    margin: 10px;
    text-align: center;
}
button {
    margin: 25px;
    padding: 10px 10px;
    outline: 0;
    width: 120px;
    font-size: 14px;
    font-weight: bold;
    text-align: center;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: .08em;
    background-color: #3b4050;
    border: none;
    color: white;
    border-radius: 10px;
}

button:hover {
    color: rgb(255, 255, 255);
    background: rgb(46, 129, 207);
    border-radius: 10px;
}
.base {
    font-size: 24px;
    letter-spacing: 2px;
    padding-top: 25px;
}
textarea{
    background: rgba(255, 255, 255, 0.4);
    border: none;
    border-bottom: 1.5px solid rgb(46, 129, 207);
    width: 400px;
    height: 103px;
    margin: 15px;
    padding: 10px;
    color: #333;
}
textarea:hover {
    -webkit-box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
    box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
}
/* END LAYOUT*/

@media (max-width: 320px) {
    .container {
        width: 100%;
    }

    .container2 {
        width: 100%;
    }
}

@media (max-width: 480px) {
    .container {
        width: 100%;
    }

    .container2 {
        width: 100%;
    }
}

@media (max-width: 768px) {
    .container {
        width: 100%;
    }

    .container2 {
        width: 100%;
    }
}


</style>
