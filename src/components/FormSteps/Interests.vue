<template>
<div>
    <!--------------------START INTERESTS-------------------------------------------------->
    <p class="base">Interests</p>
    <div class="flex-container" v-for="(interests, k) in interests" :key="k">
        <!--------------------------Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Name" v-model="interests.name"/>
            <input type="text" placeholder="Keywords" v-model="interests.keywords"/>
        </div>
        <!--------------------------endSection-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    <button @click.prevent="addInterests(k)">Add</button>
    <button @click.prevent="delInterests(k)" v-show="k || ( !k && interests.length > 1)">Remove</button>
    show: {{interests}}
    <!------------------------------------END INTERESTS------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Ten',
    components: {},
    data(){
        return{
            interests:[{
                name:'',
                keyword:''
            }]
        }
    },
    methods:{
        addInterests(){
            this.interests.push({
                name:'',
                keyword:''
            })
        },
        delInterests(k){
            this.interests.splice(k,1)
        }
    }
    }

</script>

<style scoped>
/* BASIC iNPUT STYLE */
input {
    background: rgba(255, 255, 255, 0.4);
    border: none;
    border-bottom: 1.5px solid rgb(46, 129, 207);
    width: 400px;
    height: 30p;
    margin: 15px;
    padding: 10px;
    color: #333;
}

input:hover {
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
