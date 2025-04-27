<script lang="ts">
	import FileIcon from '$lib/icons/File.svelte';
	import GithubIcon from '$lib/icons/Github.svelte';
	import LinkedinIcon from '$lib/icons/Linkedin.svelte';
	import Button from '$lib/components/Button.svelte';
</script>

<div class="content">
	<div class="profile">
		<img src="/romuz_photo.png" alt="" />
		<div class="profile-content">
			<div>
				<div class="profile-heading">
					<h6>Hi, I am</h6>
					<h1>Romuz Abdulhamidov</h1>
					<h6>Full-Stack Software Engineer</h6>
				</div>
				<div class="profile-description">
					<ul>
						<li>Tech Enthusiast</li>
						<hr />
						<li>Building cloud-native web applications at Walmart</li>
						<hr />
						<li>1.5 Years of Internship Experience</li>
						<hr />
						<li>Trilingual (English, Russian, Tajik)</li>
					</ul>
				</div>
			</div>
			<div class="profile-buttons">
				<Button
					element="a"
					href="https://drive.google.com/file/d/1yaQPURt1-27xRiQIHUXTsVO_aGjxeXJ-/view?usp=sharing"
					target="_blank"
					variant="outline"
					color="red"
				>
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
	<section class="experience">
		<h2>Work Experience</h2>
		<div class="work-experience">
			<div class="work-logo">
				<img src="/walmart.jpg" alt="" />
			</div>
			<div class="work-text">
				<h3>Walmart Global Tech</h3>
				<h4>Software Engineer</h4>
				<h5>February 2025 - Present</h5>
			</div>
		</div>
		<div class="work-experience">
			<div class="work-logo">
				<img src="/walmart.jpg" alt="" />
			</div>
			<div class="work-text">
				<h3>Walmart Global Tech</h3>
				<h4>Software Engineer Intern</h4>
				<h5>June 2024 - August 2024</h5>
			</div>
		</div>
		<div class="work-experience">
			<div class="work-logo">
				<img src="/koch.png" alt="" />
			</div>
			<div class="work-text">
				<h3>Koch Industries</h3>
				<h4>Data Engineer Intern</h4>
				<h5>May 2023 - May 2024</h5>
			</div>
		</div>
	</section>
	<section class="education">
		<h2>Education</h2>
		<div class="education-section">
			<div class="education-image">
				<img src="/sjsu.jpg" alt="" />
			</div>
			<div class="education-text">
				<h3>San Jose State University</h3>
				<h4>Bachelor of Science in Software Engineering</h4>
				<h5>August 2021 - December 2024</h5>
			</div>
		</div>
	</section>
	<section class="skills">
		<h2>Technical Skills</h2>
		<div class="skills-cards">
			<div class="card card-a">
				<h3 class="card-header cyan">Databases</h3>
				<div class="card-body">
					<ul>
						<li>
							<img src="/svgs/postgres.svg" alt="" width="25" /> PostgresSQL
						</li>
						<li>
							<img src="/svgs/mysql.svg" alt="" width="25" /> MySQL
						</li>
						<li>
							<img src="/svgs/mongodb.svg" alt="" width="25" /> MongoDB
						</li>
						<li>
							<img src="/svgs/redis.svg" alt="" width="25" /> Redis
						</li>
						<li>
							<img src="/svgs/cassandra.svg" alt="" width="25" /> Cassandra
						</li>
					</ul>
				</div>
			</div>
			<div class="card card-b">
				<h3 class="card-header cyan">Backend</h3>
				<div class="card-body">
					<ul>
						<li>
							<img src="/svgs/go.svg" alt="" width="25" /> Go
						</li>
						<li>
							<img src="/svgs/java.svg" alt="" width="25" /> Java
						</li>
						<li>
							<img src="/svgs/python.svg" alt="" width="25" /> Python
						</li>
						<li>
							<img src="/svgs/fastapi.svg" alt="" width="25" /> FastAPI
						</li>
						<li>
							<img src="/svgs/nodejs.svg" alt="" width="25" /> Node.js + Express
						</li>
						<li>
							<img src="/svgs/spring.svg" alt="" width="25" /> Spring Boot
						</li>
						<li>
							<img src="/svgs/laravel.svg" alt="" width="25" /> Laravel
						</li>
					</ul>
				</div>
			</div>
			<div class="card card-c">
				<h3 class="card-header cyan">Frontend</h3>
				<div class="card-body">
					<ul>
						<li>
							<img src="/svgs/typescript.svg" alt="" width="25" /> TypeScript
						</li>
						<li>
							<img src="/svgs/javascript.svg" alt="" width="25" /> JavaScript
						</li>
						<li>
							<img src="/svgs/sveltekit.svg" alt="" width="25" /> SvelteKit
						</li>
						<li>
							<img src="/svgs/react.svg" alt="" width="25" /> React.js
						</li>
						<li>
							<img src="/svgs/next.svg" alt="" width="25" /> Next.js
						</li>
						<li>
							<img src="/svgs/vue.svg" alt="" width="25" /> Vue.js
						</li>
					</ul>
				</div>
			</div>
			<div class="card card-d">
				<h3 class="card-header cyan">Others</h3>
				<div class="card-body">
					<ul>
						<li>
							<img src="/svgs/azure.svg" alt="" width="25" /> Azure
						</li>
						<li>
							<img src="/svgs/aws.svg" alt="" width="25" /> AWS
						</li>
						<li>
							<img src="/svgs/docker.svg" alt="" width="25" /> Docker
						</li>
						<li>
							<img src="/svgs/postman.svg" alt="" width="25" /> Postman
						</li>
						<li>
							<img src="/svgs/git.svg" alt="" width="25" /> Git
						</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
