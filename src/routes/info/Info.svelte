<script>
  import Quizz from '../quizz/Quizz.svelte'; // Remplacez 'TestComponent' par le nom de votre composant Svelte

  let activeSection = null;
  let activeQuizz = false;
  function toggleSection(section) {
    activeSection = section === activeSection ? null : section;
  }
  function displayQuizz(){
    activeQuizz = true
  }
</script>

<main class="bg-gray-200 py-10">
  <div class="container mx-auto px-4">
    <div class="text-center">
      <h1 class="text-4xl font-bold mb-4">Texte principal centré</h1>
      <p class="text-lg text-gray-700">Texte plus petit en dessous</p>
    </div>
    <div class="flex justify-center mt-4">
      <div>
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => displayQuizz()}>
          TEST
        </button>
      </div>
    </div>
    <div class="flex justify-center mt-10">
      <div class="w-1/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(1)}>
          Bouton 1
        </button>
      </div>
      <div class="w-1/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(2)}>
          Bouton 2
        </button>
      </div>
      <div class="w-1/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(3)}>
          Bouton 3
        </button>
      </div>
    </div>
    {#if activeSection !== 0}
      <div class="flex justify-center mt-4">
        <div class="w-full">
          <div class="bg-white rounded-lg shadow-md p-6">
            {#if activeSection === 1}
              <div class="flex items-center">
                <img src="path_to_image_1.jpg" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 class="text-xl font-bold mb-2">Titre du cadre 1</h2>
                  <p class="text-gray-700 mb-4">Description du cadre 1</p>
                </div>
              </div>
            {/if}
            {#if activeSection === 2}
              <div class="flex items-center">
                <img src="path_to_image_2.jpg" alt="Image 2" class="w-16 h-16 mr-4">
                <div>
                  <h2 class="text-xl font-bold mb-2">Titre du cadre 2</h2>
                  <p class="text-gray-700 mb-4">Description du cadre 2</p>
                </div>
              </div>
            {/if}
            {#if activeSection === 3}
              <div class="flex items-center">
                <img src="path_to_image_3.jpg" alt="Image 3" class="w-16 h-16 mr-4">
                <div>
                  <h2 class="text-xl font-bold mb-2">Titre du cadre 3</h2>
                  <p class="text-gray-700 mb-4">Description du cadre 3</p>
                </div>
              </div>
            {/if}
          </div>
        </div>
      </div>
    {/if}
  </div>
  <div >
    
    {#if activeQuizz === true}
      <Quizz /> <!-- Remplacez 'TestComponent' par le nom de votre composant Svelte -->
    {/if}
  </div>
</main>
