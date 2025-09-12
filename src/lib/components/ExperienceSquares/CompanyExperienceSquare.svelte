<script lang="ts">
	import ExperienceSquare from '$lib/components/ExperienceSquares/ExperienceSquare.svelte';
	import * as Tooltip from '$lib/components/ui/tooltip/index.js';

	type CompanyInfo = {
		name: string;
		description: string;
		href: string;
		timeline: string;
		background: string;
		color: string;
		border: string;
		emoji?: string;
	};

	export let companyInfo: CompanyInfo;
	const { name, description, timeline, background, color, border, emoji } = companyInfo;
	const displayTitle = name.charAt(0).toUpperCase() + name.slice(1);
</script>

<Tooltip.Root delayDuration={0}>
	<Tooltip.Trigger>
		<ExperienceSquare propLogo={name} />
	</Tooltip.Trigger>
	<Tooltip.Content>
		<div
			class="font-geist flex w-fit max-w-sm flex-col gap-1 rounded-sm border-[0.5px] px-4 py-5"
			style="background-color: {background}; color: {color}; border-color: {border}"
		>
			<span class="w-fit font-eczar text-xl font-semibold">
				<span class="whitespace-pre-line">{description} {emoji || ''}</span>
			</span>
			<span class="flex items-center gap-2 text-sm font-medium">
				{displayTitle}
				-
				{timeline}
			</span>
		</div>
	</Tooltip.Content>
</Tooltip.Root>