</div>

<style lang="scss">
	h2 {
		font-size: 1.8rem;
		font-weight: 700;
		color: #fff;
		margin: 3rem 0 0 0;
	}
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
		margin: 2rem;
		@include breakpoint.up('lg') {
			flex-direction: row;
		}
		img {
			width: 231px;
			height: 297px;
			border-radius: 15px;
			@include breakpoint.up('sm') {
				width: 280px;
				height: 360px;
			}
			@include breakpoint.up('md') {
				width: 315px;
				height: 405px;
			}
			@include breakpoint.up('lg') {
				width: 350px;
				height: 450px;
			}
		}
		.profile-content {
			margin: 1rem 0 0 0rem;
			min-width: 300px;
			max-width: 550px;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			padding: 0 0 1rem 0;
			@include breakpoint.up('lg') {
				margin: 1rem 0 0 2rem;
			}
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
					font-weight: 700;
					color: #fff;
					margin: 0 0 0.5rem 0;
					@include breakpoint.up('md') {
						font-size: 2rem;
					}
					@include breakpoint.up('lg') {
						text-align: left;
					}
					@include breakpoint.up('xl') {
						font-size: 2.2rem;
					}
				}
			}
			.profile-description {
				ul {
					font-size: 1rem;
					text-align: center;
					font-weight: 400;
					padding-left: 0;
					color: var(--text-color-lighter);
					@include breakpoint.up('sm') {
						font-size: 1.1rem;
					}
					@include breakpoint.up('lg') {
						text-align: left;
						padding-left: 1.5rem;
						font-size: 1.1rem;
					}
					@include breakpoint.up('xl') {
						font-size: 1.2rem;
					}
					li {
						list-style: none;
						line-height: 1rem;
						@include breakpoint.up('lg') {
							list-style: disc;
							line-height: 2rem;
						}
					}
					hr {
						opacity: 25%;
						width: 25%;
						@include breakpoint.up('lg') {
							display: none;
						}
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
		.skills-cards {
			display: grid;
			grid-template-columns: repeat(1, 1fr);
			grid-template-areas: 'a' 'b' 'c' 'd';
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
					'c c d d';
			}
			@include breakpoint.up('xl') {
				grid-template-columns: repeat(4, 1fr);
				grid-template-areas:
					'a a b b'
					'c c d d';
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
					&.green {
						border-bottom: 2px solid var(--green-color);
						background-image: linear-gradient(0deg, rgb(74, 222, 128, 0.6), transparent 65%);
					}
					&.cyan {
						border-bottom: 2px solid var(--cyan-color);
						background-image: linear-gradient(0deg, rgb(34, 211, 238, 0.6), transparent 65%);
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
							display: flex;
							align-items: center;
							gap: 0.5rem;
							&:last-child {
								margin: 0;
							}
						}
					}
				}
			}
		}
	}
	.education {
		text-align: center;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		.education-section {
			margin: 2rem 1rem 0 0;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			width: 100%;
			gap: 1rem;
			@include breakpoint.up('sm') {
				flex-direction: row;
				gap: 1.2rem;
			}
			.education-image {
				display: flex;
				flex-direction: column;
				align-items: center;
				@include breakpoint.up('sm') {
					align-items: end;
					width: 50%;
				}
				img {
					width: 150px;
					height: 150px;
					border-radius: 15px;
					@include breakpoint.up('md') {
						width: 200px;
						height: 200px;
					}
				}
			}
			.education-text {
				text-align: center;
				@include breakpoint.up('sm') {
					text-align: start;
					width: 50%;
					padding-right: 1rem;
				}
				h3 {
					font-size: 18px;
					@include breakpoint.up('md') {
						font-size: 1.5rem;
					}
				}
				h4 {
					font-size: 13px;
					@include breakpoint.up('md') {
						font-size: 1rem;
					}
				}
				h5 {
					font-size: 12px;
					@include breakpoint.up('md') {
						font-size: 0.9rem;
					}
				}
			}
		}
	}
	.experience {
		text-align: center;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		.work-experience {
			margin: 2rem 1rem 0 0;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			width: 100%;
			gap: 1rem;
			@include breakpoint.up('sm') {
				flex-direction: row;
				gap: 2rem;
			}
			.work-logo {
				display: flex;
				flex-direction: column;
				align-items: center;
				@include breakpoint.up('sm') {
					align-items: end;
					width: 50%;
				}
				img {
					width: 150px;
					height: 150px;
					border-radius: 15px;
					@include breakpoint.up('md') {
						width: 200px;
						height: 200px;
					}
				}
			}
			.work-text {
				text-align: center;
				@include breakpoint.up('sm') {
					text-align: start;
					width: 50%;
					padding-right: 1rem;
				}
				h3 {
					font-size: 18px;
					@include breakpoint.up('md') {
						font-size: 1.5rem;
					}
				}
				h4 {
					font-size: 13px;
					@include breakpoint.up('md') {
						font-size: 1rem;
					}
				}
				h5 {
					font-size: 12px;
					@include breakpoint.up('md') {
						font-size: 0.9rem;
					}
				}
			}
		}
	}
</style>
