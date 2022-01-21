<template>
<div>
    <!--------------------START BASIC-------------------------------------------------->
    <p class="base">Basics</p>
    <div class="flex-container">
        <!--------------------------LeftSection-------------------------------------------------->
        <div>
            <input type="text" placeholder="Name" v-model="basics.name" />
            <input type="text" placeholder="Photo URL" v-model="basics.image" />
            <input type="text" placeholder="Phone" v-model="basics.phone" />
        </div>
        <!--------------------------endLeftSection-------------------------------------------------->

        <!---------------------------START Right Section-------------------------------------------------->
        <div>
            <input type="Phone" placeholder="Label" v-model="basics.label" />
            <input type="Email" placeholder="Email" v-model="basics.email" />
            <input type="text" placeholder="URL" v-model="basics.url" />
        </div>
        <!---------------------------End Right Section-------------------------------------------------->
    </div>
    <!--FLEX-CONTAINER-CLOSE-->
    show: {{basics}}
    <!------------------------------------END BASIC------------------------------------------------------>
    
    
    <!----------------------------------START LOCATION--------------------------------------->
        <p class="base">Location</p>
        <div class="flex-container">
            <!--Leftside-->
            <div>
                <input type="text" placeholder="Address" v-model="location.address" />
                <input type="text" placeholder="City" v-model="location.city" />
                <input type="text" placeholder="Region" v-model="location.region" />
            </div>
            <!--End LeftSide-->

            <!--Right Side-->
            <div>
                <input type="Phone" placeholder="Postal Code" v-model="location.postalCode" />
                <input type="Email" placeholder="Coutry Code" v-model="location.countryCode" />
            </div>
            <!--endRight Side-->
        </div>
        show: {{location}}
    <!-----------------------------------------END LOCATION---------------------------------------------->


    <!-----------------------------------------START PROFILE----------------------------------------->
        <p class="base">Profile</p>
        <div class="flex-container" v-for="(profile,k) in profile" :key="k">
            <!--LEFT SECTION-->
            <div>
                <input type="text" placeholder="Network" v-model="profile.network" />
                <input type="text" placeholder="Username" v-model="profile.username" />
            </div>
            <!--End LEFT SECTION-->

            <!--RIGHT SECTION-->
            <div>
                <input type="Phone" placeholder="URL" v-model="profile.url" />
            </div>
            <!--END RIGHT SECTION-->
        </div>
        <button @click.prevent="newProfile(k)">Profile +</button>
        <button @click.prevent="removeProfile(k)" v-show="k || ( !k && profile.length > 1)">Remove</button>
    <!------------------------------------------END PROFILE----------------------------------------->
</div>
</template>

<script>
export default {
    name: 'One',
    components: {},
    data() {
        return {
            basics: {
                name: '',
                label: '',
                image: '',
                email: '',
                phone: '',
                url: ''
            },
            location: {
                country: null,
                address: null,
                city: null,
                region: null,
                postalCode: null,
                countryCode: null,
            },
            profile: [{
                network: '',
                username: '',
                url: ''
            }]
        }
    },

    methods: {
        newProfile() {
            this.profile.push({
                network: '',
                username: '',
                url: ''
            });
        },
        removeProfile(k) {
            this.profile.splice(k, 1);
        },

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
