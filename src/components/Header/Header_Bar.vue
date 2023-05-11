<template>
    <div class="main_div">
        <div>
            
        </div>
        <div class="sub_div">Div 1</div>
        <div class="sub_div">Div 2
                <div class="subdiv_div2">
                        <ul class="items">
                        <li>Div 2.1</li>
                        <li>Div 2.2</li>
                        <li>Div 2.3</li>
                </ul>
                </div>
             
        </div>
        <div class="sub_div">Div 3</div>
        <div class="sub_div">Div 4</div>
        <div class="sub_div">Div 5</div>
    </div>
</template>

<script>
export default{
    name: 'HeaderBar',
}


</script>

<style lan="less" scoped>
.main_div{
background-color: #FFFFFF;
display: flex;
/* height: 80px; */
}

.sub_div{
     align-items: center;
     /* border-color: #FF0000; */
     color: cadetblue;
     /* display: inline-block; */
     display: flex;
     /* width: 100px;
     height: 50px; */
     /* text-align: center; */

     padding: 10px;     
     justify-content: center;
     border : 1px solid #FF0000;
}
.sub_div:hover .subdiv_div2 .items {
    display: block;
    text-align: left;
    position: absolute;
    left: 0;
    margin-left: 1090px;
    margin-top: 20px;
    list-style-type: none;
}

.items{
    display: none;      
}
</style>