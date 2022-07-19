<template>
  <div class="sidebarArea">
    <div class="container ">
        <br/>
    </div>

    <div class="iconArea">
<LogoIcon />
    </div>

 <div class="textArea ">
<div class="activeSelector"><ArrowIcon/></div>
<div class="inactiveSelector"><HousesIcon/></div>
<div class="inactiveSelector"><LeadsIcon/></div>
<div class="inactiveSelector"><MailsIcon/></div>
<div class="inactiveSelector"><FolderIcon/></div>
<div class="inactiveSelector"><CirclesIcon/></div>
<div class="inactiveSelector"><PeopleIcon/></div>

    </div>

 <div class="fotoArea ">
<img src ="https://www.diethelmtravel.com/wp-content/uploads/2016/04/bill-gates-wealthiest-person.jpg" alt="Avatar" class="avatarIcon "></img>
    </div>
  </div>
</template>

<script>



export default {
  components: { },
 
};
</script>

<style>
.iconArea{
    margin-top: -5px;
    margin-bottom: 10px;
}

.sidebarArea {
  background-color: #0a0b0f;
  height: 100vh;
  width: 80px;
  position: absolute;
  top: 0
}

.avatarIcon{
    border-radius: 5px;
    height: 40px;
    width: 40px;
}

.activeSelector{
    margin-top: 100px;
    background-color: #304FFE;
     width: 80px;
    height: 80px;
    cursor: pointer;
}

.activeSelector:hover{

    background-color: #516bff;

}
.inactiveSelector{
    width: 80px;
    height: 80px;
  border-top: 1px solid #333333;
    background: #0A0B0F;


}

.inactiveSelector:hover{
 cursor: pointer;
    background: #333333;
    
}
h1{
    color: white;
}
/* Smartphones (portrait) ----------- */
/* @media only screen and (max-width: 620px) {
  .sidebarArea {
    display: none;
  }
} */

@media (max-width: 768px) { 
   .sidebarArea {
    display: none;
  }
}
.fotoArea{

 position: absolute;
    left: 20px;
    bottom: 3%;
}

@media (max-height: 800px) { 
   .fotoArea {
    display: none;
  }
}
</style>
