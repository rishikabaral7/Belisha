<script>
    import TabServicesCard from "./TabServicesCard.svelte";
  
    const services = [
      {
        image: "/img/eyelashes.avif",
        title: "Natural Eyelash Extensions",
     
      },
      {
        image: "/img/nail.jfif",
        title: "Doll Eye Eyelash Extensions",
       
      },
      {
        image: "/img/threading.jpg",
        title: "Cat Eye Eyelash Extensions",
        
      },
      {
        image: "/img/eyelashes.avif",
        title: "3D Eyelash Extensions",
        
      },
      {
        image: "/img/facial.jpg",
        title: "4D Eyelash Extensions",
        
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
  