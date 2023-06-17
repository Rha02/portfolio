<script lang="ts">
	import FileIcon from '$lib/icons/File.svelte';
	import GithubIcon from '$lib/icons/Github.svelte';
	import LinkedinIcon from '$lib/icons/Linkedin.svelte';
</script>

<div class="content">
	<div class="profile">
		<img src="" alt="" width="400" height="500" />
		<div class="profile-content">
			<div>
				<div class="profile-heading">
					<h6>Hi, I am</h6>
					<h1>Romuz Abdulhamidov</h1>
					<h6>Full-Stack Software Engineer</h6>
				</div>
				<div class="profile-description">
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem, possimus atque! Nisi,
						libero. Neque esse deserunt aliquam a est quae natus, ullam vitae quidem molestiae
						doloribus assumenda, dolore fuga harum! Lorem ipsum dolor sit amet consectetur
						adipisicing elit. Nam, laboriosam rerum omnis numquam assumenda quia velit magnam
						tempore deleniti rem magni explicabo pariatur sapiente. Minima est sed consequatur ad
						autem? Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto voluptatibus
						doloribus veritatis beatae aperiam vero expedita placeat nostrum eligendi maxime!
					</p>
				</div>
			</div>
			<div class="profile-buttons">
				<button>
					<FileIcon width={16} height={16} stroke="#ffffff" />Resume
				</button>
				<button><GithubIcon width={16} height={16} fill="#ffffff" stroke="#ffffff" />GitHub</button>
				<button><LinkedinIcon width={16} height={16} fill="#ffffff" stroke="#ffffff" />LinkedIn</button>
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.profile {
		display: flex;
		margin: 2rem 0 0 0;
		.profile-content {
			margin: 2rem 0 0 2rem;
			max-width: 600px;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			padding: 0 0 1rem 0;
			.profile-heading {
				h6 {
					font-size: 1.5rem;
					font-weight: 400;
					margin: 0 0 0.5rem 0;
					color: var(--text-color-light);
				}
				h1 {
					font-size: 2.5rem;
					font-weight: 700;
					color: #fff;
					margin: 0 0 0.5rem 0;
				}
			}
			.profile-description {
				p {
					font-size: 1.2rem;
					font-weight: 400;
					color: var(--text-color-lighter);
				}
			}
		}
	}
	.profile-buttons {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		gap: 1rem;
		margin: 2rem 0 0 0;
		button {
			padding: 0.5rem 1rem;
			border: none;
			border-radius: 5px;
			background-color: var(--accent-color);
			color: #fff;
			font-size: 1rem;
			font-weight: 500;
			cursor: pointer;
			transition: 0.2s;
			display: flex;
			align-items: center;
			gap: 0.2rem;
			&:hover {
				background-color: var(--accent-color-dark);
			}
		}
	}
</style>
