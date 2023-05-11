<template>
    <div class="appbar">
        <!-- <h1>Ajio</h1> -->
        <!-- <hr class="hrtag"/> -->
        <img  id='ajioImage' width="130px" src="https://assets.ajio.com/static/img/Ajio-Logo.svg" />    
        <a class="signin" href="">Sign In/Join AJIO</a>  
        <a class="customercare" href="">Customer Care</a>
        <button class="visitAjioLuxe">Visit AJIOLUXE</button>
        <input class="searchBar"  placeholder="Search AJIO" type="text" value=""/>
        <img class= "wishlist" src="https://assets.ajio.com/static/img/wishlistIcon.svg" alt="wishlistIcon"/>
         <ul class="listItem">
            <li ><a href="">Men</a></li>
            <li ><a href="">Women</a></li>
            <li ><a href="">Kids</a></li>
            <li ><a href="">Indie</a></li>
            <li ><a href="">Home & Kitchen</a></li>
        </ul>
    </div>
</template>
<script>
export default{
    name:'AppBar'

};
</script>

<style>
.appbar{
   
    /* background-color:#FFFFFF;
    height: 80px; */
    width: 100%;
    border-top: 3px solid #2c4152;
    z-index: 101;
    background-color: #fff;
    border-bottom: 1px solid #e0e0e0;
    position: fixed;
    font-family: SourceSansPro;
    top: 0;
    height: 80px;
    margin-left: -10px;
    box-shadow: 0 3px 6px 0 rgba(0,0,0,.2);
}


#ajioImage{
    width: 120px;
    margin-top: 20px;
    height: 50px;
    margin-left: 40px;
    position: absolute;
    /* margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
    border-radius: 0;
    vertical-align: middle;
    overflow-clip-margin: content-box;
    overflow: clip; */
}
.listItem {
  display: flex;
  justify-content: center;
  margin-left: 40px;
  list-style: none;
  text-align: center;

}
.listItem li {
  margin-left: 10px;
  font-family: 'SourceSansPro';
  margin-top: 40px;
  text-transform: uppercase;
  padding: 0 8px;
  font-size: 14px;
   text-decoration: none;
    color: rgb(51, 51, 51);
  /* 
  display: flex;
  justify-content: center;
  position: relative;
  font-size: 16px; */
  /* transition: all .2s ease-in-out; */
  /* color: rgb(51, 51, 51);
    height: 40px;
    font-size: 16px; */
   
}
/* .listItem li a{
   transition: all .2s ease-in-out;
    
    color: rgb(51, 51, 51);

} */
.listItem li a:hover{
    /* transition: all .2s ease-in-out; */
    font-weight: bold;
    text-decoration: none;
    color: rgb(51, 51, 51);
}

.signin{
    text-decoration: underline;
    color: #406786;
    cursor: pointer;
    letter-spacing: .1em;
    font-size: 12px;
    text-transform: capitalize;
    margin-left:825px;
    position: absolute;
    transition: all .2s ease-in-out;
}
.customercare{
    text-decoration: underline;
    color: #406786;
    cursor: pointer;
    letter-spacing: .1em;
    font-size: 12px;
    text-transform: capitalize;
    margin-left: 940px;
    position: absolute;
}
.visitAjioLuxe{
    
    color: #FFFFFF;
    background-color: black;
    cursor: pointer;
    letter-spacing: .1em;
    font-size: 10px;
    text-transform: capitalize;
    margin-left: 1040px;
    position: absolute;
    height: 30px;
    margin-top: 0px;
}
.searchBar{
    font-family: Helvetica,sans-serif;
    font-weight: 30;
    border: 1px solid #2c4152;
    border-radius: 17px;
    width: 20%;
    margin-top: 50px;
    background-color: #fffded;
    box-shadow: inset 0 1px 1px rgba(0,0,0,.075);
    height: 25px;
    font-size: 14px;
    position: absolute;
    margin-left: 850px;

}
.wishlist{
    margin-top: 47px;
    margin-left: 1105px;
    position: absolute;
}
</style>    