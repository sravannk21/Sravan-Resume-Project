<template>
<div>
    <!--------------------START WORK-------------------------------------------------->
    <p class="base">Works</p>
    <div class="flex-container">
        <!--------------------------LeftSection-------------------------------------------------->
        <div>
            <input type="text" placeholder="Location" v-model="works.location"/>
            <input type="text" placeholder="URL" v-model="works.url"/>
            <input onfocus="(this.type='date')" placeholder="Start Date" v-model="works.startDate"/>
            <input placeholder="End Date" onfocus="(this.type='date')"  v-model="works.endDate"/>
            <input type="text" placeholder="Highlights" v-model="works.highlights"/>
            <button @click.prevent="addHighlights(k)">Add New</button>
            <input type="text" placeholder="Keywords" v-model="works.keywords"/>
            <button>Add New</button>
        </div>
        <!--------------------------endLeftSection-------------------------------------------------->

        <!---------------------------START Right Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Company Name" v-model="works.companyName" />
            <input type="text" placeholder="Position" v-model="works.position" />
            <textarea placeholder="Description" v-model="works.description" ></textarea>
            <textarea placeholder="Summary" v-model="works.summary" ></textarea>
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
    name: 'Two',
    components: {},
    data() {
        return {
            works:
                {
                    location:'',
                    url: '',
                    startDate: '',
                    endDate: '',
                    highlights:'',
                    keywords: '',
                    companyName: '',
                    position: '',
                    description: '',
                    summary: ''
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
