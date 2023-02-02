<section class="text-white h-[100vh] w-full pt-[20px]">
	<section class="about-top-container">
		<h2 class="item-1 text-white">
			I create beautiful responsive websites. My flexibility as an independent developer means more
			dedication to enliven creative and interactive designs, all with natural usability at their
			core. Years of agency experience equips me to work closely with designers and developers to
			deliver on projects in an optimised and thorough way.
		</h2>
		<div class="item-2 ">
			<div class="about-top-contact text-white">
				<p class="text-xl text-[hsla(0,0%,94.1%,.5)]">Mail</p>

				<p class="flex items-center text-[white] h-full text-xl">
					<iconify-icon class="text-white" icon="carbon:dot-mark" width="20" />
					<a href="mailto:gistkiosk@gmail.com" class="text-white ">gistkiosk@gmail.com</a>
				</p>
			</div>
			<div class="about-top-contact text-white">
				<p class="text-xl text-[hsla(0,0%,94.1%,.5)]">Linkedin</p>

				<p class="flex items-center text-[white] h-full text-xl">
					<iconify-icon class="text-white" icon="carbon:dot-mark" width="20" />
					<a href="mailto:gistkiosk@gmail.com" class="text-white ">Linkedin.com</a>
				</p>
			</div>
		</div>
	</section>

	<section class="favourite-stack-container">
        <div class="favourite-stack mr-[20px] ml-[20px] border-t border-white">

        </div>
    </section>
</section>

<style>
	
	.about-top-container {
		height: max(calc(100vh - 100px),580px);
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
	}
	.about-top-contact {
		display: grid;
		grid-column-gap: 8px;
		grid-template-columns: 1fr 3fr;
	}
</style>
