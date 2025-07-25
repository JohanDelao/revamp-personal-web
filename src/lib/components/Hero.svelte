<script>
	import Resume from './Resume.svelte';
	import weightFigure from '../assets/WeightFigure.png';
	import jiujitsuFigure from '../assets/JiujitsuFigure.png';
</script>

<div class="background-gradient h-dvh w-full">
	<div class="flex h-full w-full items-center justify-center">
		<div class="flex flex-col gap-10">
			<h1 class="relative block text-center font-urbanist text-6xl font-bold">
				<span class="text-[#D2F1FF]">
					<span class="relative z-10 flex justify-center">
						Hi. I’m Johan.
						<span class="absolute -top-14 -right-52">
							<figure class="relative">
								<img src={weightFigure} width={80} height={80} alt="Weight Figure" />
							</figure>
						</span>
					</span>
					<span class="relative z-10 flex justify-center">
						A Software Engineer
						<span class="absolute -bottom-32 -left-52">
							<figure class="relative">
								<img src={jiujitsuFigure} width={80} height={80} alt="Weight Figure" />
							</figure>
						</span>
					</span>
				</span>
			</h1>
			<p class="text-center font-cabin text-lg text-white/70">
				Passionate about developing great UI/UX and designs
			</p>
			<Resume />
		</div>
	</div>
</div>
