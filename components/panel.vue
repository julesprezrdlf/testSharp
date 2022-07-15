<template>
  <div containerPanel>
    <h1 class="text-blue-600">Edit Member</h1>

    <!-- Navigation Bar -->
    <div class="navbarPanel flex flex-row space-x-8 text-base">
      <div class="elementInactive"><h2>Profile</h2></div>
      <div class="elementInactive"><h2>Access</h2></div>
      <div class="elementInactive"><h2>Permissions</h2></div>
      <div class="elementInactive"><h2>Notifications</h2></div>
      <div class="elementActive underline"><h2>Billing</h2></div>
    </div>

    <!-- Properties -->

    <div class="propertiesPanel flex flex-row rounded-lg place-content-around text-xs p-3">
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
        <div class="mainTextPanel text-lg">****5564</div>
      </div>
      <div>
        <div>Properties</div>
        <div class="mainTextPanel text-lg">6/10</div>
      </div>
    </div>

    <!-- Invoice List  -->
    <InvoiceList />

    <!-- Buttons -->

  </div>
</template>

<script>
import InvoiceList from "./invoiceList.vue";
export default {
  components: { InvoiceList },
};
</script>

<style>

.elementInactive h2 {
  font-weight: 500;
  color: #666666;
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



