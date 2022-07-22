<template>
  <div class="containerPanel ml-5 sm:ml-0">
   <TopCross/>
    
    <!-- Header of the panel -->
    <h1 class="title text-3xl font-semibold mb-9 mt-20">Edit Member</h1>
    <!-- Navigation Bar -->
    <div class="navbarPanel flex flex-row text-base space-x-6">
      <div class="elementInactive"><a>Profile</a></div>
      <div class="elementInactive"><a>Access</a></div>
      <div class="elementInactive"><a>Permissions</a></div>
      <div class="elementInactive"><a>Notifications</a></div>
      <div class="elementActive underline"><a>Billing</a></div>
    </div>
<hr class="my-4" />
 <!-- Properties -->

      <div
        class="propertiesPanel flex flex-row rounded-lg place-content-around p-3"
      >
        <div>
          <div class="head1 text-xs sm:text-sm text-gray-600">Billing type </div>
          <div class="mainTextPanel font-normal sm:font-bold"><p>Yearly</p></div>
        </div>
        <div>
          <div class="head1 text-xs sm:text-sm text-gray-600">Next Invoice</div>
          <div class="mainTextPanel font-normal sm:font-bold ">9/6/2041</div>
        </div>
        <div>
          <div class="head1 text-xs sm:text-sm text-gray-600">Payment Method</div>
          <div class="flex flex-row">
            <visaIcon />
            <div class="mainTextPanel visacard ml-2 mr-0 sm:mr-4 font-normal sm:font-bold">****5564</div>
            <penIcon />
          </div>
        </div>
        <div>
          <div class="head1 text-xs sm:text-sm text-gray-600">Properties</div>
          <div class="mainTextPanel font-normal sm:font-bold">6/10</div>
        </div>
      </div>

      <!-- Invoice List  -->
      <InvoiceList />

      <!-- Buttons -->
      <div class="buttonArea">
        <buttonArea />
      </div>



  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style>

.title {
  color: #0a0b0f;
}
.elementInactive a {
  font-weight: 500;
  color: #666666;
  cursor: pointer;
}
.elementInactive a:hover {
  color: #212121;
  text-decoration: underline;
  text-underline-offset: 20px;
}
.elementActive {
  font-weight: 500;
  color: #304ffe;
  cursor: pointer;
  text-underline-offset: 20px;
}
.propertiesPanel {
  background-color: #f3f4f6;
  max-width: 600px;
  min-width: 350px;
}
.mainPanel {
  position: relative;
  margin-top: 54px;
  left: 20%;
}

@media (max-width: 768px) {

  .propertiesPanel {
    max-width: 360px;
    margin-left: -10px;
  }

 
  .visacard{
    margin-top:1px;
  }
  .elementInactive {
    font-size: 12px;
    text-underline-offset: 22px;
  }
  .elementActive {
    font-size: 12px;
     text-underline-offset: 22px;
  }
}

</style>

</style>
