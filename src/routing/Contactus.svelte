<!-- ContactPage.svelte -->
<script>
import ContactForm from "../components/contact/ContactForm.svelte";
import AddingMap from "../components/contact/AddingMap.svelte";
</script>

<div class="flex flex-col md:flex-row gap-10 p-6 bg-white">
  <!-- Left Side: Contact Info + Map -->
  <div class="w-full md:w-1/2 space-y-6">
    <h2 class="text-black text-lg font-semibold">Contact Us</h2>

    <div class="flex items-center space-x-2 text-gray-700 text-sm hover:text-goldFigma cursor-pointer">
      <i class="fas fa-headset"></i>
      <a href="tel:014002799" class="text-xs lg:text-base font-medium hover:text-goldFigma">01-4002799</a>
    </div>

    <div class="flex items-center space-x-2 text-gray-700 text-sm hover:text-goldFigma cursor-pointer">
      <i class="fas fa-envelope"></i>
      <a href="mailto:info@beautystudio.com" target="_blank" class="text-xs lg:text-base font-medium hover:text-goldFigma">
        info@beautystudio.com
      </a>
    </div>

    <AddingMap />
  </div>

  <!-- Right Side: Contact Form -->
  <div class="w-full md:w-1/2">
    <ContactForm />
  </div>
</div>
