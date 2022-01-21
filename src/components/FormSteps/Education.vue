<template>
<div>
    <!--------------------START WORK-------------------------------------------------->
    <p class="base">Education</p>
    <div class="flex-container">
        <!--------------------------LeftSection-------------------------------------------------->
        <div>
            <input type="text" placeholder="URL" v-model="education.url"/>
            <input type="text" placeholder="Study Type" v-model="education.studyType"/>
            <input onfocus="(this.type='date')" placeholder="End Date" v-model="education.endDate"/>
            <input type="text" placeholder="Cources" v-model="education.cource"/>
            <button>Add new</button>
        </div>
        <!--------------------------endLeftSection-------------------------------------------------->

        <!---------------------------START Right Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Institution" v-model="education.institution"/>
            <input type="text" placeholder="Area" v-model="education.area"/>
            <input onfocus="(this.type='date')" placeholder="Start Date" v-model="education.endDate"/>
            <input type="text" placeholder="Score" v-model="education.score"/>
            <input type="text" placeholder="Highlights" v-model="education.highlights"/>
        </div>
        <!---------------------------End Right Section-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    show: {{works}}
    <!------------------------------------END WORK------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Four',
    components: {},
    data() {
        return {
            education:
                {
                    url:'',
                    studyType: '',
                    endDate: '',
                    cource: '',
                    institution: '',
                    area: '',
                    endDate: '',
                    score: '',
                    highlights:''
                },    
        }
    },
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
    display: flex;
    flex-wrap: nowrap;
}

.flex-container>div {
    width: 522px;
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
