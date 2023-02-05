<script lang="ts">
	import Introduction from '$lib/Introduction.svelte';
	import About from '$lib/About.svelte';
	import Works from '$lib/Works.svelte';
	import Footer from '$lib/Footer.svelte';
	import { browser } from '$app/environment';

	if (browser) {
		// g
		window.addEventListener('scroll', (e) => {
			let pinElement: any = document.querySelector('.pinned');
			let bottom : any = document.querySelector('.down');
			// if (!aboutVisible) {
			// 	pinElement.style.position = 'sticky';
			// 	pinElement.style.top = 0;

			// 	if (aboutVisible === false) {
			// 		pinElement.style.zIndex = 0;
			// 	} else pinElement.style.zIndex = 1;
			// }
			pinElement.style.position = 'sticky';
			const y = window.pageYOffset;

			if (y >= 0 && y <= 500) {
				pinElement.style.top = 0;
			}
			if ( y >= 1000) {
				bottom.style.display = 'block'
			}
			else bottom.style.display = 'none'
		});
		console.log(window);
	}

	$: aboutVisible = false;
</script>

<svelte:head>
	<title>Oluwaseyifunmi Oyefeso / Software Engineer</title>
</svelte:head>

<button
	on:click={() => (aboutVisible = false)}
	class="shadow-lg md:shadow-none  z-[99999] fixed md:h-full title bg-white border-r-[1px] border-[#e6e6e6]"
>
	<!-- {#if !aboutVisible} -->
	<iconify-icon class:active={!aboutVisible} class="icon" icon="carbon:dot-mark" />
	<!-- {/if} -->
	<p>Work</p>
</button>

<div class="md:flex flex-col pinned">
	<!-- Work -->
	<div class=" md:flex w-full  pinned">
		<div class="overflow-scroll content w-full" class:active={!aboutVisible}>
			<Introduction />
		</div>
	</div>
	
</div>
<div
	class="wrapper md:flex bg-[#191919] fixed top-0 text-white z-[9999] about"
	class:active={aboutVisible}
>
	<button on:click={() => (aboutVisible = true)} class="title">
		<!-- {#if aboutVisible} -->
		<iconify-icon class:active={aboutVisible} class="icon text-white" icon="carbon:dot-mark" />
		<!-- {/if} -->
		<p class="text-white">About</p>
	</button>
	<div class="overflow-scroll content pb-[30px] z-[999999] " class:active={aboutVisible}>
		<About {aboutVisible}/>
	</div>
</div>

<div class=" work-experience-container pt-[50px] md:mx-[2.5rem] bg-white ">
	<div class="mx-[20px] border-t border-black mb-5" />
	<div class="mx-[20px] flex md:w-[1000px] justify-between md:text-3xl text-xl md:mb-[2em] mb-[1em]">
		<p>Selected work</p>
		<p>2023 - 2020</p>
	</div>

	<section class=" mx-[20px] flex flex-col gap-[10em] pb-[2em]">
		<Works />
		<Works />
		<Works />
		<Works />
	</section>
</div>

<section class="footer-container sticky bottom-0 down md:mx-[2.5rem] bg-white">
		<Footer {aboutVisible}/>
	</section>

<style>
	.title {
		font-size: max(13px, 1.5278vw);
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
		height: 100vh;
		left: calc(100vw - 2.5rem);
		right: calc(-100vw - 2.5rem);
		position: fixed;
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
		margin-left: 2.5rem;
		width: 100%;
		opacity: 0;
		transition: all 0.5s ease;
		color: white;
	}

	p,
	h2,
	h3 {
		letter-spacing: -0.06em;
		line-height: 105%;
	}

	.content.active {
		opacity: 1;
		position: relative;
	}

	.wrapper.active .content {
		margin-right: 0;
		margin-left: 0;
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

	.work-experience-container {
		min-height: 100vh;
		position: relative;
		top: 0em;
		z-index: 999;
	}
	.down{
		display: none;
	}
	@media (max-width: 768px) {
		.title {
			width: 100%;
			flex-direction: row;
			align-items: center;
			font-size: 1.63rem;
			height: 50px;
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

		.content {
			margin-left: 0;
			padding-top: 50px;
		}
		.wrapper.active {
			top: 2.5rem;
			left: 0;
		}
	}
</style>
