<script lang="ts">
	import { page } from '$app/stores';

	interface NavItem {
		name: string;
		href: string;
	}

	const navItems: NavItem[] = [
		{
			name: 'Home',
			href: '/'
		},
		{
			name: 'About',
			href: '/about'
		},
		{
			name: 'Contact',
			href: '/contact'
		}
	];
</script>

<nav>
	<a href="/" class="title"> Romuz Abdulhamidov </a>
	<ul class="nav-links">
		{#each navItems as item}
			<li>
				<a href={item.href} class:active={item.href == $page.url.pathname}>
					{item.name}
				</a>
			</li>
		{/each}
	</ul>
</nav>

<style lang="scss">
	nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		min-height: 5rem;
		position: fixed;
		background-color: var(--bg-color);
		z-index: 100;
		width: 100%;
		border-bottom: var(--border-color) 1px solid;
		ul {
			display: flex;
			gap: 2rem;
			margin-right: 1rem;
			@include breakpoint.up('md') {
				margin-right: 2rem;
			}
			@include breakpoint.up('lg') {
				margin-right: 3rem;
			}
			@include breakpoint.up('xl') {
				margin-right: 4rem;
			}
			li {
				list-style: none;
				a {
					color: var(--text-color);
					text-decoration: none;
                    transition: 0.2s;
					&:hover, &.active {
						color: var(--accent-color);
					}
				}
			}
		}
		.title {
			font-weight: 300;
			font-size: 1.5rem;
			flex-shrink: 0;
			margin-left: 1rem;
			color: var(--text-color);
			text-decoration: none;
			@include breakpoint.up('md') {
				margin-left: 2rem;
			}
			@include breakpoint.up('lg') {
				margin-left: 3rem;
			}
			@include breakpoint.up('xl') {
				margin-left: 4rem;
			}
		}
	}
</style>
