<template>
  <div class="containerPanel">
        <TopCross />
         <div class="panelWrap" >
                <h1 class="title text-3xl font-semibold mb-9 mt-10">Edit Member</h1>
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
          <div class="head1">Billing type</div>
          <div class="mainTextPanel"><p>Yearly</p></div>
        </div>
        <div>
          <div class="head1">Next Invoice</div>
          <div class="mainTextPanel ">9/6/2041</div>
        </div>
        <div>
          <div class="head1">Payment Method</div>
          <div class="flex flex-row">
            <visaIcon />
            <div class="mainTextPanel visacard ml-2 mr-4">****5564</div>
            <penIcon />
          </div>
        </div>
        <div>
          <div class="head1">Properties</div>
          <div class="mainTextPanel">6/10</div>
        </div>
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
  components: { },
};
</script>

<style>
.panelWrap{
  margin: 0 auto;
}
</style>
