# flowbite Setup
## 프로젝트 구성
 flowbite-starter 사용
```Shell
npx degit shinokada/flowbite-svelte-starter ${프로젝트명}
cd ${프로젝트명}
npm install
npm run dev
```
flowbite-icon pack 설치
```Shell
pnpm i -D flowbite-svelte-icons
```
Theme 적용(tailwind.config.cjs 수정)
```Javascript
const config = {
	content: ['./src/**/*.{html,js,svelte,ts}', './node_modules/flowbite-svelte/**/*.{html,js,svelte,ts}'],

	plugins: [require('flowbite/plugin')],

	darkMode: 'class',

	theme: {
		extend: {
			colors: {
				// flowbite-svelte
				primary: {
					50: '#FFF5F2',
					100: '#FFF1EE',
					200: '#FFE4DE',
					300: '#FFD5CC',
					400: '#FFBCAD',
					500: '#FE795D',
					600: '#EF562F',
					700: '#EB4F27',
					800: '#CC4522',
					900: '#A5371B'
				}

				// pink
				// primary: {"50":"#fdf2f8","100":"#fce7f3","200":"#fbcfe8","300":"#f9a8d4","400":"#f472b6","500":"#ec4899","600":"#db2777","700":"#be185d","800":"#9d174d","900":"#831843"}

				// fuchsia
				// primary: {"50":"#fdf4ff","100":"#fae8ff","200":"#f5d0fe","300":"#f0abfc","400":"#e879f9","500":"#d946ef","600":"#c026d3","700":"#a21caf","800":"#86198f","900":"#701a75"}

				// purple
				// primary: {"50":"#faf5ff","100":"#f3e8ff","200":"#e9d5ff","300":"#d8b4fe","400":"#c084fc","500":"#a855f7","600":"#9333ea","700":"#7e22ce","800":"#6b21a8","900":"#581c87"}

				// violet
				// primary: {"50":"#f5f3ff","100":"#ede9fe","200":"#ddd6fe","300":"#c4b5fd","400":"#a78bfa","500":"#8b5cf6","600":"#7c3aed","700":"#6d28d9","800":"#5b21b6","900":"#4c1d95"}

				// indigo
				// primary: {"50":"#eef2ff","100":"#e0e7ff","200":"#c7d2fe","300":"#a5b4fc","400":"#818cf8","500":"#6366f1","600":"#4f46e5","700":"#4338ca","800":"#3730a3","900":"#312e81"}

				// blue
				// primary: {"50":"#eff6ff","100":"#dbeafe","200":"#bfdbfe","300":"#93c5fd","400":"#60a5fa","500":"#3b82f6","600":"#2563eb","700":"#1d4ed8","800":"#1e40af","900":"#1e3a8a"}

				// sky
				// primary: {"50":"#f0f9ff","100":"#e0f2fe","200":"#bae6fd","300":"#7dd3fc","400":"#38bdf8","500":"#0ea5e9","600":"#0284c7","700":"#0369a1","800":"#075985","900":"#0c4a6e"}

				// cyan
				// primary: {"50":"#ecfeff","100":"#cffafe","200":"#a5f3fc","300":"#67e8f9","400":"#22d3ee","500":"#06b6d4","600":"#0891b2","700":"#0e7490","800":"#155e75","900":"#164e63"}

				// teal
				// primary: {"50":"#f0fdfa","100":"#ccfbf1","200":"#99f6e4","300":"#5eead4","400":"#2dd4bf","500":"#14b8a6","600":"#0d9488","700":"#0f766e","800":"#115e59","900":"#134e4a"}

				// emerald
				// primary: {"50":"#ecfdf5","100":"#d1fae5","200":"#a7f3d0","300":"#6ee7b7","400":"#34d399","500":"#10b981","600":"#059669","700":"#047857","800":"#065f46","900":"#064e3b"}

				// green
				// primary: {"50":"#f0fdf4","100":"#dcfce7","200":"#bbf7d0","300":"#86efac","400":"#4ade80","500":"#22c55e","600":"#16a34a","700":"#15803d","800":"#166534","900":"#14532d"}

				// lime
				// primary: {"50":"#f7fee7","100":"#ecfccb","200":"#d9f99d","300":"#bef264","400":"#a3e635","500":"#84cc16","600":"#65a30d","700":"#4d7c0f","800":"#3f6212","900":"#365314"}

				// yellow
				// primary: {"50":"#fefce8","100":"#fef9c3","200":"#fef08a","300":"#fde047","400":"#facc15","500":"#eab308","600":"#ca8a04","700":"#a16207","800":"#854d0e","900":"#713f12"}

				// amber
				// primary: {"50":"#fffbeb","100":"#fef3c7","200":"#fde68a","300":"#fcd34d","400":"#fbbf24","500":"#f59e0b","600":"#d97706","700":"#b45309","800":"#92400e","900":"#78350f"}

				// orange
				// primary: {"50":"#fff7ed","100":"#ffedd5","200":"#fed7aa","300":"#fdba74","400":"#fb923c","500":"#f97316","600":"#ea580c","700":"#c2410c","800":"#9a3412","900":"#7c2d12"}

				// red
				// primary: {"50":"#fef2f2","100":"#fee2e2","200":"#fecaca","300":"#fca5a5","400":"#f87171","500":"#ef4444","600":"#dc2626","700":"#b91c1c","800":"#991b1b","900":"#7f1d1d"}

				// stone
				// primary: {"50":"#fafaf9","100":"#f5f5f4","200":"#e7e5e4","300":"#d6d3d1","400":"#a8a29e","500":"#78716c","600":"#57534e","700":"#44403c","800":"#292524","900":"#1c1917"}

				// neutral
				// primary: {"50":"#fafafa","100":"#f5f5f5","200":"#e5e5e5","300":"#d4d4d4","400":"#a3a3a3","500":"#737373","600":"#525252","700":"#404040","800":"#262626","900":"#171717"}

				// zinc
				// primary: {"50":"#fafafa","100":"#f4f4f5","200":"#e4e4e7","300":"#d4d4d8","400":"#a1a1aa","500":"#71717a","600":"#52525b","700":"#3f3f46","800":"#27272a","900":"#18181b"}

				// gray
				// primary: {"50":"#f9fafb","100":"#f3f4f6","200":"#e5e7eb","300":"#d1d5db","400":"#9ca3af","500":"#6b7280","600":"#4b5563","700":"#374151","800":"#1f2937","900":"#111827"}

				// slate
				// primary: {"50":"#f8fafc","100":"#f1f5f9","200":"#e2e8f0","300":"#cbd5e1","400":"#94a3b8","500":"#64748b","600":"#475569","700":"#334155","800":"#1e293b","900":"#0f172a"}
			}
		}
	}
};

module.exports = config;
```
## api 서버 구성
### 설치 및 실행
pocketbase 설치. zip 파일 압축 해제  
```Text
https://pocketbase.io/
```
pocketbase 실행. 설치 디렉토리 이동 후 프로그램 실행
```Shell
./pocketbase -serve
```
### pocketbase 사용
Browser 실행 후 아래 url(pocketbase admin)로 이동
```Text
http://127.0.0.1:8090/_/
```
root 계정 생성 후 root 계정 로그인 후 collection(DB table) 생성
![](스크린샷_2024-03-30_오후_2.01.20.png)

