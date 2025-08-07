<script lang="ts">
	export let title: string;
	export let value: string;
	export let style: string = '';
</script>

<div
	class="grid-item relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF]"
	{style}
>
	<span class="flex flex-col gap-1">
		<span class="flex justify-center font-cabin tracking-wide text-[#6A7282]">{title}</span>
		<span class="flex justify-center font-eczar text-4xl text-[#00A0FF]">{value}</span>
	</span>
	<svg class="absolute inset-0 size-full" xmlns="http://www.w3.org/2000/svg">
		<defs>
			<pattern id="dotGrid" x="0" y="0" width="10" height="10" patternUnits="userSpaceOnUse">
				<circle cx="1" cy="1" r="1" fill="#C5E4FF" opacity="0.3" />
			</pattern>
		</defs>
		<rect width="100%" height="100%" fill="url(#dotGrid)" />
	</svg>
</div>
