<script lang="ts">
	interface Props {
		width?: number;
		height?: number;
		fill?: string;
		stroke?: string;
	}

	let {
		width = 64,
		height = 64,
		fill = 'none',
		stroke = '#000000'
	}: Props = $props();
</script>

<svg {width} {height} viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
	<path
		d="M18,22H6a2,2,0,0,1-2-2V4A2,2,0,0,1,6,2h7.1a2,2,0,0,1,1.5.6l4.9,5.2A2,2,0,0,1,20,9.2V20A2,2,0,0,1,18,22Z"
		id="File"
		{stroke}
		{fill}
		stroke-linecap="round"
		stroke-linejoin="round"
		stroke-width="2"
	/>

	<line
		{fill}
		{stroke}
		stroke-linecap="round"
		stroke-linejoin="round"
		stroke-width="2"
		x1="7.9"
		x2="16.1"
		y1="17.5"
		y2="17.5"
	/>

	<line
		{fill}
		{stroke}
		stroke-linecap="round"
		stroke-linejoin="round"
		stroke-width="2"
		x1="7.9"
		x2="16.1"
		y1="13.5"
		y2="13.5"
	/>

	<line
		{fill}
		{stroke}
		stroke-linecap="round"
		stroke-linejoin="round"
		stroke-width="2"
		x1="8"
		x2="13"
		y1="9.5"
		y2="9.5"
	/>
</svg>
