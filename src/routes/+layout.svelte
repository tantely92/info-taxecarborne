<script>
  import Banner from './Banner.svelte';
  import "carbon-components-svelte/css/g10.css";
  import { fade } from 'svelte/transition'

  export let data


</script>

  <div class="maine">
    <Banner/>
    {#key data.pathname}
      <div  in:fade={{ duration: 200, delay: 300 }}
            out:fade={{ duration: 200 }}>
        <slot />
      </div>
    {/key}
    
  </div>
  
  <style>
    @import 'tailwindcss/tailwind.css';
    
  </style>