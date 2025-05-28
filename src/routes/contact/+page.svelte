<script>
	import Button from '$components/Button.svelte';
</script>

<div class="content">
	<h1>Let's Get In Touch!</h1>
	<form action="" method="post">
		<div class="form-field">
			<label for="name">What's your name?</label>
			<input type="text" name="name" placeholder="Name" required />
		</div>
		<div class="form-field">
			<label for="contact">Your Contact Info? (Email, LinkedIn, or Phone #)</label>
			<input type="text" name="contact" placeholder="Your contact info here..." required />
		</div>
		<div class="form-field">
			<label for="message">Message</label>
			<textarea name="message" id="" rows="6" placeholder="Message" required></textarea>
		</div>
		<section class="btn-div">
			<Button element="button" target="_blank" variant="outline" color="cyan" type="submit" disabled>
				<span style="width: 100px; font-weight: 500;">Send</span>
			</Button>
		</section>
	</form>
</div>

<style lang="scss">
	label:has(+ input:required):after {
		content: ' *';
		color: var(--red-color);
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	form {
		width: 50%;
		display: flex;
		flex-direction: column;
		gap: 1rem;
		.form-field {
			display: flex;
			flex-direction: column;
			gap: 0.5rem;
			label {
				color: var(--text-color-light);
				font-size: large;
			}
			input {
				max-width: 450px;
				background-color: var(--border-color);
				color: var(--text-color);
				padding: 8px 12px;
				outline: none;
				border-radius: 2px;
				border: 0;
				border-bottom: 1px solid var(--text-color);
				transition: border-color 0.2s ease;
				&:focus {
					border-bottom: 1px solid var(--cyan-color);
					background-image: linear-gradient(0deg, rgb(34, 211, 238, 0.4), transparent 30%);
				}
			}
			textarea {
				max-width: 800px;
				background-color: var(--border-color);
				color: var(--text-color);
				padding: 8px 12px;
				outline: none;
				border-radius: 2px;
				border: 0;
				border-bottom: 1px solid var(--text-color);
				transition: border-color 0.2s ease;
				&:focus {
					border-bottom: 1px solid var(--cyan-color);
					background-image: linear-gradient(0deg, rgb(34, 211, 238, 0.4), transparent 10%);
				}
			}
		}
		.btn-div {
			width: 100%;
		}
	}
</style>
