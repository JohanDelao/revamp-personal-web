<script>
	import ExperienceSquare from '$lib/components/ExperienceSquares/ExperienceSquare.svelte';
	import CompanyExperienceSquare from '$lib/components/ExperienceSquares/CompanyExperienceSquare.svelte';
	import MediumInfoExperienceSquare from '$lib/components/ExperienceSquares/MediumInfoExperienceSquare.svelte';
	import GridPattern from './ExperienceSquares/GridPattern.svelte';
</script>

<!-- 21 columns, 6 rows grid with left-to-right domino animation
Animation timing by column:
- Col 1: 0.05s, Col 2: 0.1s, Cols 3-5: 0.15s, Col 6: 0.3s, Col 7: 0.35s
- Cols 8-14: 0.4s (center div), Col 15: 0.45s, Col 16: 0.5s, Cols 17-19: 0.55s
- Individual squares in cols 15-21: 0.45s, 0.5s, 0.55s, 0.6s, 0.65s, 0.7s, 0.75s -->
<section class="relative h-120 w-full bg-primary px-10 py-16">
	<div
		class="grid size-full auto-rows-auto grid-cols-[repeat(21,minmax(0,1fr))] grid-rows-[repeat(6,minmax(0,1fr))] content-evenly justify-evenly gap-4"
	>
		<!-- Row 1: Slack(col1), square(col2), Internships(cols3-5), squares(cols6-7), center div(cols8-14), Fulltime(cols17-19), squares(cols20-21) -->
		<CompanyExperienceSquare
			companyInfo={{
				name: 'slack',
				description: 'Helped Slack support find \n logs faster.',
				timeline: 'Summer 2023',
				background: '#FFF4E5',
				href: 'https://www.slack.com',
				color: '#1e1e1e',
				emoji: '🕵',
				border: '#FFD8A8'
			}}
		/>
		<ExperienceSquare />
		<MediumInfoExperienceSquare title="Internships" value="2" />
		<ExperienceSquare />
		<ExperienceSquare />
		<div
			class="grid-item relative col-span-7 row-span-6 flex size-full items-center justify-center overflow-clip rounded-sm border-[0.5px] border-primary-text px-6"
			style="animation-delay: 0.4s;"
		>
			<div class="z-10 flex flex-col gap-4">
				<span class="z-10 flex justify-center font-eczar text-3xl text-[#9EC0FF]">Experience</span>
				<span
					class="font-geist flex justify-center text-center font-normal tracking-wide text-primary-text/70"
					>New Grad Software Engineer focused on delivering the best UI/UX to users. Graduated from
					the City College of New York with a bachelors degree in Computer Science.
				</span>
				<a
					class="mx-auto w-fit rounded-sm border-1 border-[#9EC0FF] px-2 py-1 font-work-sans text-[#9EC0FF] transition-all duration-300 ease-in-out hover:border-blue-300 hover:text-blue-500 hover:shadow-lg hover:shadow-blue-200/50"
					href="https://www.linkedin.com/in/johandelao/">Connect with me on LinkedIn</a
				>
			</div>
			<GridPattern patternSize={96} />
		</div>
		<ExperienceSquare />
		<ExperienceSquare />
		<MediumInfoExperienceSquare title="Fulltime Roles" value="1" />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 2: squares(cols1-2), Internships continues(cols3-5), Datadog Summer(col6), square(col7), center continues(cols8-14), Datadog Present(col16), Fulltime continues(cols17-19), squares(cols20-21) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- Internships 3x2 div continues here (cols 3-5) -->
		<CompanyExperienceSquare
			companyInfo={{
				name: 'datadog',
				description: 'Enabled power users to build faster \n in App Builder',
				timeline: 'Summer 2024',
				background: '#f4f0fb',
				href: 'https://www.datadoghq.com/product/app-builder/',
				color: '#1e1e1e',
				emoji: '🔨',
				border: '#e0d6fb'
			}}
		/>
		<ExperienceSquare />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare />
		<CompanyExperienceSquare
			companyInfo={{
				name: 'datadog',
				description: 'Bringing AI-powered tools \n to App Builder',
				timeline: 'Present',
				href: 'https://www.datadoghq.com/product/app-builder/',
				background: '#f4f0fb',
				color: '#1e1e1e',
				emoji: '🔨',
				border: '#e0d6fb'
			}}
		/>
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 3: squares(cols1-7), center continues(cols8-14), squares(cols15-21) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 4: squares(cols1-7), center continues(cols8-14), squares(cols15-21) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 5: squares(cols1-2), Communities(cols3-5), squares(cols6-7), center continues(cols8-14), squares(col15-16), Github Repos(cols17-19), squares(cols20-21) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<MediumInfoExperienceSquare title="Communities" value="4" />
		<ExperienceSquare />
		<ExperienceSquare />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare />
		<ExperienceSquare />
		<MediumInfoExperienceSquare title="Github Repos" value="77" />
		<ExperienceSquare />
		<ExperienceSquare />

		<!-- Row 6: squares(cols1-4), center continues(cols8-14), squares(cols15-18) -->
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
