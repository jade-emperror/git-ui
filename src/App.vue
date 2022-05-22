<template>
  <div id="app">
    <NavBar />
    <div class="menu-cont">
      <button @click="activate('OverView')" class="menu-btn">Overview</button>
      <button @click="activate('RepositoryVue')" class="menu-btn">Repositories</button>
      <button @click="activate('ProjectVue')" class="menu-btn">Projects</button>
      <button @click="activate('PackagesVue')" class="menu-btn">Packages</button>
      <button @click="activate('StarsVue')" class="menu-btn">Stars</button>
    </div>
    <div class="main-cont">
      <div class="left-sec">
        <ProfileSection />
      </div>
      <div class="right-sec">
        <OverView v-if="this.activecomp=='OverView'" />
        <RepositoryVue v-else-if="this.activecomp=='RepositoryVue'">
          Slot is Used -
          here i used slot for the title
        </RepositoryVue>
        <ProjectVue v-else-if="this.activecomp=='ProjectVue'" title-cont="Props - i used props in this componenet." msg-cont="i used two props one for the title and other for the msg" />
        <BoredVue v-else />    
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from './components/nav.vue'
import ProfileSection from './components/profile.vue'
import OverView from './components/overview.vue'
import RepositoryVue from './components/repository.vue'
import ProjectVue from './components/project.vue'
import BoredVue from './components/bored.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    ProfileSection,
    OverView,
    RepositoryVue,
    ProjectVue,
    BoredVue,
  },
  data(){
    return{
      activecomp:"OverView",
      propMsg:'',
    }
  },
  methods:{
    activate(str){
      this.activecomp=str;
    },
  }
}
</script>

<style>
body{
  margin: 0px;
}
.menu-cont{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  background-color: #0d1117;
  border-bottom:solid 1px #373b42;
}
.menu-btn{
  background-color:#0d1117 ;
  outline: none;
  border: none;
  color: #bcbcb8;
  font-size: 15.3px;
  margin: 25px 6px 10px 0px;
  padding: 5px 10px;
}
.menu-btn:hover{
  background-color: #373b42;
  border-radius: 5px;
}
.main-cont{
    background-color: #0d1117;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
}
.left-sec{
  margin-left: 170px;
}
</style>
