<script>
  export let image = "";
  export let title = "";
  export let description = "";
</script>

<div class="bg-white shadow-md hover:shadow-xl transition-shadow duration-300 rounded-2xl overflow-hidden h-[400px] flex flex-col">
  <img src={image} alt={title} class="w-full h-60 object-cover" />
  
  <div class="flex flex-col justify-between flex-grow p-4">
    <div>
      <h3 class="text-xl font-semibold text-goldFigma mb-2">{title}</h3>
      <p class="text-paragraphFigma text-sm mb-4">{description}</p>
    </div>
    
    <button class="w-full mt-auto bg-goldFigma hover:bg-yellow-600 text-white text-sm font-medium py-2 px-4 rounded-lg transition-colors duration-300 shadow-md">
      Explore More
    </button>
  </div>
</div>
