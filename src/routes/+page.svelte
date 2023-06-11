<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<style lang="scss">
    h1 {
        @include breakpoint.up("xs") {
            color: red;
        }
        @include breakpoint.up("sm") {
            color: orange;
        }
        @include breakpoint.up("md") {
            color: blue;
        }
        @include breakpoint.up("lg") {
            color: green;
        }
        @include breakpoint.up("xl") {
            color: purple;
        }
    }
</style>