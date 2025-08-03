<script>
	import Resume from './Resume.svelte';
	import weightFigure from '../assets/WeightFigure.png';
	import jiujitsuFigure from '../assets/JiujitsuFigure.png';
	import transformerFigure from '../assets/TransformerFigure.png';
</script>

<section class="background-gradient min-h-dvh w-full">
	<div class="flex size-full items-center justify-center">
		<div class="flex flex-col gap-10">
			<h1
				class="animate-fadeInDown relative block pt-40 text-center font-urbanist text-6xl font-bold opacity-0"
				style="animation-delay: 0.2s;"
			>
				<span class="text-[#D2F1FF]">
					<span class="relative z-10 flex justify-center">
						Hi. I'm Johan.
						<span class="absolute -top-14 -right-44">
							<figure class="animate-popIn relative">
								<img src={weightFigure} width={80} height={80} alt="Weight Figure" />
							</figure>
						</span>
						<span class="absolute top-80 -right-36">
							<figure class="animate-popIn relative">
								<img src={transformerFigure} width={80} height={80} alt="Weight Figure" />
							</figure>
						</span>
					</span>
					<span class="relative z-10 flex justify-center">
						A Software Engineer
						<span class="absolute -bottom-32 -left-44">
							<figure class="animate-popIn relative">
								<img src={jiujitsuFigure} width={80} height={80} alt="Weight Figure" />
							</figure>
						</span>
					</span>
				</span>
			</h1>
			<p
				class="animate-fadeInDown text-center font-cabin text-lg text-white/70 opacity-0"
				style="animation-delay: 0.4s;"
			>
				Passionate about developing great UI/UX and designs
			</p>
			<div class="animate-fadeInDown opacity-0" style="animation-delay: 0.8s;">
				<Resume />
			</div>
		</div>
	</div>
</section>
