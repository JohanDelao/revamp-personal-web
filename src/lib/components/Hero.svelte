<script>
	import IsometricHeroBlueprint from './isometric-illustrations/IsometricHeroBlueprint.svelte';
	import InstagramIcon from './logos/InstagramSVG.svelte';
	import FigmaIcon from './logos/FigmaSVG.svelte';
	import GithubIcon from './logos/GithubSVG.svelte';
	import LinkedInIcon from './logos/LinkedInSVG.svelte';
</script>

<section class="h-dvh w-full overflow-hidden bg-primary pb-10">
	<div class="flex size-full flex-col items-center gap-12 px-10 pt-10">
		<div class="flex w-full items-center justify-start gap-6">
			<a href="https://www.instagram.com/iamjohandelao/" target="_blank">
				<InstagramIcon />
			</a>
			<a href="https://www.figma.com/@johan_delao" target="_blank">
				<FigmaIcon />
			</a>
			<a href="https://github.com/johandelao" target="_blank">
				<GithubIcon />
			</a>
			<a href="https://www.linkedin.com/in/johandelao/" target="_blank">
				<LinkedInIcon />
			</a>
		</div>
		<div class="relative flex w-full grow flex-col gap-10">
			<h1 class="font-space-grotesk text-2xl leading-9 text-faded-white">
				<span class="font-bold text-white">Johan Delao</span> is a Software Engineer at
				<span><a class="underline" href="https://www.datadoghq.com/">Datadog</a></span>, focused on
				<br />
				delivering great UI/UX and designs.
			</h1>
			<ul class="absolute bottom-0 left-0 space-y-2 font-space-grotesk text-xl text-primary-text">
				<li>EXPERIENCE</li>
				<li>RESUME</li>
				<li>PROJECTS</li>
				<li>CONTACT</li>
			</ul>
			<span class="absolute top-0 left-[25%]">
				<div
					class="animate-fadeInDown flex size-full items-center justify-center opacity-0"
					style="animation-delay: 0.8s;"
				>
					<IsometricHeroBlueprint />
				</div>
			</span>
		</div>
	</div>
</section>
