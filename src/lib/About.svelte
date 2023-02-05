<script>
	import Footer from './Footer.svelte';
	export let aboutVisible;
	
</script>

<section class="text-white md:pt-[20px] z-[99999] container pb-[4em]">
	<section class="about-top-container">
		<div class="about-top ">
			<h2 class="item-1 text-white">
				I create beautiful responsive websites. My flexibility as an independent developer means
				more dedication to enliven creative and interactive designs, all with natural usability at
				their core. Years of agency experience equips me to work closely with designers and
				developers to deliver on projects in an optimised and thorough way.
			</h2>
			<div class="item-2 ">
				<div class="about-top-contact text-white mb-2">
					<p class=" text-[hsla(0,0%,94.1%,.5)]">Mail</p>

					<p class="flex items-center text-[white] ">
						<iconify-icon class="text-white" icon="carbon:dot-mark" width="20" />
						<a href="mailto:gistkiosk@gmail.com" class="text-white ">gistkiosk@gmail.com</a>
					</p>
				</div>
				<div class="about-top-contact text-white ">
					<p class=" text-[hsla(0,0%,94.1%,.5)]">Linkedin</p>

					<p class="flex items-center text-[white] ">
						<iconify-icon class="text-white" icon="carbon:dot-mark" width="20" />
						<a href="https://www.linkedin.com/in/oluwaseyifunmi-oyefeso-29181b263" class="text-white ">Linkedin.com</a>
					</p>
				</div>
			</div>
		</div>
	</section>

	<section class="stack-container mt-[20em] md:mt-auto mb-[8em]">
		<div
			class="stack mr-[20px] pt-[1em] ml-[20px] border-t border-white flex flex-col gap-[3em] md:gap-0 md:flex-row"
		>
			<h3 class="w-[60%] text-white text-3xl">My stack</h3>

			<ul class="text-white text-[45px] ml-[3em]">
				<li>Sveltekit</li>
				<li>NestJS</li>
				<li>FastApi</li>
				<li>Flutter</li>
				<li>Docker</li>
			</ul>
		</div>
	</section>

	<section class="client-list-container">
		<div
			class="stack mr-[20px] pt-[1em] ml-[20px] border-t mb-[10em] border-white flex-col gap-[2em] md:gap-[7em] flex"
		>
			<h3 class=" text-white text-2xl">Client list</h3>

			<p class="text-white text-[45px]">
				Cooversa, Dept, Kontrapunkt, AM Copenhagen, Kontainer, Day21, Studio GD, Eksakte, Lousiana,
				Betty Nansen, Snedkernes Efterårsudstilling, Det Danske Akademi, Specsavers, Beatroot
				Studio, Grant Compass, Uruggo
			</p>
		</div>
	</section>
	<!-- 
	<section class="work-experience-container">
		<div class="border-t-[10px] mx-[20px] pt-2 border-white">
			<h2 class="text-white text-4xl">Work Experience</h2>
			<table>
				<tr>
					<th>Header 1</th>
					<th>Header 2</th>
				</tr>
				<tr>
					<td>Row 1, Column 1</td>
					<td>Row 1, Column 2</td>
				</tr>
				<tr>
					<td>Row 2, Column 1</td>
					<td>Row 2, Column 2</td>
				</tr>
			</table>
		</div>
	</section> -->

	<section class="footer-container mb:mb-0 ">
		<Footer {aboutVisible}/>
	</section>
</section>

<style>
	*{
		transition: all 0.5s ease;
	}
	.about-top {
		--grid-columns: 9;
		--grid-gap: 8px;
		display: grid;
		grid-column-gap: var(--grid-gap);
		grid-template-columns: repeat(var(--grid-columns), minmax(0, 1fr));
		margin-left: 20px;
		margin-right: 20px;
	}
	.item-1 {
		grid-column: 2/-1;
		letter-spacing: -0.06em;
		line-height: 105%;
		font-size: max(30px, 3.2vw);
	}
	.item-2 {
		grid-column: 1 / span 4;
		font-size: min(5vw, 28px);
		align-self: end;
		margin-top: 70px;
	}
	.about-top-contact {
		display: grid;
		grid-column-gap: 8px;
		grid-template-columns: 1fr 3fr;
	}
	ul {
		list-style-type: none;
	}
	ul > li {
		color: white;
	}
	p,
	li {
		letter-spacing: -0.06em;
		line-height: 105%;
	}
	.about-top-container {
		padding-top: 20px;
		padding-bottom: 120px;
		height: max(calc(100vh - 100px), 580px);
	}
	.container{
	  height: 100vh;
	}
	@media (max-width: 768px) {
		.about-top-container {
			padding-top: 48px;
			padding-bottom: 120px;
		}
		.item-1 {
			grid-column: 1/-1;
			font-size: min(10vw, 60px);
		}
		.item-2 {
			grid-column: 1/-1;
			align-self: end;
			margin-top: 70px;
		}
	}
</style>
