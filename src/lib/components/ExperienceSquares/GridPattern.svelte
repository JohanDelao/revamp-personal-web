<script lang="ts">
	let { patternSize = 40 } = $props();
	const patternId = `gridPattern-${Math.random().toString(36).substring(2, 9)}`;
</script>

<svg class="absolute inset-0 z-0 h-full w-full overflow-hidden" xmlns="http://www.w3.org/2000/svg">
	<defs>
		<!-- Define your tile pattern -->
		<pattern id={patternId} patternUnits="userSpaceOnUse" width={patternSize} height={patternSize}>
			<!-- Paste the exported paths inside -->
			<g transform="scale({patternSize / 121})" transform-origin="0 0">
				<path
					d="M1 1V0.7H0.7V1H1ZM1 1V1.3H25V1V0.7H1V1ZM1 25H1.3V1H1H0.7V25H1Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M1 25V24.7H0.7V25H1ZM1 25V25.3H25V25V24.7H1V25ZM1 49H1.3V25H1H0.7V49H1Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M25 25V24.7H24.7V25H25ZM25 25V25.3H49V25V24.7H25V25ZM25 49H25.3V25H25H24.7V49H25Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M25 1V0.7H24.7V1H25ZM25 1V1.3H49V1V0.7H25V1ZM25 25H25.3V1H25H24.7V25H25Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M1 49V48.7H0.7V49H1ZM1 49V49.3H25V49V48.7H1V49ZM1 73H1.3V49H1H0.7V73H1Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M25 49V48.7H24.7V49H25ZM25 49V49.3H49V49V48.7H25V49ZM25 73H25.3V49H25H24.7V73H25Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M49 49V48.7H48.7V49H49ZM49 49V49.3H73V49V48.7H49V49ZM49 73H49.3V49H49H48.7V73H49Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M73 49V48.7H72.7V49H73ZM73 49V49.3H97V49V48.7H73V49ZM73 73H73.3V49H73H72.7V73H73Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M97 49V48.7H96.7V49H97ZM97 49V49.3H121V49V48.7H97V49ZM97 73H97.3V49H97H96.7V73H97Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M1 73V72.7H0.7V73H1ZM1 73V73.3H25V73V72.7H1V73ZM1 97H1.3V73H1H0.7V97H1Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M25 73V72.7H24.7V73H25ZM25 73V73.3H49V73V72.7H25V73ZM25 97H25.3V73H25H24.7V97H25Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M49 73V72.7H48.7V73H49ZM49 73V73.3H73V73V72.7H49V73ZM49 97H49.3V73H49H48.7V97H49Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M73 73V72.7H72.7V73H73ZM73 73V73.3H97V73V72.7H73V73ZM73 97H73.3V73H73H72.7V97H73Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M97 73V72.7H96.7V73H97ZM97 73V73.3H121V73V72.7H97V73ZM97 97H97.3V73H97H96.7V97H97Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M1 97V96.7H0.7V97H1ZM1 97V97.3H25V97V96.7H1V97ZM1 121H1.3V97H1H0.7V121H1Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M25 97V96.7H24.7V97H25ZM25 97V97.3H49V97V96.7H25V97ZM25 121H25.3V97H25H24.7V121H25Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M49 97V96.7H48.7V97H49ZM49 97V97.3H73V97V96.7H49V97ZM49 121H49.3V97H49H48.7V121H49Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M73 97V96.7H72.7V97H73ZM73 97V97.3H97V97V96.7H73V97ZM73 121H73.3V97H73H72.7V121H73Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M97 97V96.7H96.7V97H97ZM97 97V97.3H121V97V96.7H97V97ZM97 121H97.3V97H97H96.7V121H97Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M49 1V0.7H48.7V1H49ZM49 1V1.3H73V1V0.7H49V1ZM49 25H49.3V1H49H48.7V25H49Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M49 25V24.7H48.7V25H49ZM49 25V25.3H73V25V24.7H49V25ZM49 49H49.3V25H49H48.7V49H49Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M73 1V0.7H72.7V1H73ZM73 1V1.3H97V1V0.7H73V1ZM73 25H73.3V1H73H72.7V25H73Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M73 25V24.7H72.7V25H73ZM73 25V25.3H97V25V24.7H73V25ZM73 49H73.3V25H73H72.7V49H73Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M97 1V0.7H96.7V1H97ZM97 1V1.3H121V1V0.7H97V1ZM97 25H97.3V1H97H96.7V25H97Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
				<path
					d="M97 25V24.7H96.7V25H97ZM97 25V25.3H121V25V24.7H97V25ZM97 49H97.3V25H97H96.7V49H97Z"
					fill="#9EC0FF"
					fill-opacity="0.2"
				/>
			</g>
		</pattern>
	</defs>

	<!-- Big rectangle filled with the repeating pattern -->
	<rect width="100%" height="100%" fill="url(#{patternId})" />
</svg>
