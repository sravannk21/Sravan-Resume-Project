<template>
<div>
    <!--------------------START VOLUNTEER-------------------------------------------------->
    <p class="base">Volunteer</p>
    <div class="flex-container">
        <!--------------------------LeftSection-------------------------------------------------->
        <div>
            <input type="text" placeholder="Position" v-model="volunteer.position"/>
            <input onfocus="(this.type='date')" placeholder="Start Date" v-model="volunteer.startDate"/>
            <textarea placeholder="Summary" v-model="volunteer.summary" ></textarea>
        </div>
        <!--------------------------endLeftSection-------------------------------------------------->

        <!---------------------------START Right Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Organization" v-model="volunteer.organization" />
            <input type="text" placeholder="URL" v-model="volunteer.url" />
            <input onfocus="(this.type='date')" placeholder="End Date" v-model="volunteer.endDate" >
            <input placeholder="Highlights" v-model="volunteer.highlights" >
        </div>
        <!---------------------------End Right Section-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    show: {{volunteer}}
    <!------------------------------------END VOLUNTEER------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Three',
    components: {},
    data() {
        return {
            volunteer:
                {
                    position: '',
                    startDate:'',
                    summary: '',
                    organization:'',
                    url:'',
                    endDate:'',
                    highlights
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
