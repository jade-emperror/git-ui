<template>
    <div class="navbar-cont">
        <div class="left-cont">
            <div class="search-bar">
                <img src="../assets/gitlogo2.png">
                <input type="text" id="sbar" placeholder="Search or jump to...">
            </div>  
            <div class="nav-btns">
                <button class="nav-btn">Pull requests</button>
                <button class="nav-btn">Issues</button>
                <button class="nav-btn">Marketplace</button>
                <button class="nav-btn">Explore</button>
            </div>
        </div>
        <div class="right-cont">
            <img :src=prof_url alt="profile_pic" id="pp">
        </div>
    </div>
</template>
<script>
export default{
    name : 'NavBar',
    data(){
        return{
            prof_url:'https://avatars.githubusercontent.com/u/72389559?s=40&v=4'
        }
    }
}
</script>
<style>
.navbar-cont{
    margin: 0px;
    padding: 13px 0px;
    background-color: #161b22;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.left-cont{
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-left: 30px;
}
.search-bar{
    display: flex;
    flex-direction: row;
    align-items: center;
}
#sbar{
    margin-left: 16px;
    background-color: #0d1117;
    outline: none;
    border: solid 1px #373b42;
    padding: 7px 10px 6px 10px;
    color: rgb(193, 193, 193);
    font-size: 14px;
    width: 225px;
    border-radius: 6px;
}
#sbar::placeholder{
    color: rgb(193, 193, 193);
    font-size: 14px;
}
.nav-btns{
    margin-left: 15px;
}
.nav-btn{
    background-color: #161b22;
    border: none;
    color:#f0f6fc;
    font-weight: 600;
    margin-right: 4px;
    letter-spacing: .3px;
}
.nav-btn:hover{
    cursor: pointer;
}
#pp{
    margin-right: 30px;
    border-radius: 50%;
    height: 33px;
}
#pp:hover{
    cursor: pointer;
}
</style>