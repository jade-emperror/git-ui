<template>
    <div class="overview-cont">
        <div class="toppin-sec">
            <span class="pinned">Pinned</span>
            <span class="customisedpin">Customize your pin</span>
        </div>
        <div class="tabs-sec">
            <div class="tab-sec" v-for="tab in tabs" :key="tab.name">
                <div class="tab-desc">
                    <div class="tab-title">
                        <span class="tabtitle">{{ tab.name }}</span>
                        <span class="scope">{{tab.scope}}</span>
                    </div>
                    <span class="tabdesc">{{ tab.desc }}</span>
                </div>
                <div class="tech-desc">
                    <span :class=tab.color>&nbsp;&nbsp;&nbsp;&nbsp;</span>      
                    <span class="tab-tech">{{tab.tech}}</span> 
                </div>
            </div>
        </div>
    </div>
</template>
<script>

export default{
    name:'OverView',
    data(){
        return{
            tabs:[
                {
                    'name':'Gluetone',
                    'scope':'public',
                    'desc':'Glutone - Stock Price Prediction',
                    'tech':'CSS',
                    'color':'purple',
                },
                {
                    'name':'HEM',
                    'scope':'public',
                    'desc':'HEM - Happy Event Management is a static web page for an imaginary event mangement company.',
                    'tech':'HTML',
                    'color':'orange',
                },
                {
                    'name':'learning-management-system',
                    'scope':'public',
                    'desc':'learning management system is a web application constructed with DJANGO framework. The sole purpose of the LMS is to fetch learning material from internet for the desired topic.',
                    'tech':'Python',
                    'color':'skyblue',
                }
            ],
        }
    }
}
</script>
<style>
.overview-cont{
    display: flex;
    flex-direction: column;
    width: 60vw;
    font-family: Arial, Helvetica, sans-serif;

}
.toppin-sec{
    margin-top: 30px;
    display: flex;
    justify-content: space-between;
}
.pinned{
    color:#c9d1d9;
}
.customisedpin{
    color:#6d7a75;
    font-size: 12px;
}
.tabs-sec{
    margin-top: 10px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.tab-sec{
    padding: 20px 10px 15px 15px;
    border: solid 1px #3e3d3d;
    border-radius: 10px;
    max-width: 27.5vw;
    width: 28.5vw;
    margin-bottom: 13px;
}
.tab-title{
    display: flex;
    flex-direction: row;
    align-items: center;
}
.tabtitle{
    color: #3888ea;
}
.scope{
    color: #6d7a75;
    border: solid 1px #6d7a75;
    border-radius: 10px;
    font-size: 12px;
    padding: 3px 7px;
    margin-left: 5px;
}
.tabdesc{
    color: #6d7a75;
    margin-top: 13px;
    font-size: 13px;
}
.purple{
    border-radius: 50%;
    background-color: rebeccapurple;
    margin-right: 3px;
}
.orange{
    border-radius: 50%;
    background-color: rgb(212, 137, 38);
    margin-right: 3px;
}
.skyblue{
    border-radius: 50%;
    background-color: rgb(38, 116, 212);
    margin-right: 3px;
}
.tab-tech{
    color: #c9d1d9;
    font-size: 14px;
}
.tech-desc{
    margin-top: 20px;
    font-size: 12px;
}
</style>