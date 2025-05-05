<script>
  import active from "svelte-spa-router/active";
  import TabsServices from "../components/services/TabsHairServices.svelte";
  import TabsNailServices from "../components/services/TabsNailServices.svelte";
  import TabsHairRemoval from "../components/services/TabsHairRemoval.svelte";
  import Tabs from "../components/Tabs.svelte";
  import TabsEyeLashes from "../components/services/TabsEyeLashes.svelte";
  import TabsBodyMassage from "../components/services/TabsBodyMassage.svelte";
  let items = ['Hair Services', 'Nail Services', 'Hair Removal', 'Eyelash Services', 'Facial Treatments'];
  let activeItem = items[0]; // Set the first item as active by default
  const tabChange = (e) =>{
    activeItem = e.detail;
  }

</script>


    <section
        class="font-sans lg:h-140 h-50 w-full bg-cover bg-center flex items-center justify-center font-sans"
        style="background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.6)), url('/img/services/herosection.jpeg');">
        <h1 class="text-softBeigeFigma text-4xl lg:text-8xl font-bold font-display">SERVICES</h1>
    </section>
   
<Tabs {activeItem} {items} on:tabChange={tabChange}/>
{#if activeItem === 'Hair Services'}
<TabsServices/>
{:else if activeItem === 'Nail Services'}
<TabsNailServices/>
{:else if activeItem === 'Hair Removal'}
<TabsHairRemoval/>
{:else if activeItem === 'Eyelash Services'}
<TabsEyeLashes/>
{:else if activeItem === 'Facial Treatments'}
<TabsBodyMassage/>
{/if}
