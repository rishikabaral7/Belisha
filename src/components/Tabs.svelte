<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    export let items;
    export let activeItem;
  </script>
  
  <div class="pt-10 font-sans bg-lightFigma lg:font-semibold">
    <ul class="flex flex-wrap justify-center gap-2 px-4">
      {#each items as item}
        <li on:click={() => dispatch('tabChange', item)}>
          <div
            class={`cursor-pointer px-4 py-2 rounded whitespace-nowrap 
              ${item === activeItem 
                ? 'text-goldFigma font-semibold border-b-2 border-goldFigma' 
                : 'text-paragraphFigma hover:text-goldFigma'}`}
          >
            {item}
          </div>
        </li>
      {/each}
    </ul>
  </div>
  