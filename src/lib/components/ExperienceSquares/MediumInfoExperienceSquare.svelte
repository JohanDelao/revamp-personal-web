<script lang="ts">
	import GridPattern from './GridPattern.svelte';

	export let title: string;
	export let value: string;
	export let style: string = '';
</script>

<div
	class="grid-item relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-[0.5px] border-primary-text"
	{style}
>
	<span class="flex flex-col gap-1">
		<span class="flex justify-center font-work-sans tracking-wide text-primary-text">{title}</span>
		<span class="flex justify-center font-eczar text-4xl text-[#9EC0FF]">{value}</span>
	</span>
	<GridPattern patternSize={56} />
</div>
