<!-- Map.svelte -->
<script>
    export let locationUrl = "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3532.0823851455033!2d85.3134853!3d27.7175151!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39eb191d57e5ba51%3A0x4fdab04a04ced998!2sThe%20Malla%20Hotel!5e0!3m2!1sen!2snp!4v1683134081463!5m2!1sen!2snp";
  </script>
  
  <div class="w-full h-72 md:h-[400px] lg:h-[500px] rounded-xl overflow-hidden shadow-lg mt-10">
    <iframe
      src={locationUrl}
      width="100%"
      height="100%"
      allowfullscreen
      title="Map showing the location"
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      class="border-none w-full h-100"
    ></iframe>
  </div>
  