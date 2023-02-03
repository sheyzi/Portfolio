<script>
	import Introduction from '$lib/Introduction.svelte';
	import About from '$lib/About.svelte';

	let aboutVisible = false;
</script>

<svelte:head>
	<title>Oluwaseyifunmi Oyefeso / Software Engineer</title>
</svelte:head>

<div class="md:flex h-screen">
	<!-- Work -->
	<div class=" md:flex w-full">
		<button on:click={() => (aboutVisible = false)} class="title shadow border-r-[1px] border-[#35353589]">
			<!-- {#if !aboutVisible} -->
			<iconify-icon class:active={!aboutVisible} class="icon" icon="carbon:dot-mark" />
			<!-- {/if} -->
			<p>Work</p>
		</button>
		<div class="overflow-scroll content" class:active={!aboutVisible}>
			<Introduction />
		</div>
	</div>

	<!-- About -->
	<div
		class="wrapper md:flex bg-[#191919] text-white z-[9999] about miny"
		class:active={aboutVisible}
	>
		<button on:click={() => (aboutVisible = true)} class="title">
			<!-- {#if aboutVisible} -->
			<iconify-icon class:active={aboutVisible} class="icon text-white" icon="carbon:dot-mark" />
			<!-- {/if} -->
			<p class="text-white">About</p>
		</button>

		<div class="overflow-scroll content pb-[20px]" class:active={aboutVisible}>
			<About />
		</div>
	</div>
	
</div>

<style>
	.title {
		font-size: max(13px,1.5278vw);
		margin: 0;
		padding: 0.5rem;
		cursor: pointer;
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 2.9vw;
	}

	.wrapper {
		transition: all 0.5s ease;
		position: fixed;
		height: 100vh;
		left: calc(100vw - 2.5rem);
		right: calc(-100vw - 2.5rem);
	}

	.wrapper.active {
		left: 2.5rem;
		right: 0;
	}

	.title p {
		writing-mode: vertical-rl;
		margin-top: 0.5rem;
	}

	.content {
		margin-right: 2.5rem;
		width: 100%;
		opacity: 0;
		transition: all 0.5s ease;
		color: white;
	}

	.content p {
		color: white;
	}

	.content.active {
		opacity: 1;
	}

	.wrapper.active .content {
		margin-right: 0;
	}

	.content::-webkit-scrollbar {
		display: none;
	}

	.icon {
		transform: scale(0);
		transition: all 1.5s ease;
	}

	.icon.active {
		transform: scale(1);
	}

	@media (max-width: 768px) {
		.title {
			width: 100%;
			flex-direction: row;
			align-items: center;
			font-size: 1.2rem;
			height: 2.5rem;
		}
		.title p {
			writing-mode: horizontal-tb;
			margin: 0;
			margin-left: 5px;
		}

		.wrapper {
			left: 0;
			right: 0;
			bottom: 0;
			top: calc(100vh - 2.5rem);
		}

		.wrapper.active {
			top: 2.5rem;
			left: 0;
		}
	}
</style>
