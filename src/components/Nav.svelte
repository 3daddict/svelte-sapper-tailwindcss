<script>
	export let segment;
</script>

<style>

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

</style>

<header class="text-gray-600 body-font">
  <div class="container mx-auto flex flex-wrap p-5 items-center">
    <nav class="flex lg:w-2/5 flex-wrap items-center text-base">
	<a class="mr-5 hover:text-gray-900" aria-current="{segment === undefined ? 'page' : undefined}" href=".">home</a>
	  <a class="mr-5 hover:text-gray-900" aria-current="{segment === 'about' ? 'page' : undefined}" href="about">about</a>
		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches the blog data when we hover over the link or tap it on a touchscreen -->
	  <a class="mr-5 hover:text-gray-900" rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a>
    </nav>
    <div class="lg:w-2/5 inline-flex lg:justify-end ml-5 lg:ml-0">
    </div>
  </div>
</header>