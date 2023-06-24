<script>
  import Banner from './Banner.svelte';
  import "carbon-components-svelte/css/g10.css";
  import { onMount } from 'svelte';
  onMount(() => {
    document.body.classList.add('bg');
  });

</script>

<style>
  .bg {
    background: url('/fondaquarelle.jpg') no-repeat center center fixed; 
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
  }
</style>

  <div>
    <Banner/>
    <slot />
  </div>
  