<template>
  <div class="sidebarArea">
    

    <div class="iconArea">
<LogoIcon />
    </div>

 <div class="textArea">
<div class="activeSelector"><ArrowIcon/></div>
<div class="inactiveSelector"><HousesIcon/></div>
<div class="inactiveSelector"><LeadsIcon/></div>
<div class="inactiveSelector"><MailsIcon/></div>
<div class="inactiveSelector"><FolderIcon/></div>
<div class="inactiveSelector"><h1>gñe</h1></div>
<div class="inactiveSelector"><h1>gñe</h1></div>

    </div>

 <div class="fotoArea">
<img src="https://www.diethelmtravel.com/wp-content/uploads/2016/04/bill-gates-wealthiest-person.jpg" alt="Avatar" class="avatarIcon "></img>
    </div>
  </div>
</template>

<script>
import FolderIcon from "./folderIcon.vue";


export default {
  components: { FolderIcon },
 
};
</script>

<style>
.sidebarArea {
  background-color: #0a0b0f;
  height: 100vh;
  width: 80px;
}

.avatarIcon{
    border-radius: 5px;
    height: 40px;
    width: 40px;
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
@media only screen and (max-width: 620px) {
  .sidebarArea {
    /* background-color: #0A0B0F; */
    display: none;
  }
}
</style>
