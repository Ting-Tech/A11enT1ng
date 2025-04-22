<script lang="ts">
	// import welcome from '$lib/images/svelte-welcome.webp';
	import me from '$lib/images/me-line.jpg';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import {
		Github,
		Youtube,
		MapPinned,
		Phone,
		Mail,
		Send,
		Facebook,
		Instagram,
		Linkedin
	} from 'lucide-svelte';

	const skills = [
		{
			title: 'Operation System',
			data: [
				{
					name: 'Linux',
					src: 'https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black'
				},
				{
					name: 'Debian',
					src: 'https://img.shields.io/badge/Debian-D70A53?style=for-the-badge&logo=debian&logoColor=white'
				},
				{
					name: 'Ubuntu',
					src: 'https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white'
				},
				{
					name: 'Fedora',
					src: 'https://img.shields.io/badge/Fedora-294172?style=for-the-badge&logo=fedora&logoColor=white'
				},
				{
					name: 'Kalilinux',
					src: 'https://img.shields.io/badge/Kali-268BEE?style=for-the-badge&logo=kalilinux&logoColor=white'
				},
				{
					name: 'OpenWRT',
					src: 'https://img.shields.io/badge/OpenWRT-00B5E2?style=for-the-badge&logo=OpenWrt&logoColor=white'
				},
				{
					name: 'MacOS',
					src: 'https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0'
				},
				{
					name: 'Windows',
					src: 'https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white'
				}
			]
		},
		{
			title: 'Editor',
			data: [
				{
					name: 'VSCode',
					src: 'https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white'
				},
				{
					name: 'Vim',
					src: 'https://img.shields.io/badge/Vim-019733?style=for-the-badge&logo=vim&logoColor=white'
				},
				{
					name: 'Helix',
					src: 'https://img.shields.io/badge/Helix-%2328153e.svg?style=for-the-badge&logo=helix&logoColor=white'
				}
			]
		},
		{
			title: 'Language',
			data: [
				{
					name: 'C',
					src: 'https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white'
				},
				{
					name: 'C++',
					src: 'https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white'
				},
				{
					name: 'Python',
					src: 'https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white'
				},
				{
					name: 'PowerShell',
					src: 'https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white'
				},
				{
					name: 'JavaScript',
					src: 'https://img.shields.io/badge/JavaScript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E'
				},
				{
					name: 'TypeScript',
					src: 'https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white'
				},
				{
					name: 'HTML5',
					src: 'https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white'
				},
				{
					name: 'CSS3',
					src: 'https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white'
				},
				{
					name: 'Golang',
					src: 'https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white'
				},
				{
					name: 'Markdown',
					src: 'https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white'
				},
				{
					name: 'JSON',
					src: 'https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white'
				},
				{
					name: 'R',
					src: 'https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white'
				},
				{
					name: 'Ruby',
					src: 'https://img.shields.io/badge/ruby-%23CC342D.svg?style=for-the-badge&logo=ruby&logoColor=white'
				},
				{
					name: 'Rust',
					src: 'https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white'
				}
			]
		},
		{
			title: ' Framework',
			data: [
				{
					name: 'React',
					src: 'https://img.shields.io/badge/React-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB'
				},
				{
					name: 'Svelte',
					src: 'https://img.shields.io/badge/Svelte-FF3E00?style=for-the-badge&logo=svelte&logoColor=white'
				},
				{
					name: 'SvelteKit',
					src: 'https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white'
				},
				{
					name: 'Tailwind CSS',
					src: 'https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white'
				},
				{
					name: 'UnoCSS',
					src: 'https://img.shields.io/badge/unocss-333333.svg?style=for-the-badge&logo=unocss&logoColor=white'
				},
				{
					name: 'vite',
					src: 'https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white'
				},
				{
					name: 'Bun',
					src: 'https://img.shields.io/badge/bun-%23FFA500.svg?style=for-the-badge&logo=bun&logoColor=white'
				},
				{
					name: 'Vue',
					src: 'https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D'
				},
				{
					name: 'AntDesign',
					src: 'https://img.shields.io/badge/-AntDesign-%230170FE?style=for-the-badge&logo=ant-design&logoColor=white'
				},
				{
					name: 'Chart.js',
					src: 'https://img.shields.io/badge/chart.js-F5788D.svg?style=for-the-badge&logo=chart.js&logoColor=white'
				},
				{
					name: 'Express.js',
					src: 'https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB'
				},
				{
					name: 'Framwork7',
					src: 'https://img.shields.io/badge/framework7-%23EE350F.svg?style=for-the-badge&logo=framework7&logoColor=white'
				},
				{
					name: 'MUI',
					src: 'https://img.shields.io/badge/MUI-%230081CB.svg?style=for-the-badge&logo=mui&logoColor=white'
				},
				{
					name: 'NestJS',
					src: 'https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white'
				},
				{
					name: 'Next JS',
					src: 'https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white'
				},
				{
					name: 'Node.js',
					src: 'https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white'
				},
				{
					name: 'Nuxt JS',
					src: 'https://img.shields.io/badge/Nuxt-002E3B?style=for-the-badge&logo=nuxtdotjs&logoColor=#00DC82'
				},
				{
					name: 'OpenCV',
					src: 'https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white'
				},
				{
					name: 'PNPM',
					src: 'https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220'
				},
				{
					name: 'Tauri',
					src: 'https://img.shields.io/badge/tauri-%2324C8DB.svg?style=for-the-badge&logo=tauri&logoColor=%23FFFFFF'
				}
			]
		},
		{
			title: 'Database',
			data: [
				{
					name: 'MySQL',
					src: 'https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white'
				},
				{
					name: 'PostgreSQL',
					src: 'https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white'
				},
				{
					name: 'MongoDB',
					src: 'https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white'
				}
			]
		},
		{
			title: 'Design',
			data: [
				{
					name: 'Figma',
					src: 'https://img.shields.io/badge/Figma-0AC97C?style=for-the-badge&logo=figma&logoColor=white'
				},
				{
					name: 'Canva',
					src: 'https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white'
				},
				{
					name: 'Final Cut Pro',
					src: 'https://img.shields.io/badge/Final%20Cut%20Pro-000000?style=for-the-badge&logo=finalcutpro&logoColor=white'
				}
			]
		},
		{
			title: 'Other',
			data: [
				{
					name: 'Git',
					src: 'https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white'
				},
				{
					name: 'GitHub',
					src: 'https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white'
				},
				{
					name: 'Docker',
					src: 'https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white'
				},
				{
					name: 'CMake',
					src: 'https://img.shields.io/badge/CMake-%23008FBA.svg?style=for-the-badge&logo=cmake&logoColor=white'
				},
				{
					name: 'ESLint',
					src: 'https://img.shields.io/badge/ESLint-4B3263?style=for-the-badge&logo=eslint&logoColor=white'
				},
				{
					name: 'Prettier',
					src: 'https://img.shields.io/badge/Prettier-FFB800?style=for-the-badge&logo=prettier&logoColor=black'
				},
				{
					name: 'Jira',
					src: 'https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white'
				},
				{
					name: 'Notion',
					src: 'https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white'
				},
				{
					name: 'AnyType',
					src: 'https://img.shields.io/badge/AnyType-000000?style=for-the-badge&logo=anytype&logoColor=white'
				},
				{
					name: 'Raspberry Pi',
					src: 'https://img.shields.io/badge/-Raspberry_Pi-C51A4A?style=for-the-badge&logo=Raspberry-Pi'
				},
				{
					name: 'Swagger',
					src: 'https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white'
				},
				{
					name: 'PicoCTF',
					src: 'https://img.shields.io/badge/PicoCTF-FF4B00?style=for-the-badge&logo=picoctf&logoColor=white'
				},
				{
					name: 'Apple Music',
					src: 'https://img.shields.io/badge/Apple_Music-9933CC?style=for-the-badge&logo=apple-music&logoColor=white'
				}
			]
		}
	];

	const Experiences = [
		{
			title: 'Tech & Robot',
			data: [
				{
					name: '2014 - 2018 Power Tech International Robot Contest - Bronze Medal🥉 - Gold Medal🥇',
					description: ''
				},
				{
					name: '2019 TIRT All-Robot International Invitational Tournament - Bronze Medal🥉',
					description: ''
				},
				{
					name: '2020 National Skills Competition robotics Central Division - Gold Medal🥇',
					description: ''
				},
				{
					name: '2020 National Skills Competition robotics - 6th Place',
					description: ''
				},
				{
					name: '2021 National Skills Competition robotics Central Division - Silver Medal🥈',
					description: ''
				},
				{
					name: '2021 National Skills Competition robotics - Gold Medal🥇',
					description: ''
				}
			]
		},
		{
			title: 'Invention',
			data: [
				{ name: 'Taiwan Innovation Expo - Distinguished Inventor Pavilion', description: '' },
				{
					name: '2016 Concours Lépine International Paris - Gold Medal🥇',
					description: ''
				},
				{
					name: 'Competition at the International Exhibition of Inventions in Paris, France and Special Prize in Poland - Gold Medal🥇',
					description: ''
				},
				{
					name: 'Competition at the International Invention Exhibition in Brussels, Belgium - Bronze Medal🥉',
					description: ''
				},
				{
					name: 'The 5th Suzhou-Taiwan Youth Creativity and Innovation Competition 2019 - Silver Medal🥈',
					description: ''
				},
				{
					name: 'Ministry of Education National Higher Secondary School Professional Cluster - 110 Years Project and Creative Production Competition - Masterpiece',
					description: ''
				}
			]
		},
		{
			title: 'Verification',
			data: [
				{
					name: 'Miaoli County Gifted and Talented Program for the 105th School Year and Gifted and Talented in the Arts Assessment',
					description: ''
				},
				{
					name: "Miaoli County's 103～105 First Half Year Out-of-School Expert and Teacher Model Support Program for Gifted Education-Creative Invention Field",
					description: ''
				},
				{
					name: 'Prague Music Certification - 9 Grades',
					description: ''
				}
			]
		},
		{
			title: 'Work',
			data: [
				{
					name: 'REMISYS',
					description:
						'Robotics Instructor, Robotics Research Engineer, Robotics Maintenance Engineer'
				},
				{
					name: 'Bidbuy4u',
					description: 'EV3 LEGO Robotics Instructor'
				},
				{
					name: 'Photon Future 光速未來有限公司',
					description: 'Front-end Engineer'
				}
			]
		},
		{
			title: 'Now',
			data: [{ name: 'Studying in NTUST', description: '' }]
		}
	];
