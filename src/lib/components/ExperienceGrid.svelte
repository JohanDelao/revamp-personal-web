<script>
	import ExperienceSquare from './ExperienceSquare.svelte';
</script>

<!-- 21 columns, 6 rows grid filled with experience squares -->
<section class="relative h-96 w-full px-10">
	<div
		class="grid size-full auto-rows-auto grid-cols-[repeat(21,minmax(0,1fr))] grid-rows-[repeat(6,minmax(0,1fr))] content-evenly justify-evenly gap-4"
	>
		<!-- Row 1: positions 1-2, 3x2 div takes 3-5, positions 6-7, 7x6 div takes 8-14, positions 15-21 -->
		<ExperienceSquare propLogo="slack" />
		<ExperienceSquare />
		<div
			class="relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF]"
		>
			<span class="flex flex-col gap-1">
				<span class="flex justify-center font-cabin tracking-wide text-[#6A7282]">Internships</span>
				<span class="flex justify-center font-eczar text-4xl text-[#00A0FF]">2</span>
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
		<ExperienceSquare />
		<ExperienceSquare />
		<div
			class="relative col-span-7 row-span-6 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF] px-6"
		>
			<div class="z-10 flex flex-col gap-4">
				<span class="z- flex justify-center font-eczar text-3xl text-[#00A0FF]">Experience</span>
				<span
					class="font-cabinfont-normal flex justify-center text-center tracking-wide text-[#6A7282]"
					>New Grad Software Engineer focused on delivering the best UI/UX to users. Graduated from
					the City College of New York with a bachelors degree in Computer Science.
				</span>
				<a
					class="mx-auto w-fit rounded-sm border-2 border-[#D9D9D9] px-2 py-1 font-geist text-[#565D6B]"
					href="https://www.linkedin.com/in/johandelao/">Connect with me on LinkedIn</a
				>
			</div>
			<svg class="absolute inset-0 size-full" xmlns="http://www.w3.org/2000/svg">
				<defs>
					<pattern id="dotGrid2" x="0" y="0" width="10" height="10" patternUnits="userSpaceOnUse">
						<circle cx="1" cy="1" r="1" fill="#C5E4FF" opacity="0.3" />
					</pattern>
				</defs>
				<rect width="100%" height="100%" fill="url(#dotGrid2)" />
			</svg>
		</div>
		<ExperienceSquare />
		<ExperienceSquare />
		<div
			class="relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF]"
		>
			<span class="flex flex-col gap-1">
				<span class="flex justify-center font-cabin tracking-wide text-[#6A7282]"
					>Fulltime Roles</span
				>
				<span class="flex justify-center font-eczar text-4xl text-[#00A0FF]">1</span>
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
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 2: positions 1-2, 3x2 continues, positions 6-7, 7x6 continues, positions 15-21 -->
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- 3x2 div continues here (positions 3-5) -->
		<ExperienceSquare propLogo="datadog" />
		<ExperienceSquare />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare propLogo="datadog" />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 3: positions 1-7, 7x6 continues 8-14, positions 15-21 -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 4: positions 1-7, 7x6 continues 8-14, positions 15-21 -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 5: positions 1-7, 7x6 continues 8-14, positions 15-21 -->
		<ExperienceSquare />
		<ExperienceSquare />
		<div
			class="relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF]"
		>
			<span class="flex flex-col gap-1">
				<span class="flex justify-center font-cabin tracking-wide text-[#6A7282]">Communities</span>
				<span class="flex justify-center font-eczar text-4xl text-[#00A0FF]">4</span>
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
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<div
			class="relative col-span-3 row-span-2 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF]"
		>
			<span class="flex flex-col gap-1">
				<span class="flex justify-center font-cabin tracking-wide text-[#6A7282]">Github Repos</span
				>
				<span class="flex justify-center font-eczar text-4xl text-[#00A0FF]">77</span>
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
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 6: positions 1-7, 7x6 continues 8-14, positions 15-21 -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
	</div>
</section>
