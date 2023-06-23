<script>
  let showDropdown_info = false;
  let showDropdown_inspi = false;
</script>
<div class="bg-gray-200 py-4">
  <div class="container mx-auto px-4 flex items-center justify-between">
    <div>
      <a href="/">
        <img src="logo.png" alt="Logo" class="h-8">
      </a>
    </div>
    <div class="flex items-center">
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_info = true}" on:mouseleave="{() => showDropdown_info = false}">
        <a href="/info" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1"
           >
          S'informer
        </a>
        {#if showDropdown_info}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded"
            on:mouseover="{() => showDropdown_info = true}" on:mouseleave="{() => showDropdown_info = false}">
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Lien 1</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Lien 2</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Lien 3</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Lien 4</a>
          </div>
        {/if}
      </div>
      
      <a href="/bouton2" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">S'inspirer</a>
      <a href="bouton3" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">Agir</a>
      <a href="/bouton4" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">Actualités</a>
      <a href="/bouton5" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">Nous contacter</a>
    </div>
  </div>
</div>




  
  
  
<style>
    @import 'tailwindcss/tailwind.css';
</style>