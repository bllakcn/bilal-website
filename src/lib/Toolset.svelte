<script>
	import reactlogo from './assets/react.png';
	import sveltelogo from './assets/svelte.png';
	import nextjslogo from './assets/nextjs.png';
	import htmllogo from './assets/html.png';
	import csslogo from './assets/css.png';
	import jslogo from './assets/js.png';
	import typescriptlogo from './assets/typescript.png';
	import tailwindlogo from './assets/tailwind.png';
	import pslogo from './assets/ps.png';
	import ailogo from './assets/ai.png';
	import lrlogo from './assets/lr.png';
	import xdlogo from './assets/xd.png';
	import splinelogo from './assets/spline.png';
	import sasslogo from './assets/sass.png';

	const frontSkills = [
		{ logo: htmllogo, name: 'HTML', id: 1 },
		{ logo: csslogo, name: 'CSS', id: 2 },
		{ logo: jslogo, name: 'Javascript', id: 3 },
		{ logo: typescriptlogo, name: 'TypeScript', id: 4 },
		{ logo: reactlogo, name: 'React', id: 5 },
		{ logo: nextjslogo, name: 'Nextjs', id: 6 },
		{ logo: sveltelogo, name: 'Svelte', id: 7 },
		{ logo: sasslogo, name: 'Sass', id: 8 },
		{ logo: tailwindlogo, name: 'Tailwindcss', id: 9 }
	];
	const contentSkills = [
		{ logo: pslogo, name: 'Adobe Photoshop', id: 1 },
		{ logo: ailogo, name: 'Adobe Illustrator', id: 2 },
		{ logo: xdlogo, name: 'Adobe Xd', id: 3 },
		{ logo: lrlogo, name: 'Adobe Lightroom', id: 4 },
		{ logo: splinelogo, name: 'Spine', id: 5 }
	];
</script>

<section id="toolset" class="bg-black text-neutral-300 flex flex-col justify-center pb-16">
	<h3 class="text-center text-neutral-200 text-xl my-10">
		My <span class="highlight-tools relative z-10 text-2xl font-black">Toolset</span>
	</h3>
	<div class="mx-auto text-center">
		<p class="font-thin mx-6 text-sm tracking-widest">Front-end development</p>
		<div class="grid ml-0 p-4 grid-cols-3 justify-center md:grid-cols-9 gap-5 grey-filtered">
			{#each frontSkills as frontSkill (frontSkill.id)}
				<img title={frontSkill.name} class="w-12" src={frontSkill.logo} alt={frontSkill.name} />
			{/each}
		</div>
	</div>
	<div class="mx-auto text-center">
		<p class="font-thin mx-6 text-sm tracking-widest">Content Creation</p>
		<div class="grid ml-0 p-4 grid-cols-3 md:grid-cols-5 gap-5 grey-filtered">
			{#each contentSkills as contentSkill (contentSkill.id)}
				<img
					title={contentSkill.name}
					class="w-12"
					src={contentSkill.logo}
					alt={contentSkill.name}
				/>
			{/each}
		</div>
	</div>
</section>

<style>
	.grey-filtered img {
		filter: grayscale(95%);
		transition: filter 0.2s ease-out;
	}
	.grey-filtered img:hover {
		filter: grayscale(0);
	}
	.highlight-tools::before {
		content: '';
		width: 100px;
		height: 20px;
		left: -5px;
		bottom: -4px;
		background-color: rgba(49, 46, 129, 0.5);
		position: absolute;
		z-index: -1;
	}
</style>
