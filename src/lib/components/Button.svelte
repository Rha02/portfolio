<script lang="ts">
	import type { HTMLAnchorAttributes, HTMLButtonAttributes } from 'svelte/elements';

	// Generic type of button element
	type Element = $$Generic<'button' | 'a'>;

	// Button Elements interface
	interface ButtonComponentElements {
		button: HTMLButtonAttributes;
		a: HTMLAnchorAttributes;
	}

	// Generic props for button component
	type $$Props = ButtonComponentElements[Element] & {
		element: Element;
		variant?: 'solid' | 'outline' | 'text';
		color?: 'red' | 'green' | 'cyan';
		className?: string;
	};

	// Props
	export let element: Element;
	export let variant: 'solid' | 'outline' | 'text' = 'solid';
	export let color: 'red' | 'green' | 'cyan' = 'cyan';
	export let className: string = '';
</script>

<svelte:element
	this={element}
	class="btn btn-{variant} btn-{color} {className}"
	on:click
	{...$$restProps}
>
	<slot />
</svelte:element>

<style lang="scss">
	.btn {
		padding: 0.5rem 1rem;
		cursor: pointer;
		display: flex;
		align-items: center;
		transition: 0.15s;
		outline: none;
		color: white;
		border-radius: 5px;
		gap: 0.2rem;
		text-decoration: none;
		&.btn-solid {
			border: none;
			&.btn-red {
				background-color: var(--red-color);
			}
			&.btn-green {
				background-color: var(--green-color);
			}
			&.btn-cyan {
				background-color: var(--cyan-color);
			}
			&:hover,
			&:focus {
				&.btn-red {
					box-shadow: 0 0 5px 2px var(--red-color);
					text-shadow: 0 0 2px var(--red-color);
				}
				&.btn-green {
					box-shadow: 0 0 5px 2px var(--green-color);
					text-shadow: 0 0 2px var(--green-color);
				}
				&.btn-cyan {
					box-shadow: 0 0 5px 2px var(--cyan-color);
					text-shadow: 0 0 2px var(--cyan-color);
				}
			}
		}
		&.btn-outline {
			background-color: transparent;
			border: 1px solid;
			&.btn-red {
				border-color: var(--red-color);
				color: var(--red-color);
			}
			&.btn-green {
				border-color: var(--green-color);
				color: var(--green-color);
			}
			&.btn-cyan {
				border-color: var(--cyan-color);
				color: var(--cyan-color);
			}
			&:hover,
			&:focus {
				&.btn-red {
					box-shadow: 0 0 5px 2px var(--red-color);
					text-shadow: 0 0 2px var(--red-color);
				}
				&.btn-green {
					box-shadow: 0 0 5px 2px var(--green-color);
					text-shadow: 0 0 2px var(--green-color);
				}
				&.btn-cyan {
					box-shadow: 0 0 5px 2px var(--cyan-color);
					text-shadow: 0 0 2px var(--cyan-color);
				}
			}
		}
		&.btn-text {
			background-color: transparent;
			border: none;
		}
	}
</style>
