<template>
  <div containerPanel>
    <h1 class="title text-3xl font-semibold	mb-9	">Edit Member</h1>

    <!-- Navigation Bar -->
    <div class="navbarPanel flex flex-row space-x-8 text-base ">
      <div class="elementInactive"><a>Profile</a></div>
      <div class="elementInactive"><a>Access</a></div>
      <div class="elementInactive"><a>Permissions</a></div>
      <div class="elementInactive"><a>Notifications</a></div>
      <div class="elementActive underline"><a>Billing</a></div>
    </div>
<hr class="my-4"/>
    <!-- Properties -->

    <div class="propertiesPanel flex flex-row rounded-lg place-content-around text-xs p-3 ">
      <div>
        <div>Billing type</div>
        <div class="mainTextPanel text-lg"><p>Yearly</p></div>
      </div>
      <div>
        <div>Next Invoice</div>
        <div class="mainTextPanel text-lg">9/6/2041</div>
      </div>
      <div>
        <div>Payment Method</div>
        <div class="flex flex-row" ><visaIcon/><div class="mainTextPanel text-lg">****5564</div><penIcon/></div>
        
      </div>
      <div>
        <div>Properties</div>
        <div class="mainTextPanel text-lg">6/10</div>
      </div>
      
    </div>

    <!-- Invoice List  -->
    <InvoiceList />

    <!-- Buttons -->
<div class="buttonArea">
    <buttonArea/>
</div>
  </div>
</template>

<script>


export default {
  components: { },
};
</script>

<style>
.title{
    color: #0A0B0F;
}

.elementInactive a {
  font-weight: 500;
  color: #666666;
  cursor: pointer;
}

.elementInactive a:hover {
  color: #212121;
}

.elementActive {
  font-weight: 500;
  color: #304ffe;
}

.propertiesPanel{
    background-color: #F3F4F6;
    max-width: 600px;

}



</style>



