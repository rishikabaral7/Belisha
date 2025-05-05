<script>
  import { push } from "svelte-spa-router";
  import OurServices from "../components/OurServices.svelte";
  import HeroPage from "../components/HeroPage.svelte";

  const workingHours = [
    { day: "SUNDAY", hours: "09:00–19:00" },
    { day: "MONDAY", hours: "09:00–19:00" },
    { day: "TUESDAY", hours: "09:00–19:00" },
    { day: "WEDNESDAY", hours: "09:00–19:00" },
    { day: "THURSDAY", hours: "09:00–19:00" },
    { day: "FRIDAY", hours: "09:00–19:00" },
    { day: "SATURDAY", hours: "closed" },
  ];

  function navigateTo(path){
    push(path);
  }
</script>

<!-- firstsection -->
<HeroPage />

<!-- 2nd Section -->
<div
  class="bg-lightFigma py-12 px-4 md:px-20 lg:px-40 grid grid-cols-1 md:grid-cols-2 gap-10"
>
  <div>
    <img
      src="/img/secondsection.jpg"
      class="w-full h-[345px] object-cover rounded-md"
      alt="Second section showing a hair salon environment"
    />
  </div>
  <div class="md:pt-12 lg:pt-16">
    <h1 class="text-3xl md:text-4xl lg:text-5xl text-brownFigma font-bold">
      We Are More Than a Hair Salon
    </h1>
    <p class="text-paragraphFigma text-sm md:text-base py-6 font-sans">
      A place where professional beauty services like hair styling, makeup,
      skincare, and grooming are provided to help clients look and feel their
      best.
    </p>
    <button
    class="-ml-12 -my-22 bg-goldFigma px-4 py-2 lg:-mt-2 lg:-ml-1 md:-ml-45 text-white text-sm lg:text-base rounded-lg hover:bg-white hover:border-goldFigma hover:text-goldFigma transition-all duration-300 hover:cursor-pointer hover:border-1"
  >
  <a on:click={()=>navigateTo('/about')} >

    About Us
  </a>
  </button>
  </div>
</div>

<!-- 3rd Section -->
<div
  class="py-12 px-4 md:px-20 lg:px-40 grid grid-cols-1 md:grid-cols-2 gap-10"
  style="background-image: url('/img/background.png');"
>
  <div>
    <img
      src="/img/thirdsession.jpg"
      class="w-full h-[400px] object-cover rounded-md"
      alt="Third section showing a professional hair salon setup"
    />
  </div>
  <div
    class="border-2 border-lightFigma p-6 bg-lightFigma bg-opacity-70 rounded-lg flex flex-col items-center"
  >
    <h2 class="text-2xl md:text-3xl font-bold mb-6 text-brownFigma">
      WORKING HOURS
    </h2>
    <div class="w-full max-w-md flex flex-col gap-3">
      {#each workingHours as entry}
        <div class="flex justify-between border-b border-gray-300 pb-1">
          <span class="text-brownFigma font-medium">{entry.day}</span>
          <span class="text-brownFigma font-medium">{entry.hours}</span>
        </div>
      {/each}
    </div>
  </div>
</div>

<!-- Services Section -->
<OurServices />

<!-- 5th Section -->
<div
  class="bg-white py-12 px-4 md:px-20 lg:px-40 grid grid-cols-1 md:grid-cols-2 gap-10 font-roboto"
>
  <div>
    <img
      src="/img/lastpage.jpg"
      class="w-full h-[500px] object-cover rounded-md"
      alt="A stylish haircut and treatment session in progress"
    />
  </div>
  <div class="md:pt-12 lg:pt-16">
    <h1 class="text-3xl md:text-4xl text-brownFigma font-bold">
      Best Haircut & Treatments Experience For All Customers
    </h1>
    <p class="text-paragraphFigma text-sm md:text-base py-6">
      We provide the ultimate haircut and treatment experience, ensuring the
      best results for all our customers
    </p>

    <div class="flex flex-col gap-6">
      <div class="flex items-start gap-4">
        <img src="/img/experience.jpg" class="w-10 h-10" alt="Experience icon" />
        <div>
          <h4 class="font-bold text-blackFigma">Years Of Experiences</h4>
          <p class="text-xs text-paragraphFigma">Expertise honed over time</p>
        </div>
      </div>

      <div class="flex items-start gap-4">
        <img src="/img/clean.png" class="w-10 h-10" alt="Clean and best choice icon" />
        <div>
          <h4 class="font-bold text-blackFigma">Clean & Best Choicing</h4>
          <p class="text-xs text-paragraphFigma">
            Optimal and spotless selections
          </p>
        </div>
      </div>
    </div>
  </div>
</div>
