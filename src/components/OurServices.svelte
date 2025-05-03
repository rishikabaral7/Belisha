<script>
  import ServiceCard from "./ServiceCard.svelte";

  const services = [
    {
      image: "/img/haircut.jpg",
      title: "Hair Services",
      description: "Perfect cut with a silky smooth blowout.",
    },
    {
      image: "/img/nail.jfif",
      title: "Nail Services",
      description: "Shiny, chip-free gel polish for 2+ weeks.",
    },
    {
      image: "/img/threading.jpg",
      title: "Hair Removal",
      description: "Gentle, long-lasting hair removal for smooth skin.",
    },
    {
      image: "/img/eyelashes.avif",
      title: "Eyelash Services",
      description: "Beautiful, fuller lashes with expert lifts, tints, and extensions.",
    },
    {
      image: "/img/facial.jpg",
      title: "Facial Treatments",
      description: "Deep cleansing and glow-boosting skin care.",
    },
    {
      image: "/img/bodymassage.webp",
      title: "Body Massage",
      description: "Relax your body and mind with soothing massage.",
    }
  ];
</script>

<section class="py-12 px-4 lg:px-40 bg-lightFigma">
  <h2 class="text-center text-4xl lg:text-5xl font-bold mb-10 text-goldFigma">OUR SERVICES</h2>

  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
    {#each services as service}
      <ServiceCard {...service} />
    {/each}
  </div>
</section>
