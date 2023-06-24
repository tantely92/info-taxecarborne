<script>
  let showDropdown_info = false;
  let showDropdown_inspi = false;
  let showDropdown_agir = false;
</script>
<div class="fixed top-0 w-full z-10 h-40 bg-cover bg-repeat self-auto flex items-center border-double border-4 border-green-600 outline outline-offset-2 outline-2" style="background-image: url('fondaquarelle.jpg');">
  <div class="container mx-auto px-4 flex items-center justify-center placeholder:">
    <div>
      <a href="/" >
        <img  src="logo2.png" alt="Logo" class="w-28 h-28 rounded-full border-2 border-blue-500 overflow-hidden" >
      </a>
    </div>
    <div class="container mx-auto px-4 flex items-center justify-center">
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_info = true}" on:mouseleave="{() => showDropdown_info = false}">
        <a href="/info" class="inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200"
           >
          S'informer
        </a>
        {#if showDropdown_info}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded fade-in" >
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-blue-200">TESTEZ VOS CONNAISSANCES</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-blue-200">Différents types de tarification carbone</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-blue-200">Historique récent en France</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-blue-200">Fonctionnement en France</a>
          </div>
        {/if}
      </div>
      
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_inspi = true}" on:mouseleave="{() => showDropdown_inspi = false}">
        <a href="/bouton2" class="inline-block bg-green-500 hover:bg-green-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200"
           >
          S'inspirer
        </a>
        {#if showDropdown_inspi}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded fade-in"
            on:mouseover="{() => showDropdown_inspi = true}" on:mouseleave="{() => showDropdown_inspi = false}">
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-green-200">...des économistes environnementaux</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-green-200">...des économistes écologiques</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-green-200">...du monde de l'entreprise</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-green-200">...de la sphère politique</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-green-200">...des ONG</a>
          </div>
        {/if}
      </div>

      <div class="relative inline-block" on:mouseenter="{() => showDropdown_agir = true}" on:mouseleave="{() => showDropdown_agir = false}">
        <a href="/bouton3" class="inline-block bg-orange-500 hover:bg-orange-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200"
           >
          Agir
        </a>
        {#if showDropdown_agir}
          <div class="absolute bg-white mt-2 py-2 w-48 shadow-lg rounded fade-in"
            on:mouseover="{() => showDropdown_agir = true}" on:mouseleave="{() => showDropdown_agir = false}">
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-orange-200">...selon différents axes</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-orange-200">...en entreprise</a>
            <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-orange-200">VOS SUGGESTIONS</a>
          </div>
        {/if}
      </div>

      <a href="/bouton4" class="inline-block bg-rose-500 hover:bg-rose-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200">Actualités</a>
      <a href="/bouton5" class="inline-block bg-violet-500 hover:bg-violet-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200"> Contact</a>
    </div>
  </div>
</div>




  
  
  
<style>
    
  @import 'tailwindcss/tailwind.css';
  .background {
    background-image: url('fondaquarelle.jpg'); 
  }
  
  @keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
  }

  .fade-in {
    animation: fadeIn .5s ease-in-out;
  }



</style>