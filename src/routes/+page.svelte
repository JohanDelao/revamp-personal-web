<script>
	import Hero from '$lib/components/Hero.svelte';
	import Separator from '$lib/components/Separator.svelte';
	import Experience from '$lib/components/ExperienceGrid.svelte';
	import ResumeSection from '$lib/components/ResumeSection.svelte';
	import * as Tooltip from '$lib/components/ui/tooltip/index.js';
</script>

<Tooltip.Provider>
	<div class="relative h-full w-full">
		<Hero />
		<Separator />
		<Experience />
		<Separator />
		<ResumeSection />
		<Separator />
	</div>
</Tooltip.Provider>
