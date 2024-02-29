<script lang="ts">
    import Icon from './icon.svelte';
</script>

<footer class="h-48 bg-black/30 mt-12 p-12">
    <div class="flex h-full w-full justify-center items-center gap-4">
        <a
            href="https://github.com/Squshy"
            target="_blank"
            aria-label="My GitHub page"
        >
            <Icon
                name="GitHub"
                class="w-8 h-8 flex hover:scale-110 transition duration-100 ease-out fill-white/70 hover:fill-white"
            />
        </a>
        <a
            href="https://linkedin.com/in/calvin-lapp"
            target="_blank"
            aria-label="My LinkedIn profile"
        >
            <Icon
                name="LinkedIn"
                class="w-8 h-8 flex hover:scale-110 transition duration-100 ease-out fill-white/70 hover:fill-white"
            />
        </a>
        <a
            href="mailto:lapp.cd@gmail.com"
            target="_blank"
            aria-label="Email me :^)"
        >
            <Icon
                name="Mail"
                class="w-8 h-8 flex hover:scale-110 transition duration-100 ease-out fill-white/70 hover:fill-white"
            />
        </a>
    </div>
</footer>
