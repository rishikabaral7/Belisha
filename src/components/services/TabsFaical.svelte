<script>
    import TabServicesCard from "./TabServicesCard.svelte";
  
    const services = [
      {
        image: "/img/facial.jpg",
        title: "Hydra Facial",
     
      },
      {
        image: "/img/nail.jfif",
        title: "Gold Facial",
       
      },
      {
        image: "/img/threading.jpg",
        title: "Four Layer Facial",
        
      },
      {
        image: "/img/eyelashes.avif",
        title: "Normal Facial",
        
      },
      {
        image: "/img/facial.jpg",
        title: "Ayurvedic Facial",
        
      },
      {
        image: "/img/bodymassage.webp",
        title: "Face Cleansing",
       
      }
    ];
  </script>
  
  <section class="py-12 px-4 lg:px-40 bg-lightFigma">
  
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each services as service}
        <TabServicesCard {...service} />
      {/each}
    </div>
  </section>
  