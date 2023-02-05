<script lang="ts">
	export let aboutVisible: boolean;
</script>

<div class="footer mx-[20px] flex flex-col mb-[150px] md:mb-[10px]">
	<div class="flex w-full md:items-end mb-4 flex-col md:flex-row ">
		<h1
			class="{aboutVisible
				? 'text-white'
				: 'text-[#191919]'} w-full text-[4.5em] md:text-[12em] md:h-[220px] tracking-[-0.06em] md:mr-auto"
		>
			Get in touch
		</h1>
		<div class="{aboutVisible ? 'w-[190px]' : 'w-[250px]'} items-start flex flex-col">
			<div class=" text-white mb-2">
				<p class="flex items-center {aboutVisible ? 'text-white' : 'text-[#191919]'} text-xl">
					<iconify-icon
						class={aboutVisible ? 'text-white' : 'text-[#191919]'}
						icon="carbon:dot-mark"
						width="20"
					/>
					<a
						href="mailto:gistkiosk@gmail.com"
						class="{aboutVisible ? 'text-white' : 'text-[#191919]'} ">gistkiosk@gmail.com</a
					>
				</p>
			</div>
			<div class="about-top-contact text-white mb-1">
				<p class="flex items-center {aboutVisible ? 'text-white' : 'text-[#191919]'} text-xl">
					<iconify-icon
						class={aboutVisible ? 'text-white' : 'text-[#191919]'}
						icon="carbon:dot-mark"
						width="20"
					/>
					<a
						href="https://www.linkedin.com/in/oluwaseyifunmi-oyefeso-29181b263"
						class="{aboutVisible ? 'text-white' : 'text-[#191919]'} ">Linkedin.com</a
					>
				</p>
			</div>
		</div>
	</div>
	<div class="flex flex-col md:gap-3 gap-2 md:mb-5 mb-2">
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
		<div class="border-t-[7px] {aboutVisible ? 'border-white' : 'border-black'}" />
	</div>
	<div class="flex w-full justify-between md:text-xl text-white mb-5">
		<p class={aboutVisible ? 'text-white' : 'text-[#191919]'}>Oluwaseyifunmi Oyefeso</p>
		<p class={aboutVisible ? 'text-white' : 'text-[#191919]'}>© 2023</p>
	</div>
</div>
