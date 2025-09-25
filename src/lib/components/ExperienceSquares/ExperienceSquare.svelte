<script lang="ts">
	import logo from '$lib/assets/Logo.png';
	import SlackLogo from '$lib/components/logos/Slack.svelte';
	import DatadogLogo from '$lib/components/logos/Datadog.svelte';
	import clsx from 'clsx';
	import GridPattern from './GridPattern.svelte';

	let { propLogo = undefined, gridSize = 24 } = $props();
</script>

<div
	class={clsx(
		'grid-item relative flex aspect-square size-full items-center justify-center rounded-sm border-[0.6px] border-primary-text p-1.5',
		propLogo
			? 'transition-all duration-300 ease-in-out hover:border-blue-300 hover:shadow-lg hover:shadow-blue-200/50'
			: ''
	)}
>
	<GridPattern patternSize={gridSize} />
	{#if propLogo == 'slack'}
		<SlackLogo />
	{:else if propLogo == 'datadog'}
		<DatadogLogo />
	{:else}
		<img src={logo} alt="Logo" class="h-full w-full object-contain opacity-90" />
	{/if}
</div>
