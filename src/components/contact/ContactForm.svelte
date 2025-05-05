<!-- src/lib/contact/ContactForm.svelte -->
<script>
    export let endpoint = "https://formsubmit.co/ajax/info@beautystudio.com";
  
    let name = '';
    let email = '';
    let message = '';
    let submitted = false;
    let errorMessage = '';
  
    async function handleSubmit(e) {
      e.preventDefault();
      errorMessage = '';
  
      try {
        const res = await fetch(endpoint, {
          method: "POST",
          headers: { "Content-Type": "application/json", Accept: "application/json" },
          body: JSON.stringify({ name, email, message })
        });
  
        if (res.ok) {
          submitted = true;
          name = '';
          email = '';
          message = '';
          setTimeout(() => (submitted = false), 5000);
        } else {
          throw new Error("Something went wrong. Please try again.");
        }
      } catch (error) {
        errorMessage = error.message;
      }
    }
  </script>
  
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
  
      <button type="submit" class="bg-goldFigma text-white font-medium px-4 py-2 rounded hover:bg-white hover:border hover:border-goldFigma hover:text-goldFigma cursor-pointer">
        Send
      </button>
    </form>
  {/if}
  