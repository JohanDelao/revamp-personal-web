<script lang="ts">
	import logo from '$lib/assets/Logo.png';
	import SlackLogo from '$lib/components/logos/Slack.svelte';
	import DatadogLogo from '$lib/components/logos/Datadog.svelte';
	import clsx from 'clsx';

	let { propLogo = undefined, style = '' } = $props();
</script>

<div
	class={clsx(
		'grid-item flex aspect-square size-full items-center justify-center rounded-md border-2 border-dashed border-[#C5E4FF] p-1.5',
		propLogo
			? 'transition-all duration-300 ease-in-out hover:border-blue-300 hover:shadow-lg hover:shadow-blue-200/50'
			: ''
	)}
	{style}
>
	{#if propLogo == 'slack'}
		<SlackLogo />
	{:else if propLogo == 'datadog'}
		<DatadogLogo />
	{:else}
		<img src={logo} alt="Logo" class="h-full w-full object-contain opacity-30" />
	{/if}
</div>
