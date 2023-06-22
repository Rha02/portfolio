<script lang="ts">
	import { page } from '$app/stores';
	import MenuIcon from '$lib/icons/Menu.svelte';
	import XIcon from '$lib/icons/X.svelte';

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

	let isMenuOpen = false;

	const openMenu = () => {
		isMenuOpen = true;
	};

	const closeMenu = () => {
		isMenuOpen = false;
	};
</script>

<nav>
	<div class="top-bar">
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
		<div class="nav-links-mobile">
			{#if isMenuOpen}
				<button class="menu-button" on:click={closeMenu}>
					<XIcon stroke="white" width={32} height={32} />
				</button>
			{:else}
				<button class="menu-button" on:click={openMenu}>
					<MenuIcon stroke="white" width={32} height={32} />
				</button>
			{/if}
		</div>
	</div>
	{#if isMenuOpen}
		<div class="mobile-menu">
			<ul>
				{#each navItems as item}
					<li>
						<a href={item.href} class:active={item.href == $page.url.pathname}>
							{item.name}
						</a>
					</li>
				{/each}
			</ul>
		</div>
	{/if}
</nav>

<style lang="scss">
	nav {
		z-index: 100;
		position: fixed;
		width: 100%;
	}
	.top-bar {
		display: flex;
		justify-content: space-between;
		align-items: center;
		min-height: 5rem;
		background-color: var(--bg-color);
		border-bottom: var(--border-color) 1px solid;
		.nav-links {
			display: none;
			gap: 2rem;
			margin-right: 1rem;
			@include breakpoint.up('md') {
				margin-right: 2rem;
				display: flex;
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
					padding: 12px;
					&:hover {
						color: var(--cyan-color);
					}
					&.active {
						color: var(--cyan-color);
						text-shadow: 0 0 2px var(--cyan-color);
					}
				}
			}
		}
		.nav-links-mobile {
			margin-right: 1rem;
			@include breakpoint.up('md') {
				display: none;
			}
			.menu-button {
				padding: 0.5rem 1rem;
				cursor: pointer;
				transition: 0.15s;
				outline: none;
				color: white;
				background-color: transparent;
				border: none;
				border-radius: 5px;
				&:hover,
				&:focus {
					background-color: rgba(255, 255, 255, 0.1);
				}
				&:active {
					background-color: rgba(255, 255, 255, 0.2);
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
	.mobile-menu {
		display: flex;
		justify-content: end;
		@include breakpoint.up('md') {
			display: none;
		}
		ul {
			margin: -0.5rem 0.5rem;
			padding: 0;
			list-style: none;
			width: 45%;
			max-width: 14rem;
			border: 1px solid var(--border-color);
			border-radius: 5px;
			background-color: var(--bg-color);
			box-shadow: 0 0 4px rgba(255, 255, 255, 0.2);
			li {
				width: 100%;
				transition: 0.1s;
				&:hover {
					background-color: rgba(0, 0, 0, 0.1);
				}
				a {
					display: inline-block;
					padding: 0.5rem 1rem;
					height: 100%;
					width: 100%;
					color: var(--text-color);
					text-decoration: none;
					transition: 0.2s;
					&.active {
						color: var(--cyan-color);
						text-shadow: 0 0 2px var(--cyan-color);
					}
				}
			}
		}
	}
</style>
