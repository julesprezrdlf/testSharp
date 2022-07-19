<template>
  <div class="containerPanel">
    <TopCross />
    <div class="mainPanel">
      <h1 class="title text-3xl font-semibold mb-9 mt-10">Edit Member</h1>

      <!-- Navigation Bar -->
      <div class="navbarPanel flex flex-row  text-base space-x-6 ">
        <div class="elementInactive"><a>Profile</a></div>
        <div class="elementInactive"><a>Access</a></div>
        <div class="elementInactive"><a>Permissions</a></div>
        <div class="elementInactive"><a>Notifications</a></div>
        <div class="elementActive underline"><a>Billing</a></div>
      </div>
      <hr class="my-4" />
      <!-- Properties -->

      <div
        class="propertiesPanel flex flex-row rounded-lg place-content-around text-xs p-3"
      >
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
          <div class="flex flex-row">
            <visaIcon />
            <div class="mainTextPanel text-lg ml-2 mr-4">****5564</div>
            <penIcon />
          </div>
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
        <buttonArea />
      </div>
    </div>
  </div>
</template>

<script>
import TopCross from "./topCross.vue";
export default {
  components: { TopCross },
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
}

.mainPanel {
  position: relative;
  margin-top: 54px;
  left: 20%;
}

@media (max-width: 640px) {
  .mainPanel {
    position: relative;
    margin-top: 54px;
    left: 1%;
  }
}

@media (max-width: 768px) {
  .mainPanel {
    position: relative;
    margin-top: 54px;
    left: 5%;
  }

  .propertiesPanel{
    max-width: 500px;
  }

  .navbarPanel{
font-size: 10px;
  }
  

  .elementInactive{
    
    font-size: 12px;
  }

  .elementActive{
    
    
    font-size: 12px;
 
  }
}

@media (max-width: 1100px) {
  .mainPanel {
    position: relative;
    margin-top: 54px;
    left: 12%;
  }
}
</style>
