<script>
  import AddingMap from "../lib/contact/AddingMap.svelte";
  
  let name = '';
  let email = '';
  let message = '';
  let submitted = false;
  let errorMessage = '';

  async function handleSubmit(e) {
    e.preventDefault();
    errorMessage = ''; // Reset error message

    try {
      const res = await fetch("https://formsubmit.co/ajax/info@beautystudio.com", {
        method: "POST",
        headers: { "Content-Type": "application/json", Accept: "application/json" },
        body: JSON.stringify({ name, email, message })
      });

      if (res.ok) {
        submitted = true;
        name = '';
        email = '';
        message = '';

        // Reset the success message after 5 seconds
        setTimeout(() => {
          submitted = false;
        }, 5000); // 5000ms = 5 seconds
      } else {
        throw new Error("Something went wrong. Please try again.");
      }
    } catch (error) {
      errorMessage = error.message;
    }
  }
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

    <!-- Map -->
    <AddingMap />
  </div>

  <!-- Right Side: Form -->
  <div class="w-full md:w-1/2">
    {#if submitted}
      <div class="bg-green-100 text-green-800 p-4 rounded shadow-md">
        ✅ Message sent successfully! We’ll be in touch soon.
      </div>
    {:else}
      {#if errorMessage}
        <div class="bg-red-100 text-red-800 p-4 rounded shadow-md">
          ❌ {errorMessage}
        </div>
      {/if}

      <form on:submit={handleSubmit} class="space-y-4">
        <div>
          <label class="block text-gray-700 text-sm mb-1">Name</label>
          <input type="text" bind:value={name} required placeholder="Your Name"
                 class="w-full border border-gray-300 bg-white text-gray-800 rounded p-2" />
        </div>

        <div>
          <label class="block text-gray-700 text-sm mb-1">Email</label>
          <input type="email" bind:value={email} required placeholder="you@example.com"
                 class="w-full border border-gray-300 bg-white text-gray-800 rounded p-2" />
        </div>

        <div>
          <label class="block text-gray-700 text-sm mb-1">Message</label>
          <textarea bind:value={message} required placeholder="Your message here..."
                    class="w-full border border-gray-300 bg-white text-gray-800 rounded p-2 h-32"></textarea>
        </div>

        <button type="submit" class="bg-goldFigma text-white font-medium px-4 py-2 rounded hover:bg-white hover:border-1 hover:border-goldFigma hover:text-goldFigma cursor-pointer">
          Send
        </button>
      </form>
    {/if}
  </div>
</div>
