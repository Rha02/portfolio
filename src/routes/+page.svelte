<script lang="ts">
	import FileIcon from '$lib/icons/File.svelte';
	import GithubIcon from '$lib/icons/Github.svelte';
	import LinkedinIcon from '$lib/icons/Linkedin.svelte';
	import Button from '$lib/components/Button.svelte';
</script>

<div class="content">
	<div class="profile">
		<img src="" alt="" />
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
				<Button element="a" href="/" target="_blank" variant="outline" color="red">
					<FileIcon width={16} height={16} stroke="#f87171" />Resume
				</Button>
				<Button
					element="a"
					href="https://github.com/Rha02"
					target="_blank"
					variant="outline"
					color="green"
				>
					<GithubIcon width={16} height={16} fill="#4ade80" stroke="#4ade80" />GitHub
				</Button>
				<Button
					element="a"
					href="https://www.linkedin.com/in/romuz-abdulhamidov/"
					target="_blank"
					variant="outline"
					color="cyan"
				>
					<LinkedinIcon
						width={16}
						height={16}
						fill="var(--cyan-color)"
						stroke="var(--cyan-color)"
					/>LinkedIn
				</Button>
			</div>
		</div>
	</div>
	<div class="skills">
		<h2>Technical Skills</h2>
		<div class="skills-cards">
			<div class="card card-a">
				<h3 class="card-header red">Databases</h3>
				<div class="card-body">
					<ul>
						<li>PostgresSQL</li>
						<li>MySQL</li>
						<li>MongoDB</li>
						<li>Redis</li>
						<li>SQL</li>
					</ul>
				</div>
			</div>
			<div class="card card-b">
				<h3 class="card-header amber">Languages</h3>
				<div class="card-body">
					<ul>
						<li>Go</li>
						<li>TypeScript</li>
						<li>Python</li>
						<li>JavaScript</li>
						<li>Java</li>
						<li>PHP</li>
					</ul>
				</div>
			</div>
			<div class="card card-c">
				<h3 class="card-header green">Backend</h3>
				<div class="card-body">
					<ul>
						<li>Go</li>
						<li>Node.js</li>
						<li>Express.js</li>
						<li>Laravel</li>
						<li>Django</li>
						<li>Flask</li>
						<li>PHP</li>
					</ul>
				</div>
			</div>
			<div class="card card-d">
				<h3 class="card-header cyan">Frontend</h3>
				<div class="card-body">
					<ul>
						<li>Svelte</li>
						<li>React.js</li>
						<li>Vue.js</li>
						<li>HTML</li>
						<li>CSS</li>
						<li>SCSS</li>
					</ul>
				</div>
			</div>
			<div class="card card-e">
				<h3 class="card-header indigo">Others</h3>
				<div class="card-body">
					<ul>
						<li>Azure</li>
						<li>AWS</li>
						<li>Docker</li>
						<li>Postman</li>
						<li>CI/CD</li>
						<li>Git</li>
					</ul>
				</div>
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
		flex-direction: column;
		align-items: center;
		@include breakpoint.up('lg') {
			flex-direction: row;
		}
		margin: 2rem;
		img {
			width: 301px;
			height: 387px;
			@include breakpoint.up('sm') {
				width: 350px;
				height: 450px;
			}
		}
		.profile-content {
			margin: 1rem 0 0 0rem;
			@include breakpoint.up('lg') {
				margin: 1rem 0 0 2rem;
			}
			min-width: 300px;
			max-width: 550px;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			padding: 0 0 1rem 0;
			.profile-heading {
				h6 {
					font-size: 1.1rem;
					text-align: center;
					font-weight: 400;
					margin: 0 0 0.5rem 0;
					color: var(--text-color-light);
					@include breakpoint.up('sm') {
						font-size: 1.4rem;
					}
					@include breakpoint.up('lg') {
						text-align: left;
					}
					@include breakpoint.up('xl') {
						font-size: 1.5rem;
					}
				}
				h1 {
					font-size: 1.6rem;
					text-align: center;
					@include breakpoint.up('md') {
						font-size: 2rem;
					}
					@include breakpoint.up('lg') {
						text-align: left;
					}
					@include breakpoint.up('xl') {
						font-size: 2.2rem;
					}
					font-weight: 700;
					color: #fff;
					margin: 0 0 0.5rem 0;
				}
			}
			.profile-description {
				p {
					font-size: 1rem;
					text-align: center;
					font-weight: 400;
					color: var(--text-color-lighter);
					@include breakpoint.up('sm') {
						font-size: 1.1rem;
					}
					@include breakpoint.up('lg') {
						text-align: left;
						font-size: 1.1rem;
					}
					@include breakpoint.up('xl') {
						font-size: 1.2rem;
					}
				}
			}
		}
		.profile-buttons {
			display: flex;
			flex-direction: row;
			justify-content: center;
			gap: 0.5rem;
			margin: 1rem 0 0 0;
			font-size: 11px;
			@include breakpoint.up('sm') {
				gap: 1rem;
				font-size: 1rem;
			}
			@include breakpoint.up('lg') {
				justify-content: flex-start;
			}
		}
	}
	.skills {
		text-align: center;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		h2 {
			font-size: 1.8rem;
			font-weight: 700;
			color: #fff;
			margin: 4rem 0 0 0;
		}
		.skills-cards {
			display: grid;
			grid-template-columns: repeat(1, 1fr);
			grid-template-areas: 'a' 'b' 'c' 'd' 'e';
			@include breakpoint.down('md') {
				width: 100%;
			}
			@include breakpoint.up('lg') {
				gap: 1rem;
				grid-template-columns: repeat(2, 1fr);
				grid-template-areas:
					'a a b b'
					'a a b b'
					'c c d d'
					'c c d d'
					'. e e .';
			}
			@include breakpoint.up('xl') {
				grid-template-columns: repeat(6, 1fr);
				grid-template-areas:
					'a a b b c c'
					'. d d e e .';
			}
			.card {
				width: 90%;
				max-width: 24rem;
				margin: 1rem 0 0 0;
				display: flex;
				flex-direction: column;
				justify-self: center;
				@include breakpoint.up('lg') {
					width: 24rem;
				}
				@include breakpoint.up('xl') {
					width: 100%;
					min-width: 20rem;
					max-width: 24rem;
				}
				&-a {
					grid-area: a;
				}
				&-b {
					grid-area: b;
				}
				&-c {
					grid-area: c;
				}
				&-d {
					grid-area: d;
				}
				&-e {
					grid-area: e;
				}
				.card-header {
					font-size: 1.5rem;
					font-weight: 700;
					color: #fff;
					padding: 1rem;
					margin: 0;
					&.red {
						border-bottom: 2px solid var(--red-color);
						background-image: linear-gradient(0deg, rgb(248, 113, 113, 0.6), transparent 65%);
					}
					&.amber {
						border-bottom: 2px solid var(--amber-color);
						background-image: linear-gradient(0deg, rgb(252, 211, 77, 0.6), transparent 65%);
					}
					&.green {
						border-bottom: 2px solid var(--green-color);
						background-image: linear-gradient(0deg, rgb(74, 222, 128, 0.6), transparent 65%);
					}
					&.cyan {
						border-bottom: 2px solid var(--cyan-color);
						background-image: linear-gradient(0deg, rgb(34, 211, 238, 0.6), transparent 65%);
					}
					&.indigo {
						border-bottom: 2px solid var(--indigo-color);
						background-image: linear-gradient(0deg, rgb(129, 140, 248, 0.6), transparent 65%);
					}
				}
				.card-body {
					text-align: left;
					border: 1px solid var(--border-color);
					border-bottom-left-radius: 1rem;
					border-bottom-right-radius: 1rem;
					flex: auto;
					ul {
						list-style: none;
						margin: 1rem 0 1rem 0;
						padding: 0 1rem 0 1.5rem;
						li {
							font-size: 1.2rem;
							font-weight: 400;
							color: var(--text-color-light);
							margin: 0 0 0.5rem 0;
							&:last-child {
								margin: 0;
							}
						}
					}
				}
			}
		}
	}
</style>