### api 사용 권한 
Collection을 기본 생성하였을 경우 조회가 되지 않는다. 추가적으로 권한 설정을 해주어야 한다. 아래와 같이 권한 설정을 추가해주어야만 권한없이 조회 가능하다

![](스크린샷_2024-03-30_오후_2.17.08.png)
```Text
@request.auth.id = ''
```
### api 호출 포맷
호출 포맷은 아래와 같다. 
```Text
http://${pocketbaseUrl}:${port}/api/collections/${Collection명}/records
```
결과 값은 아래와 같이 출력된다. 
```JSON
{
    "page": 1,
    "perPage": 30,
    "totalItems": 4,
    "totalPages": 1,
    "items": [
        {
            "collectionId": "x41a0c2yrnoey9l",
            "collectionName": "services",
            "created": "2024-03-30 01:47:37.428Z",
            "desc": "about page",
            "id": "hfij0a4e1nj3osv",
            "name": "About",
            "updated": "2024-03-30 01:47:37.428Z",
            "url": "http://localhost:5173/about",
            "use_yn": true
        },
        {
            "collectionId": "x41a0c2yrnoey9l",
            "collectionName": "services",
            "created": "2024-03-30 01:48:10.998Z",
            "desc": "service page",
            "id": "j9m9bzge7whggo3",
            "name": "Service",
            "updated": "2024-03-30 01:48:26.165Z",
            "url": "http://localhost:5173/service",
            "use_yn": true
        },
        {
            "collectionId": "x41a0c2yrnoey9l",
            "collectionName": "services",
            "created": "2024-03-30 01:49:50.717Z",
            "desc": "pricing page",
            "id": "0z3rivcpg0csbtk",
            "name": "Pricing",
            "updated": "2024-03-30 01:49:50.717Z",
            "url": "http://localhost:5173/pricing",
            "use_yn": true
        },
        {
            "collectionId": "x41a0c2yrnoey9l",
            "collectionName": "services",
            "created": "2024-03-30 01:50:28.236Z",
            "desc": "contract page",
            "id": "e8l3uqrjlxq3lpq",
            "name": "Contact",
            "updated": "2024-03-30 01:50:28.236Z",
            "url": "http://localhost:5173/contact",
            "use_yn": true
        }
    ]
}

```
## flowbite svelte 및 api 연계 사용
svelte에서 로딩 시 api 서버에서 정보를 가지고 올 때에는 아래 내용을 import 해야 한다
```Javascript
import { onMount } from 'svelte';
```
import 후 사용 방법은 아래와 같다. 
```
    let data = {};
	let items = [];

	onMount(async () => {
		try {
			const response = await fetch('http://localhost:8090/api/collections/services/records');
			if (response.ok) {
				data = await response.json();
				items = data.items;
				console.log(items.length);
			} else {
				throw new Error('Failed to fetch data');
			}
		} catch (error) {
			console.error('Error fetching data:', error);
		}
	});
```
화면에서의 사용 예시는 아래와 같다. 
```Javascript
<NavUl {hidden}>
		<NavLi href="/" active={true}>Home</NavLi>

			{#each items as item, idx}
				<NavLi href="{item.url}">{item.name}</NavLi>
			{/each}


		<NavLi href="/about">About1</NavLi>
		<NavLi href="/services">Services1</NavLi>
		<NavLi href="/pricing">Pricing1</NavLi>
		<NavLi href="/contact">Contact1</NavLi>

	</NavUl>
```
## Flowbite Drop down Menu 사용
Drop down Menu를 사용하기 위해서는 아래 내용을 추가해야 한다. 
```Javascript
import { ..., Dropdown, DropdownItem, DropdownDivider } from 'flowbite-svelte';
```
NavUI 코드 추가
```
<NavLi class="cursor-pointer">
			Dropdown<ChevronDownOutline class="w-3 h-3 ms-2 text-primary-800 dark:text-white inline" />
		</NavLi>
		<Dropdown class="w-44 z-20">
			<DropdownItem href="/">Dashboard</DropdownItem>
			<DropdownItem href="/docs/components/navbar">Settings</DropdownItem>
			<DropdownItem href="/">Earnings</DropdownItem>
			<DropdownDivider />
			<DropdownItem href="/">Sign out</DropdownItem>
		</Dropdown>
```
## Svelte layout 활용
```Javascript
<script>
	import '../app.css';
	import { DarkMode } from 'flowbite-svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Dropdown, DropdownItem, DropdownDivider } from 'flowbite-svelte';
	import { ChevronDownOutline } from 'flowbite-svelte-icons';
	import { onMount } from 'svelte';
	let darkmodebtn =
		'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 focus:outline-none focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 rounded-lg text-lg p-2.5 fixed right-4 top-2 z-50';

	let data = {};
	let items = [];

	onMount(async () => {
		try {
			const response = await fetch('http://localhost:8090/api/collections/services/records');
			if (response.ok) {
				data = await response.json();
				items = data.items;
				console.log(items.length);
			} else {
				throw new Error('Failed to fetch data');
			}
		} catch (error) {
			console.error('Error fetching data:', error);
		}
	});
</script>

<Navbar let:hidden let:toggle color="primary">
	<NavBrand href="/">
		<img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-red-800">Flowbite</span>
	</NavBrand>
	<NavHamburger on:click={toggle} />
	<NavUl {hidden}>
		<NavLi href="/" active={true}>Home</NavLi>
		<NavLi class="cursor-pointer">
			Dropdown<ChevronDownOutline class="w-3 h-3 ms-2 text-primary-800 dark:text-white inline" />
		</NavLi>
		<Dropdown class="w-44 z-20">
			<DropdownItem href="/">Dashboard</DropdownItem>
			<DropdownItem href="/docs/components/navbar">Settings</DropdownItem>
			<DropdownItem href="/">Earnings</DropdownItem>
			<DropdownDivider />
			<DropdownItem href="/">Sign out</DropdownItem>
		</Dropdown>

		{#each items as item, idx}
			<NavLi href="{item.url}">{item.name}</NavLi>
		{/each}
	</NavUl>
</Navbar>


<!-- +layout.svelte -->
<header>Hi, I'm a header</header>
<DarkMode btnClass={darkmodebtn} />
<main>
	<slot />
</main>

<footer>Hello, I'm the footer.</footer>

```