</script>

<svelte:head>
	<title>About Me</title>
	<meta name="description" content="Allen's website" />
</svelte:head>

<section class="flex flex-row flex-wrap justify-start items-center p-0 m-0 h-screen sm:flex-nowrap">
	<aside class="flex w-1/2 h-auto sm:1/2">
		<picture class="w-full h-auto sm:w-[60%]">
			<img src={me} alt="me" />
		</picture>
	</aside>
	<article class="w-full sm:w-2/3">
		<h1 class="text-[32px] font-bold sm:text-xl">Hey, this is Allen</h1>
		I'm a college student and I love adventure, computer science, music, and photography.
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Skills & Interests</h1>
	<article>
		<section class="flex flex-col gap-4">
			{#each skills as { title, data }}
				<h1 class="text-xl">
					{title}
					<article class="flex flex-row gap-2 flex-wrap">
						{#each data as { name, src }}
							<img alt={name} {src} />
						{/each}
					</article>
				</h1>
			{/each}
		</section>
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Experiences</h1>
	<article>
		<section>
			<div
				class="grid grid-row-[max-content_1px_1fr] gap-5 items-start sm:grid-cols-[max-content_1px_1fr] sm:gap-10"
			>
				{#each Experiences as { title, data }}
					<h1 class="text-2xl font-bold">{title}</h1>
					<Separator class="h-full sm:block hidden sm:orientation-horizontal" />
					<article class="flex flex-col gap-5">
						{#each data as { name, description }}
							<div class="flex flex-col gap-2">
								<h2>{name}</h2>
								{#if description}
									<p>{description}</p>
								{/if}
							</div>
						{/each}
					</article>
				{/each}
			</div>
		</section>
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Contact Me</h1>
	<article>
		<section class="flex flex-col gap-4">
			<a
				class="flex flex-row items-center gap-2"
				href="https://maps.app.goo.gl/yRhGqYAGgVU8oYXJ7?g_st=com.google.maps.preview.copy"
			>
				<MapPinned strokeWidth={1} class="h-10 w-10" />
				Taiwan (R.O.C.)
			</a>
			<a class="flex flex-row items-center gap-2" href="tel:+886978247835">
				<Phone strokeWidth={1} class="h-10 w-10" />
				Phone: +886 978247835
			</a>
			<a class="flex flex-row items-center gap-2" href="mailto:allen0523win@gmail.com">
				<Mail strokeWidth={1} class="h-10 w-10" />
				Email: allen0523win@gmail.com
			</a>
			<a class="flex flex-row items-center gap-2" href="https://t.me/AllenTing">
				<Send strokeWidth={1} class="h-10 w-10" />
				@AllenTing
			</a>
		</section>
	</article>
</section>

<section>
	<h1 class="mb-5 text-[40px]">Social Media</h1>
	<article>
		<section class="flex flex-col gap-4">
			<a class="flex flex-row items-center gap-2" href="https://github.com/Ting-Tech">
				<Github strokeWidth={1} class="h-10 w-10" />
				Ting-Tech
			</a>
			<a
				class="flex flex-row items-center gap-2"
				href="https://youtube.com/@studiovideography1618?si=MelXKRk3JyuPxNeE"
			>
				<Youtube strokeWidth={1} class="h-10 w-10" />
				Studio Videography
			</a>
			<a
				class="flex flex-row items-center gap-2"
				href="https://www.facebook.com/share/16RutnVqY5/?mibextid=wwXIfr"
			>
				<Facebook strokeWidth={1} class="h-10 w-10" />
				Allen Ting
			</a>
			<a
				class="flex flex-row items-center gap-2"
				href="https://www.instagram.com/allen_ting.0523?igsh=MTB3YnJqcjVtZzFybg%3D%3D&utm_source=qr"
			>
				<Instagram strokeWidth={1} class="h-10 w-10" />
				allen_ting.0523
			</a>
			<a class="flex flex-row items-center gap-2" href="https://www.linkedin.com/in/allen523">
				<Linkedin strokeWidth={1} class="h-10 w-10" />
				鄭健廷(Allen)
			</a>
		</section>
	</article>
</section>
