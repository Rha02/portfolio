<script lang="ts">
	import 'modern-normalize/modern-normalize.css';
    import '../styles/main.scss'
	import Navbar from '$components/Navbar.svelte';
    import NProgress from 'nprogress';
    import "nprogress/nprogress.css";
	import { afterNavigate, beforeNavigate } from '$app/navigation';

    NProgress.configure({ showSpinner: false });

    afterNavigate(() => {
        NProgress.done();
    })

    beforeNavigate(() => {
        NProgress.start();
    });
</script>

<div class="main">
    <header>
        <Navbar />
    </header>
    <main>
        <slot></slot>
    </main>
    <footer></footer>
</div>

<style lang="scss">
	.main {
		display: flex;
        flex-direction: column;
        overflow-y: hidden;
        min-height: 100vh;
        background-color: var(--bg-color);
        color: var(--text-color);
        padding-bottom: 4rem;
        header {
            min-height: 5rem;
        }
	}
</style>
