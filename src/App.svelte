<script>
  import Router from 'svelte-spa-router';
  import Home from "./routing/Home.svelte";
  import AboutUs from "./routing/AboutUs.svelte";
  import Contact from "./routing/Contactus.svelte";
  import Services from "./routing/Services.svelte";
  import Navbar from "./components/Navbar.svelte";
  import Footer from './components/Footer.svelte';
  const routes={
    '/': Home,
    '/about': AboutUs,
    '/contact': Contact,
    '/services': Services

  }
let NavbarOpen = false;

function toggleNavbar(){
  NavbarOpen = !NavbarOpen;
}
</script>

<!-- <div class="layout {NavbarOpen ? 'navbar-open' : 'navbar-closed'}">
  {#if NavbarOpen} -->
    <div class="bg-bgFigma">

      <Navbar/>  
    </div>
  <!-- {/if} -->
<main>
  <Router {routes} />
</main>
<!-- </div> -->

<Footer/>