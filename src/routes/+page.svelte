<script>
	import Nav from '$lib/components/Nav.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Separator from '$lib/components/Separator.svelte';
	import Experience from '$lib/components/ExperienceGrid.svelte';
	import ParallaxBackground from '$lib/components/ParallaxBackground.svelte';
	import * as Tooltip from '$lib/components/ui/tooltip/index.js';
</script>

<Tooltip.Provider>
	<div class="relative w-full">
		<Nav />
		<Hero />
		<Separator />
		<Experience />
		<Separator />
		<section class="relative my-8 h-[500px] w-full overflow-hidden border-2 border-gray-300">
			<ParallaxBackground className="absolute top-0 left-0 w-full h-full -z-10" />
			<div
				class="relative z-10 flex h-full flex-col items-center justify-center bg-black/30 p-8 text-center text-white"
			>
				<h1 class="mb-4 text-5xl font-bold" style="text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);">
					Tech Stack Explosion
				</h1>
				<p class="text-xl" style="text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);">
					Watch my technologies and frameworks explode outward when you scroll to this section!
				</p>
			</div>
		</section>
	</div>
</Tooltip.Provider>
