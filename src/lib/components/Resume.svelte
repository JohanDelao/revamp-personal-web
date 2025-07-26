<script>
	import resume from '../assets/Resume Design.png';
</script>

<div class="w-full">
	<div class="flex w-full max-w-2xl">
		<div class="contents">
			<a
				class="group relative flex max-h-[600px] w-full flex-col rounded-[60px] bg-gradient-to-br from-orange-100 to-pink-50 transition-all duration-300 hover:-translate-y-[3px] hover:shadow-[var(--shadow-lg)] hover:saturate-[1.2]"
				href="/resume"
			>
				<div class="relative flex size-full flex-col overflow-hidden rounded-[60px] p-14">
					<div class="text-right text-[#364442]">
						<span class="text-base font-normal tracking-wider">TAKE A LOOK AT MY</span>
						<h2 class="font-urbanist text-4xl font-bold">RESUME</h2>
					</div>
					<div
						class="mt-10 flex flex-1 items-end justify-center transition-all duration-300 group-hover:translate-y-[1rem]"
					>
						<div class="mx-auto my-0 w-full max-w-2xl">
							<figure class="relative">
								<img src={resume} class="relative max-w-2xl" alt="Resume" />
							</figure>
						</div>
					</div>
				</div>
			</a>
		</div>
	</div>
</div>
