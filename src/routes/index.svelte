<script>
  import successkid from "images/successkid.jpg";
</script>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<section class="text-center">
  <h1
    class="title-font sm:text-6xl text-3xl mb-4 font-medium text-gray-900
    uppercase">
    Great success!
  </h1>
  <figure
    class="mx-auto mt-2 lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
    <img
      class="object-cover object-center rounded shadow"
      alt="Success Kid"
      src={successkid} />
    <figcaption>Have fun with Sapper and TailwindCSS!</figcaption>
  </figure>
  <p class="mt-2">
    <strong>
      Try editing this file (src/routes/index.svelte) to test live reloading.
    </strong>
  </p>
</section>
