<script>
  import Banner from './Banner.svelte';
  import "carbon-components-svelte/css/g10.css";


</script>

  <div class="maine">
    <Banner/>
    <slot />
    
  </div>
  
  <style>
    @import 'tailwindcss/tailwind.css';
    
  </style>