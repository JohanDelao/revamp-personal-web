<script>
	import ExperienceSquare from '$lib/components/ExperienceSquares/ExperienceSquare.svelte';
	import CompanyExperienceSquare from '$lib/components/ExperienceSquares/CompanyExperienceSquare.svelte';
	import MediumInfoExperienceSquare from '$lib/components/ExperienceSquares/MediumInfoExperienceSquare.svelte';

	function inView(node) {
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					if (entry.isIntersecting) {
						// Add animate class to all grid items with staggered delays
						const gridItems = node.querySelectorAll('.grid-item');
						gridItems.forEach((item, index) => {
							const delay = item.style.animationDelay || '0s';
							setTimeout(
								() => {
									item.classList.add('animate');
								},
								parseFloat(delay) * 1000
							);
						});
						observer.unobserve(node);
					}
				});
			},
			{ threshold: 0.2 }
		);
		observer.observe(node);

		return {
			destroy() {
				observer.disconnect();
			}
		};
	}
</script>

<!-- 21 columns, 6 rows grid with left-to-right domino animation
Animation timing by column:
- Col 1: 0.05s, Col 2: 0.1s, Cols 3-5: 0.15s, Col 6: 0.3s, Col 7: 0.35s
- Cols 8-14: 0.4s (center div), Col 15: 0.45s, Col 16: 0.5s, Cols 17-19: 0.55s
- Individual squares in cols 15-21: 0.45s, 0.5s, 0.55s, 0.6s, 0.65s, 0.7s, 0.75s -->
<section class="relative h-96 w-full px-10">
	<div
		class="grid size-full auto-rows-auto grid-cols-[repeat(21,minmax(0,1fr))] grid-rows-[repeat(6,minmax(0,1fr))] content-evenly justify-evenly gap-4"
		use:inView
	>
		<!-- Row 1: Slack(col1), square(col2), Internships(cols3-5), squares(cols6-7), center div(cols8-14), Fulltime(cols17-19), squares(cols20-21) -->
		<CompanyExperienceSquare
			style="animation-delay: 0.05s;"
			companyInfo={{
				name: 'slack',
				description: 'Helped Slack support find \n logs faster.',
				href: '',
				timeline: 'Summer 2023',
				background: '#FFF4E5',
				color: '#1e1e1e',
				emoji: '&#128373',
				border: '#FFD8A8'
			}}
		/>
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<MediumInfoExperienceSquare style="animation-delay: 0.15s;" title="Internships" value="2" />
		<ExperienceSquare style="animation-delay: 0.3s;" />
		<ExperienceSquare style="animation-delay: 0.35s;" />
		<div
			class="grid-item relative col-span-7 row-span-6 flex size-full items-center justify-center overflow-clip rounded-sm border-2 border-[#C5E4FF] px-6"
			style="animation-delay: 0.4s;"
		>
			<div class="z-10 flex flex-col gap-4">
				<span class="z-10 flex justify-center font-eczar text-3xl text-[#00A0FF]">Experience</span>
				<span
					class="flex justify-center text-center font-geist font-normal tracking-wide text-[#6A7282]"
					>New Grad Software Engineer focused on delivering the best UI/UX to users. Graduated from
					the City College of New York with a bachelors degree in Computer Science.
				</span>
				<a
					class="mx-auto w-fit rounded-sm border-2 border-[#D9D9D9] px-2 py-1 font-geist text-[#565D6B] transition-all duration-300 ease-in-out hover:border-blue-300 hover:text-blue-500 hover:shadow-lg hover:shadow-blue-200/50"
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
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<ExperienceSquare style="animation-delay: 0.5s;" />
		<MediumInfoExperienceSquare style="animation-delay: 0.55s;" title="Fulltime Roles" value="1" />
		<ExperienceSquare style="animation-delay: 0.7s;" />
		<ExperienceSquare style="animation-delay: 0.75s;" />

		<!-- Row 2: squares(cols1-2), Internships continues(cols3-5), Datadog Summer(col6), square(col7), center continues(cols8-14), Datadog Present(col16), Fulltime continues(cols17-19), squares(cols20-21) -->
		<ExperienceSquare style="animation-delay: 0.05s;" />
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<!-- Internships 3x2 div continues here (cols 3-5) -->
		<CompanyExperienceSquare
			style="animation-delay: 0.3s;"
			companyInfo={{
				name: 'datadog',
				description: 'Enabled power users to build faster \n in App Builder',
				href: '',
				timeline: 'Summer 2024',
				background: '#f4f0fb',
				color: '#1e1e1e',
				emoji: '&#x1F528',
				border: '#e0d6fb'
			}}
		/>
		<ExperienceSquare style="animation-delay: 0.35s;" />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<CompanyExperienceSquare
			style="animation-delay: 0.5s;"
			companyInfo={{
				name: 'datadog',
				description: 'Bringing AI-powered tools \n to App Builder',
				href: '',
				timeline: 'Present',
				background: '#f4f0fb',
				color: '#1e1e1e',
				emoji: '&#129302',
				border: '#e0d6fb'
			}}
		/>
		<ExperienceSquare style="animation-delay: 0.55s;" />
		<ExperienceSquare style="animation-delay: 0.6s;" />

		<!-- Row 3: squares(cols1-7), center continues(cols8-14), squares(cols15-21) -->
		<ExperienceSquare style="animation-delay: 0.05s;" />
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<ExperienceSquare style="animation-delay: 0.15s;" />
		<ExperienceSquare style="animation-delay: 0.2s;" />
		<ExperienceSquare style="animation-delay: 0.25s;" />
		<ExperienceSquare style="animation-delay: 0.3s;" />
		<ExperienceSquare style="animation-delay: 0.35s;" />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<ExperienceSquare style="animation-delay: 0.5s;" />
		<ExperienceSquare style="animation-delay: 0.55s;" />
		<ExperienceSquare style="animation-delay: 0.6s;" />
		<ExperienceSquare style="animation-delay: 0.65s;" />
		<ExperienceSquare style="animation-delay: 0.7s;" />
		<ExperienceSquare style="animation-delay: 0.75s;" />

		<!-- Row 4: squares(cols1-7), center continues(cols8-14), squares(cols15-21) -->
		<ExperienceSquare style="animation-delay: 0.05s;" />
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<ExperienceSquare style="animation-delay: 0.15s;" />
		<ExperienceSquare style="animation-delay: 0.2s;" />
		<ExperienceSquare style="animation-delay: 0.25s;" />
		<ExperienceSquare style="animation-delay: 0.3s;" />
		<ExperienceSquare style="animation-delay: 0.35s;" />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<ExperienceSquare style="animation-delay: 0.5s;" />
		<ExperienceSquare style="animation-delay: 0.55s;" />
		<ExperienceSquare style="animation-delay: 0.6s;" />
		<ExperienceSquare style="animation-delay: 0.65s;" />
		<ExperienceSquare style="animation-delay: 0.7s;" />
		<ExperienceSquare style="animation-delay: 0.75s;" />

		<!-- Row 5: squares(cols1-2), Communities(cols3-5), squares(cols6-7), center continues(cols8-14), squares(col15-16), Github Repos(cols17-19), squares(cols20-21) -->
		<ExperienceSquare style="animation-delay: 0.05s;" />
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<MediumInfoExperienceSquare style="animation-delay: 0.15s;" title="Communities" value="4" />
		<ExperienceSquare style="animation-delay: 0.3s;" />
		<ExperienceSquare style="animation-delay: 0.35s;" />
		<!-- Center 7x6 div continues here (cols 8-14) -->
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<ExperienceSquare style="animation-delay: 0.5s;" />
		<MediumInfoExperienceSquare style="animation-delay: 0.55s;" title="Github Repos" value="77" />
		<ExperienceSquare style="animation-delay: 0.7s;" />
		<ExperienceSquare style="animation-delay: 0.75s;" />

		<!-- Row 6: squares(cols1-4), center continues(cols8-14), squares(cols15-18) -->
		<ExperienceSquare style="animation-delay: 0.05s;" />
		<ExperienceSquare style="animation-delay: 0.1s;" />
		<ExperienceSquare style="animation-delay: 0.15s;" />
		<ExperienceSquare style="animation-delay: 0.2s;" />
		<!-- 7x6 div continues here (positions 8-14) -->
		<ExperienceSquare style="animation-delay: 0.45s;" />
		<ExperienceSquare style="animation-delay: 0.5s;" />
		<ExperienceSquare style="animation-delay: 0.55s;" />
		<ExperienceSquare style="animation-delay: 0.6s;" />
	</div>
</section>
