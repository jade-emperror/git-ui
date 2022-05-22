<template>
    <div class="profile-cont">
        <div class="img-sec">
            <img :src=prof_url id="profilesecp" alt="">
        </div>
        <div class="desc-sec">
            <span class="uname">{{ usr_name }}</span>
            <button class="edit">Edit profile </button>
            <span class="followlist">
                <span class="count"> {{ followers }}</span> followers <span class="count">· {{ following }}</span>  following
            </span>
        </div>
        <div class="highlight-sec">
            <span id="highlight-title">Highlights</span>
            <div class="highlight-tags">
                <span v-for="tag in tags" :key='tag' :class=tag.color>{{ tag.tag_name }}</span>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    name : 'ProfileSection',
    data(){
        return{
            prof_url:'https://avatars.githubusercontent.com/u/72389559?v=4',
            usr_name:'jade-emperror',
            followers:500,
            following:5,
            tags:[
                {tag_name:'pro',color:'tag tag1'},
                {tag_name:'staff',color:'tag tag2'},
                {tag_name:'GitHub Sponsor',color:'tag tag3'},
            ]
        }
    }
}
</script>
<style>
.profile-cont{
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: center;
}
#profilesecp{
    border-radius: 50%;
    height: 275px;
    margin-top: -25px;
}
.desc-sec{
    width: 275px;
    display: flex;
    flex-direction: column;
    border-bottom: solid 1.5px #21262d;
}
.uname{
    font-size: 20px;
    font-weight: 100;
    color: #585f67;
    font-family: Arial, Helvetica, sans-serif;
    padding: 11px 0px;
}
.edit{
    background: #21262d;
    outline: none;
    border: solid 1.5px #737475;
    font-size: 15px;
    padding: 5px 0px;
    border-radius: 7px;
    color: #c9cdd4;
}
.followlist{
    font-family: Arial, Helvetica, sans-serif;
    padding: 17px 0px;
    color: #585f67;
    font-size: 14px;
    margin-bottom: 12px;
}
.count{
    color:#c9cdd4;
    font-size: 15px;
}
.highlight-sec{
    width: 275px;
    font-family: Arial, Helvetica, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding-bottom: 20px;
}
#highlight-title{
    color: #c3cbd3;
    font-size: 17px;
    font-weight: bold;
    padding: 15px 0px 0px 0px;
}
.highlight-tags{
    margin-top: 13px;
}
.tag{
    text-transform: uppercase;
    margin-right: 6px;
    font-size: 13px;
    padding: 4px 7px;
    border-radius: 17px;
}
.tag1{
    color: #8957e5;
    border: solid 1px #8957e5;
}
.tag2{
    color: #57e578;
    border: solid 1px #57e578;
}
.tag3{
    color: #57d2e5;
    border: solid 1px #57d2e5;
}
</style>