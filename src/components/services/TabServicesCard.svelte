<script>
    export let image = "";
    export let title = "";
    export let description = "";
  </script>
  
  <div class="bg-white shadow-md hover:shadow-xl transition-shadow duration-300 rounded-2xl overflow-hidden h-[300px] flex flex-col">
    <img src={image} alt={title} class="w-full h-60 object-cover" />
    
    <div class="flex flex-col justify-between flex-grow p-4">
      <div>
        <h3 class="text-lg font-semibold text-goldFigma mb-2">{title}</h3>
      </div>
      
   
    </div>
  </div>
  