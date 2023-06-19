<script lang="ts">
	export let width = 64;
	export let height = 64;
	export let fill = 'none';
	export let stroke = '#000000';
</script>

<svg
	{width}
    {height}
	viewBox="0 0 20 20"
	xmlns="http://www.w3.org/2000/svg"
	fill={fill}
>
	<path
		fill={stroke}
		fill-rule="evenodd"
		d="M19 4a1 1 0 01-1 1H2a1 1 0 010-2h16a1 1 0 011 1zm0 6a1 1 0 01-1 1H2a1 1 0 110-2h16a1 1 0 011 1zm-1 7a1 1 0 100-2H2a1 1 0 100 2h16z"
	/>
</svg>
