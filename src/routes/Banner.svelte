<script>
  let showDropdown_info = false;
  let showDropdown_inspi = false;
  let showDropdown_agir = false;
</script>
<div class="fixed top-0 w-full z-50 h-40 bg-cover bg-repeat self-auto flex items-center border-double border-4 border-green-600 outline outline-offset-2 outline-2" style="background-image: url('fondaquarelle.jpg');">
  <div class="container mx-auto px-4 flex items-center justify-between">
    <div>
      <a href="/" >
        <img src="logo2.png" alt="Logo" class="w-12 h-12 sm:w-20 sm:h-20 md:w-28 md:h-28 lg:w-28 lg:h-28 xl:w-28 xl:h-28 rounded-full border-2 border-blue-500" >

      </a>
    </div>
    <div class="flex items-center justify-center">
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_info = true}" on:mouseleave="{() => showDropdown_info = false}">
        <a href="/info" class=" bg-blue-500 hover:bg-blue-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200">
          S'informer
        </a>
      </div>
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_inspi = true}" on:mouseleave="{() => showDropdown_inspi = false}">
        <a href="/bouton2" class=" bg-green-500 hover:bg-green-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200">
          S'inspirer
        </a>
      </div>
      <div class="relative inline-block" on:mouseenter="{() => showDropdown_agir = true}" on:mouseleave="{() => showDropdown_agir = false}">
        <a href="/bouton3" class=" bg-orange-500 hover:bg-orange-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200">
          Agir
        </a>
      </div>
      <a href="/bouton4" class=" bg-rose-500 hover:bg-rose-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200">Actualités</a>
      <a href="/bouton5" class=" bg-violet-500 hover:bg-violet-600 text-white font-bold rounded-full mx-4 flex items-center justify-center w-24 h-24 shadow-2xl transform hover:scale-105 transition-transform duration-200"> Contact</a>
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