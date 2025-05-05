<script>
  import Router from 'svelte-spa-router';
  import Home from "./routing/Home.svelte";
  import AboutUs from "./routing/AboutUs.svelte";
  import Contact from "./routing/Contactus.svelte";
  import Services from "./routing/Services.svelte";
  import Navbar from "./components/Navbar.svelte";
  import Footer from './components/Footer.svelte';

  const routes = {
    '/': Home,
    '/about': AboutUs,
    '/contact': Contact,
    '/services': Services
  };

  let NavbarOpen = false;

  function toggleNavbar() {
    NavbarOpen = !NavbarOpen;
  }
</script>

<div class="bg-bgFigma min-h-screen flex flex-col font-display">
  <Navbar />
  <main class="flex-grow">  
    <Router {routes} />
  </main>
  <Footer />
</div>
