<template>
    <div class="bored-vue">
        <button id="bbtn" @click="getActivity()">I'm Bored</button>
        <div class="bored-activity">
            <h3 class="title">Heres what you have to do:</h3>
            <span class="qn">Activity:</span><span class="ans">{{ this.activity }}</span><br>
            <span class="qn">No of participants required:</span><span class="ans">{{ this.participants }}</span><br>
            <span class="qn">Accessibility of the activity:</span><span class="ans">{{ this.accessibility }}</span><br>
            <span class="qn">Cost required:</span><span class="ans">{{ this.price }}</span><br>
            <span class="qn">Genere of the Activity:</span><span class="ans">{{ this.type }}</span><br>
            <span class="qn">Link:</span><span class="ans">{{ this.link }}</span><br>
        </div>
    </div>
</template>
<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)
export default{
    name:'BoredVue',
    data(){
        return{
            "api":'https://www.boredapi.com/api/activity',
            "activity":"",
            "type":"",
            "participants":null,
            "price":null,
            "link":"",
            "key":"",
            "accessibility":null
        }
    },
    methods:{
        getActivity(){
            this.axios.get(this.api).then((response) => {
            this.activity=response.data.activity;
            this.accessibility=response.data.accessibility;
            this.link=response.data.link;
            this.participants=response.data.participants;
            this.price=response.data.price;
            this.type=response.data.type;
            })
        }
    }
}
</script>
<style>
#bbtn{
    border-radius: 50%;
    height: 70px;
    outline: none;
    background: rgb(255, 118, 118);
    border: none;
    margin: 40px 0px 10px 50px;
}
.qn{
    color: #bcbcb8;
}
</style>