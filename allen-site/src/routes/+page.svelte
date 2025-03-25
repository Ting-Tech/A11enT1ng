<script lang="ts">
	// import welcome from '$lib/images/svelte-welcome.webp';
	import me from '$lib/images/me.jpg';
	import Separator from '$lib/components/ui/separator/separator.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Allen's website" />
</svelte:head>

<section class="flex flex-row justify-between items-center p-0 m-0">
	<aside class="about">
		<picture>
			<!-- <source srcset={welcome} type="image/webp" /> -->
			<img src={me} alt="me" />
		</picture>
	</aside>
	<article class="w-1/2">
		<h1 class="text-xl font-bold">Hi, my name is Allen.</h1>
		I'm a college student and I love adventure, computer science, music, and photography.
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Experience</h1>
	<!-- <Separator class="my-5" /> -->
	<article>
		<section class="flex flex-row gap-10">
			<h1 class="w-[10%]">Competition</h1>
			<Separator orientation="vertical" />
			<article class="flex flex-col gap-5">
				<div>
					<h2 class="font-bold">2016 Concours Lépine International Paris - Gold Medal🥇</h2>
					<p>
						I was identified as a gifted student in creativity as early as 2014 and have
						continuously participated in the “Model Teacher” program. Throughout my learning
						journey, I have been studying under my mentor, 陳鴻偉(Chen Hong-Wei), embracing the
						philosophy of creativity: Innovation, Play, Aesthetics, and Humanistic(創、遊、美、人)!
					</p>
				</div>
				<div>
					<h2 class="font-bold">2021 National Skills Competition robotics - Gold Medal🥇</h2>
					<!-- <p>I have been playing robotics since 2014.</p> -->
				</div>
			</article>
		</section>

		<section class="flex flex-row justify-start gap-10 pt-10">
			<h1 class="w-[10%]">Work</h1>
			<Separator orientation="vertical" />
			<article class="flex flex-col gap-5">
				<div>
					<h2 class="font-bold">REMISYS瑞明系統科技</h2>
					<p>外派機器人講師、機器人研發工程師、機器人維修工程師</p>
				</div>
				<div>
					<h2 class="font-bold">Bidbuy4u樂高必買站</h2>
					<p>EV3樂高機器人講師</p>
				</div>
				<div>
					<h2 class="font-bold">Photon Future光速未來有限公司</h2>
					<p>前端工程師</p>
				</div>
			</article>
		</section>
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Interests & Skills</h1>
</section>

<style>
	.about {
		display: flex;
		width: 40%;
		height: auto;
	}

	.about img {
		width: 100%;
		height: auto;
	}
</style>
