<script>
    import TabServicesCard from "./TabServicesCard.svelte";
  
    const services = [
      {
        image: "/img/haircut.jpg",
        title: "Hair Cut",
     
      },
      {
        image: "/img/nail.jfif",
        title: "Shampoo & Blow Dry",
       
      },
      {
        image: "/img/threading.jpg",
        title: "Hair Treatment",
        
      },
      {
        image: "/img/eyelashes.avif",
        title: "Hair Rebounding",
        
      },
      {
        image: "/img/facial.jpg",
        title: "Hair Highlights",
        
      },
      {
        image: "/img/bodymassage.webp",
        title: "Hair Smoothing",
       
      },
      {
        image: "/img/bodymassage.webp",
        title: "Hair Spa",
       
      },
      {
        image: "/img/bodymassage.webp",
        title: "Hot Hair Oil Massage",
       
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
  