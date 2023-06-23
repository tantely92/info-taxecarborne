<script>
    import { onMount } from 'svelte';
    let news = [];
  
    onMount(async () => {
      const response = await fetch(`https://gnews.io/api/v4/search?q=carbone&lang=fr&token=677702bb48f6fb8683643401fdadc26b`);

      const data = await response.json();
      news = data.articles.slice(0, 8);
    });
  </script>
  
  <section class="news-section">
    <h1>Les actualités récentes sur la taxe carbone</h1>
    <div class="news-grid">
      {#each news as item (item.url)}
        <article class="news-item">
          <img src={item.image} alt={item.title} />
          <h2><a href={item.url} target="_blank">{item.title}</a></h2>
        </article>
      {/each}
    </div>
  </section>
  