<template>
<div>
    <!--------------------START PROJECT-------------------------------------------------->
    <p class="base">Projects</p>
    <div class="flex-container" v-for="(projects,k) in projects" :key="k">
        <!--------------------------FirstSection-------------------------------------------------->
        <div>
            <input type="text" placeholder="Name" v-model="projects.name"/>
            <input type="text" placeholder="Highlights" v-model="projects.highlights"/>
            <input type="text" placeholder="Keyword"/>
            <input type="text" placeholder="Description" v-model="projects.description">
        </div>
        <!--------------------------endFirstSection-------------------------------------------------->

        <!--------------------------SecondSection-------------------------------------------------->
        <div class="Flex_for_Duration">
                <div>
                    <input onfocus="(this.type='date')" placeholder="Start Date" v-model="projects.startDate"/>
                    <input type="text" placeholder="URL" v-model="projects.url"/>
                </div>

                <div>
                    <input onfocus="(this.type='date')" placeholder="End Date" v-model="projects.endDate"/>
                    <input type="text" placeholder="Roles" v-model="projects.roles"/>
                </div>
            </div>
        <!--------------------------endSecondSection-------------------------------------------------->

         <!--------------------------ThirdSection-------------------------------------------------->
        <div class="Flex_for_Duration">
                <div>
                    <input type="text" placeholder="Entity" v-model="projects.entity"/>
                </div>
                <div>
                    <input type="text" placeholder="type" v-model="projects.type"/>
                </div>
            </div>
        <!--------------------------endThirdSection-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    <button @click.prevent="addProject(k)">Add</button>
    <button @click.prevent="delProject(k)" v-show="k || ( !k && projects.length > 1)">Remove</button>
    show: {{projects}}
    <!------------------------------------END PROJECT------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Twelve',
    components: {},
    data(){
        return{
            projects:[{
                name:'',
                description:'',
                highlights:'',
                keywords:'',
                startDate:'',
                endDate:'',
                url:'',
                role:'',
                entity:'',
                type:''
            }]
        }
    },
    methods:{
        addProject(){
            this.projects.push({
                name:'',
                description:'',
                highlights:'',
                keywords:'',
                startDate:'',
                endDate:'',
                url:'',
                role:'',
                entity:'',
                type:''
            })
        },
        delProject(k){
            this.projects.splice(k,1)
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
.Flex_for_Duration {
    display: flex;
    margin-top: 60px;
}

.Flex_for_Duration>div {
    width: 522px;
    margin: 10px;
    text-align: center;
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
