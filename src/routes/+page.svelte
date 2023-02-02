<script>
	let aboutVisible = false;
</script>

<svelte:head>
	<title>Oluwaseyifunmi Oyefeso / Software Engineer</title>
</svelte:head>

<div class="md:flex justify-between h-screen">
	<!-- Work -->
	<div class="flex ">
		<button on:click={() => (aboutVisible = false)} class="title">
			{#if !aboutVisible}
				<iconify-icon icon="carbon:dot-mark" />
			{/if}
			<p>Work</p>
		</button>
		<div class="overflow-scroll content" class:active={!aboutVisible}>
			<p class="h-screen">
				Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe voluptate obcaecati quidem
				voluptatum beatae perspiciatis accusantium at ex! Consectetur iste voluptate neque soluta
				magni tempora voluptates officia sit amet facere.
			</p>

			<p class="h-screen">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum temporibus aliquam, et
				porro aspernatur earum! Iste perferendis dolorum, aut possimus blanditiis sed dicta, illo
				omnis, impedit mollitia voluptates odit ab.
			</p>
		</div>
	</div>

	<!-- About -->
	<div class="flex bg-black text-white z-[9999]">
		<button on:click={() => (aboutVisible = true)} class="title">
			{#if aboutVisible}
				<iconify-icon icon="carbon:dot-mark" />
			{/if}
			<p>About</p>
		</button>

		<div class="overflow-scroll content" class:active={aboutVisible}>
			<p class="h-screen">
				Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe voluptate obcaecati quidem
				voluptatum beatae perspiciatis accusantium at ex! Consectetur iste voluptate neque soluta
				magni tempora voluptates officia sit amet facere.
			</p>

			<p class="h-screen">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum temporibus aliquam, et
				porro aspernatur earum! Iste perferendis dolorum, aut possimus blanditiis sed dicta, illo
				omnis, impedit mollitia voluptates odit ab.
			</p>
		</div>
	</div>
</div>

<style>
	.title {
		font-size: 1.5rem;
		margin: 0 auto;
		padding: 0.5rem;
		cursor: pointer;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.title p {
		writing-mode: vertical-rl;
		margin-top: 0.5rem;
	}

	.content {
		transform: scaleX(0);
		width: 0;
		transition: transform 0.5s ease-in-out;
		transform-origin: left;
	}

	.content.active {
		width: 100%;
		transform: scaleX(1);
	}

	.content::-webkit-scrollbar {
		display: none;
	}
</style>
