<script>
    import TabServicesCard from "./TabServicesCard.svelte";
  
    const services = [
      {
        image: "/img/threading.jpg",
        title: "Eyebrow Threading",
     
      },
      {
        image: "/img/threading.jpg",
        title: "Upper Lip Threading",
     
      },
      {
        image: "/img/threading.jpg",
        title: "Full Face Threading",
     
      },
      {
        image: "/img/threading.jpg",
        title: "Under Arm Waxing",
     
      },
      {
        image: "/img/nail.jfif",
        title: "Full Legs Waxing",
       
      },
      {
        image: "/img/threading.jpg",
        title: "Half Legs Waxing",
        
      },
      {
        image: "/img/eyelashes.avif",
        title: "Full Body Waxing",
        
      },
      {
        image: "/img/facial.jpg",
        title: "Full Hand Waxing",
        
      },
      {
        image: "/img/bodymassage.webp",
        title: "Half Hand Waxing",
       
      },
      {
        image: "/img/bodymassage.webp",
        title: "Bikini Waxing",
       
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
  