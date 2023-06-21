<script lang="ts">
	import 'modern-normalize/modern-normalize.css';
    import '../styles/main.scss'
	import Navbar from '$components/Navbar.svelte';
</script>

<div class="main">
    <header>
        <Navbar />
    </header>
    <main>
        <slot></slot>
    </main>
    <footer>
        <p>Footer</p>
    </footer>
</div>

<style lang="scss">
	.main {
		display: flex;
        flex-direction: column;
        overflow-y: hidden;
        min-height: 100vh;
        background-color: var(--bg-color);
        color: var(--text-color);

        header {
            min-height: 5rem;
        }
	}
</style>
