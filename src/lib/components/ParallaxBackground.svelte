<script lang="ts">
	import { onMount } from 'svelte';
	import StarLayer from './layers/StarLayer.svelte';
	import MainTech from './layers/MainTech.svelte';
	import Frameworks from './layers/Frameworks.svelte';

	// Props for configuration
	let { className = '', threshold = 0.3 } = $props();

	let containerRef: HTMLDivElement;
	let isVisible = $state(false);

	onMount(() => {
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					isVisible = entry.isIntersecting;
				});
			},
			{ threshold }
		);

		if (containerRef) {
			observer.observe(containerRef);
		}

		return () => observer.disconnect();
	});
</script>

<div
	class="pointer-events-none relative size-full overflow-hidden {className}"
	bind:this={containerRef}
>
	<!-- Layer 1: Star Layer - Slowest, largest scale variations -->
	<div
		class="absolute top-1/2 left-1/2 size-full -translate-x-1/2 -translate-y-1/2 scale-[0.3] opacity-40 transition-all duration-[1200ms] ease-out {isVisible
			? 'exploded-1'
			: ''}"
	>
		<StarLayer />
	</div>

	<!-- Layer 2: Main Tech - Medium-slow, moderate movement -->
	<div
		class="absolute top-1/2 left-1/2 size-full -translate-x-1/2 -translate-y-1/2 scale-[0.3] opacity-40 transition-all delay-100 duration-[1200ms] ease-out {isVisible
			? 'exploded-2'
			: ''}"
	>
		<MainTech />
	</div>

	<!-- Layer 3: Frameworks - Medium-fast, smaller scale -->
	<div
		class="absolute top-1/2 left-1/2 size-full -translate-x-1/2 -translate-y-1/2 scale-[0.3] opacity-40 transition-all delay-200 duration-[1200ms] ease-out {isVisible
			? 'exploded-3'
			: ''}"
	>
		<Frameworks />
	</div>
</div>
