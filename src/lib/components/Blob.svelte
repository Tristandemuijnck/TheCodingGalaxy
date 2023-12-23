<script>
    export let topAbsolute = "initial"
    export let leftAbsolute = "initial"
    export let bottomAbsolute = "initial"
    export let rightAbsolute = "initial"
    export let blobWidth = "150px"
    export let rotateBlob = "initial"
</script>

<div class="blob" style="--top-absolute: {topAbsolute}; --left-absolute: {leftAbsolute}; --rotate-blob: {rotateBlob}; --bottom-absolute: {bottomAbsolute}; --right-absolute: {rightAbsolute}">
	<div class="blob__inner" style="--blob-width: {blobWidth}">
		<img src="/images/galaxy.jpg" alt="" />
	</div>
</div>

<style>
	.blob {
		display: flex;
		justify-content: center;
		align-items: center;
        position: absolute;
        top: var(--top-absolute);
        left: var(--left-absolute);
        bottom: var(--bottom-absolute);
        right: var(--right-absolute);
        transform: rotateX(var(--rotate-blob));
	}

	.blob__inner {
		animation: morph 6s linear infinite;
		border-radius: 40% 60% 70% 30%/40% 50% 60% 50%;
		width: var(--blob-width);
		height: var(--blob-width);
		overflow: hidden;
	}

	.blob__inner img {
		width: 100%;
        height: 100%;
        object-fit: cover;
	}

	@keyframes morph {
		0%,
		100% {
			border-radius: 40% 60% 70% 30%/40% 40% 60% 50%;
		}
		34% {
			border-radius: 70% 30% 50% 50%/30% 30% 70% 70%;
		}
		67% {
			border-radius: 100% 60% 60% 100%/100% 100% 60% 60%;
		}
	}
</style>
