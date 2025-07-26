<script lang="ts">
	import logo from '../assets/Logo.png';
	import SlackLogo from './logos/Slack.svelte';
	import DatadogLogo from './logos/Datadog.svelte';

	let { propLogo = undefined } = $props();
</script>

<div class="aspect-square size-full rounded-sm border-2 border-dashed border-[#C5E4FF] p-2">
	{#if propLogo == 'slack'}
		<SlackLogo />
	{:else if propLogo == 'datadog'}
		<DatadogLogo />
	{:else}
		<img src={logo} alt="Logo" class="h-full w-full object-contain opacity-30" />
	{/if}
</div>
