<template>
<div>
    <!--------------------START CERTIFICATE-------------------------------------------------->
    <p class="base">Certificate</p>
    <div class="flex-container" v-for="(certificate,k) in certificate" :key="k">
        <!--------------------------LeftSection-------------------------------------------------->
        <div>
            <input onfocus="(this.type='date')" placeholder="Date" v-model="certificate.date"/>
             <input type="text" placeholder="Issuer" v-model="certificate.issuer"/>
        </div>
        <!--------------------------endLeftSection-------------------------------------------------->

        <!---------------------------START Right Section-------------------------------------------------->
        <div>
            <input type="text" placeholder="Name" v-model="certificate.name"/>
            <input type="text" placeholder="Url" v-model="certificate.url"/>
        </div>
        <!---------------------------End Right Section-------------------------------------------------->
    </div>
    <button @click.prevent="newCertificate(k)">Add +</button>
    <button @click.prevent="delCertificate(k)" v-show="k || ( !k && certificate.length > 1)">Remove</button>
    <!--FLEX-CONTAINER-CLOSE-->
    show: {{certificate}}
    <!------------------------------------END CERTIFICATE------------------------------------------------------>
    
    

</div>
</template>

<script>
export default {
    name: 'Six',
    components: {},
    data(){
        return{
            certificate:[{
                date:'',
                issuer:'',
                name:'',
                url:''
            }]
        }
    },
    methods:{
        newCertificate() {
            this.certificate.push({
                date:'',
                issuer:'',
                name:'',
                url:''
            })
        },
        delCertificate(k){
            this.certificate.splice(k,1)
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
