<script>
    import { onMount } from 'svelte';
    let news = [];
  
    onMount(async () => {
      const response = await fetch(`https://gnews.io/api/v4/search?q=carbone&lang=fr&token=677702bb48f6fb8683643401fdadc26b`);
  
      const data = await response.json();
      news = data.articles.slice(0, 8);
    });
  
    function checkImage(node) {
      node.onerror = function() {
        node.src = 'actualitesecologie.png';
      }
    }
  </script>
  
  <style>
    .news-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      justify-content: center;
      text-align: center;
      font-size: 1.5rem;
    }
  
    .news-item img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
  </style>
  
  <section class="absolute w-full top-40 news-section bg-gradient-to-r from-rose-200 " >
    <div class="py-40"><h1 class="text-4xl font-bold mb-4 text-center">Les actualités récentes sur la taxe carbone</h1></div>
    <div class="news-grid">
      {#each news as item (item.url)}
        <article class="news-item">
          <img src={item.image} alt={item.title} use:checkImage />
          <h2><a href={item.url} target="_blank">{item.title}</a></h2>
        </article>
      {/each}
    </div>
  </section>
  