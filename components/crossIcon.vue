<template>
  <div class="containerCrossed place-content-end">
    
    <svg
      class="cross-svg"
      width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M14.6554 0L0 14.6554L1.34459 16L16 1.34459L14.6554 0Z" fill="#111111"/>
<path d="M16 14.6554L1.34459 0L0 1.34459L14.6554 16L16 14.6554Z" fill="#111111"/>
</svg>
  </div>
</template>

<script>
export default {
  name: "MySVGComponent",
};
</script>

<style scoped>
.containerCrossed{
  position: absolute;
  left: 80%;
  top: 2%
}

@media (max-width: 1100px) { 
  .containerCrossed{

  left: 95%;
 
}
}

</style>
