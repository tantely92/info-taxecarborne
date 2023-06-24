<script>
  let showDropdown_info = false;
  let showDropdown_inspi = false;
  let showDropdown_agir = false;
</script>
<div class="bg-gray-200 py-4">
  <div class="container mx-auto px-4 flex items-center justify-between">
    <div>
      <a href="/">
        <img  src="logo2.png" alt="Logo" class="h-23 ">
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
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">TESTEZ VOS CONNAISSANCES</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Différents types de tarification carbone</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Historique récent en France</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">Fonctionnement en France</a>
          </div>
        {/if}
      </div>
      
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_inspi = true}" on:mouseleave="{() => showDropdown_inspi = false}">
        <a href="/bouton2" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1"
           >
          S'inspirer
        </a>
        {#if showDropdown_inspi}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded"
            on:mouseover="{() => showDropdown_inspi = true}" on:mouseleave="{() => showDropdown_inspi = false}">
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...des économistes environnementaux</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...des économistes écologiques</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...du monde de l'entreprise</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...de la sphère politique</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...des ONG</a>
          </div>
        {/if}
      </div>

      <div class="relative inline-block" on:mouseenter="{() => showDropdown_agir = true}" on:mouseleave="{() => showDropdown_agir = false}">
        <a href="/bouton3" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1"
           >
          Agir
        </a>
        {#if showDropdown_agir}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded"
            on:mouseover="{() => showDropdown_agir = true}" on:mouseleave="{() => showDropdown_agir = false}">
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...selon différents axes</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">...en entreprise</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-200">VOS SUGGESTIONS</a>
          </div>
        {/if}
      </div>

      <a href="/bouton4" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">Actualités</a>
      <a href="/bouton5" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mx-1">Nous contacter</a>
    </div>
  </div>
</div>




  
  
  
<style>
    @import 'tailwindcss/tailwind.css';
</style>