<script>
    import { link } from 'svelte-spa-router';
    import { push } from 'svelte-spa-router';
    
    let showMobileMenu = false;

  
    function toggleMobileMenu() {
      showMobileMenu = !showMobileMenu;
    }
    function navigateTo(path) {
    push(path);
    if (showMobileMenu) {
      showMobileMenu = false;
    }
  }
  </script>
  <div>
    <div class=" fixed top-0 left-0 w-full z-50 flex justify-center flex-row lg:space-x-12 lg:justify-center lg:items-center bg-blackFigma px-2 py-2 lg:px-40 gap-3">
  
      <div class="flex items-center space-x-2 text-softBeigeFigma text-sm hover:text-goldFigma cursor-pointer">
        <i class="fas fa-headset lg:text-base font-semibold"></i>
        <a href="tel:014002799" class="text-xs lg:text-base font-medium hover:text-goldFigma">01-4002799</a>      </div>
    
      <div class="flex items-center space-x-2 text-softBeigeFigma text-sm hover:text-goldFigma cursor-pointer">
        <i class="fas fa-envelope"></i>
        <a href="mailto:info@beautystudio.com" class="text-xs lg:text-base font-medium hover:text-goldFigma">info@beautystudio.com</a>
      </div>
    
      <div class="flex space-x-3 -pl-15">
        <a href="https://www.facebook.com/belishabeautystudio" target="_blank" class="text-softBeigeFigma hover:text-goldFigma"><i class="fab fa-facebook-f"></i></a>
        <a href="https://wa.me/977114002799" target="_blank" class="text-softBeigeFigma hover:text-goldFigma"><i class="fab fa-whatsapp"></i></a>
        <a href="https://www.instagram.com/belishabeautystudio" target="_blank" class="text-softBeigeFigma hover:text-goldFigma"><i class="fab fa-instagram"></i></a>
        <a href="#" target="_blank" class="text-softBeigeFigma hover:text-goldFigma"><i class="fab fa-tiktok"></i></a>
      </div>
    
    </div>
    

    
    <nav class="flex justify-between items-center px-6 pt-12 h-28 md:px-20 lg:px-40 py-4 top-0  sticky opacity-75 bg-transparent">
    <!-- Logo always on the left -->
    <div class="flex items-center mt-5">
      <img src="/public/img/logo.png" class="h-20 w-16" alt="Logo" />
    </div>
  
    <!-- Desktop Navigation -->
    <div class="hidden md:flex space-x-8 text-lg font-semibold">
      <a on:click={() => navigateTo('/')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Home</a>
      <a on:click={() => navigateTo('/about')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">About Us</a>
      <a on:click={() => navigateTo('/contact')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Contact</a>
      <a on:click={() => navigateTo('/services')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Services</a>

      
    </div>
    
    <!-- Hamburger button: visible only on mobile, on the right side -->
    <button class="md:hidden text-3xl mt-auto" on:click={toggleMobileMenu}>
      ☰
    </button>
  </nav>
  
  <!-- Mobile Menu -->
  {#if showMobileMenu}
  <div class="md:hidden flex flex-col items-center space-y-4 px-4 md:px-20 py-4 bg-gray-100">
    <a on:click={() => navigateTo('/')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Home</a>
      <a on:click={() => navigateTo('/about')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">About Us</a>
      <a on:click={() => navigateTo('/contact')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Contact</a>
      <a on:click={() => navigateTo('/services')} class="hover:text-yellow-600 cursor-pointer hover:border-b-2">Services</a>

  
  </div>
  {/if}
  
</div>