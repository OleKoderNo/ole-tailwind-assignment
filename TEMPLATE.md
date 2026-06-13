The navbar here has all buttons and need to be modified by removing the unwanted once.

    	<header class="bg-slate-900 text-white">
    		<nav class="mx-auto flex max-w-6xl flex-wrap items-center justify-between p-4">
    			<a href="/" class="text-xl font-bold">Cool project name</a>
    			<input id="menu-toggle" type="checkbox" class="peer hidden" />
    			<label
    				for="menu-toggle"
    				class="cursor-pointer rounded border border-white px-4 py-2 md:hidden"
    				aria-label="Toggle menu"
    			>
    				☰
    			</label>
    			<!-- Mobile dropdown -->
    			<div class="hidden w-full flex-col gap-2 pt-4 text-center peer-checked:flex md:hidden">
    				<a href="/feed/" class="rounded bg-slate-700 px-4 py-2">Home</a>
    				<a href="/profile/" class="rounded bg-slate-700 px-4 py-2">Profile</a>
    				<a href="#" class="rounded px-4 py-2 bg-blue-500 hover:bg-blue-700">Log in</a>
    				<a href="#" class="rounded px-4 py-2 text-slate-900 bg-slate-100 hover:bg-slate-300">
    					Register
    				</a>
    				<a href="/index.html" class="rounded bg-blue-500 px-4 py-2">Log out</a>
    			</div>
    			<!-- Desktop menu -->
    			<div class="hidden flex-1 justify-center gap-6 md:flex">
    				<a href="/feed/" class="hover:underline">Home</a>
    				<a href="/profile/" class="hover:underline">Profile</a>
    			</div>
    			<a
    				href="/index.html"
    				class="hidden rounded bg-blue-500 px-4 py-2 hover:bg-blue-700 md:block"
    			>
    				Log out
    			</a>
    		</nav>
    	</header>

This is a aditional class for tailwind to target the dialog element correctly. Normally I would use javascript to make this happen. But this is a nice work around.

dialog:not(:target) {
display: none;
}

dialog:target {
display: block;
position: fixed;
inset: 0;
margin: auto;
z-index: 50;
}
