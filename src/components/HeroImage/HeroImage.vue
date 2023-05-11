<template>
    <div class="main_div">
        <div>
            <img class="hero_image" src="https://cdn.pixelbin.io/v2/falling-surf-7c8bb8/fyndnp/wrkr/addsale/company/13807/applications/6405af0c0cf857073a63aaee/theme/pictures/free/original/theme-image-1683019171733.png"/>
        </div>
        <div class="para">
            <p class="heading">
                NEXT GENERATION OF DENIM 
            </p>
            <p class="sub_heading">
                JUST LAUNCHED 2023 COLLECTION 
            </p>
        </div>
        <div class="buttons">
            <Button class="men">
                DISCOVER MEN
            </Button>
            <Button class="women">
                DISCOVER WOMEN
            </Button>
        </div>
   </div>
</template>

<script>
    export default{
        name: 'HeroImage'
    }
</script>

<style>
.hero_image{
    width: 100%;
   
}
.heading{
    position: absolute;
    top: 0;
    font-weight: 600;
    margin-top: 520px;
    margin-left: 480px;
    font-size: 72px;
    padding: 0 0.5px;
    font-style: normal;
    text-shadow: 0px 10px 24px rgba(0, 0, 0, 0.5);
    line-height: 130%;
    color: white;
    word-break: break-word;
    word-wrap: break-word;
    display: block;
    text-align: right;
}
.sub_heading{
    position: absolute;
    top: 0;
    font-weight: 600;
    margin-top: 610px;
    margin-left: 900px;
    font-size: 36px;
    padding: 0 0.5px;
    font-style: normal;
    text-shadow: 0px 10px 24px rgba(0, 0, 0, 0.5);
    line-height: 130%;
    color: white;
    word-break: break-word;
    word-wrap: break-word;
    display: block;
    text-align: right;
}
.men{
    font-weight: 600 !important;
    line-height: 130% !important;
    border: none;
    top: 0;
    align-items: center;
    font-size: 16px;
    width: 180px;
    height: 48px;
    margin-top: 730px;
    margin-left: 1060px;
    position: absolute;
}
.men:hover{
    background: transparent;
    color: #ffffff;
    border: 1px solid #ffffff;
}
.women:hover{
    background: transparent;
    color: #ffffff;
    border: 1px solid #ffffff;
}
.women{
    font-weight: 600 !important;
    line-height: 130% !important;
    border: none;
    top: 0;
    align-items: center;
    font-size: 16px;
    width: 180px;
    height: 48px;
    margin-top: 730px;
    margin-left: 1260px;
    position: absolute;
}
</style>