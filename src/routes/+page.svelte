<script lang="ts">
	import { onMount } from 'svelte';

	let email = '';
	
	const faqs = [
		{ question: "Is Endex its own web application separate from Excel?", answer: "No, Endex lives directly within Excel as a native add-in." },
		{ question: "Can Endex pull in data from outside my excel workbook?", answer: "Yes, Endex can connect to various external data sources." },
		{ question: "Can Endex give me actionable insights, rather than just AI-generated summaries?", answer: "Absolutely. Endex is designed to perform complex analysis and provide actionable financial insights." },
		{ question: "Is Endex limited to a specific set of workflows?", answer: "Endex is flexible and can adapt to a wide range of financial and data analysis workflows." },
		{ question: "How does Endex manage the data in my Excel files? Are my Excel files and queries used for model training?", answer: "Your data privacy is paramount. We do not use your data for model training without explicit permission." },
		{ question: "How can I trust Endex's outputs to be accurate?", answer: "Endex provides citations and audit trails for all its outputs, allowing you to verify every number." },
		{ question: "Am I allowed to download Endex at my firm?", answer: "Please check with your IT department. We offer enterprise deployment options." },
		{ question: "What if Endex builds an analysis I don't like?", answer: "You can easily undo changes or iterate on the prompt to refine the analysis." },
		{ question: "How do I best prompt Endex to complete a task?", answer: "Use clear, natural language instructions as if you were speaking to a junior analyst." },
		{ question: "Can Endex help me build charts and create other visualizations?", answer: "Yes, Endex can generate charts and graphs based on your data." }
	];
</script>

<div class="min-h-screen bg-dark-bg text-white font-sans selection:bg-brand-green selection:text-dark-bg">
	
	<!-- Announcement Banner -->
	<div class="w-full bg-dark-bg py-3 text-center text-[10px] tracking-widest uppercase border-b border-white/5">
		<span class="text-gray-400">Announcing</span> <span class="text-brand-green">$14M Led By OpenAI</span> <span class="text-gray-400">Startup Fund</span>
	</div>

	<!-- Navigation -->
	<nav class="flex items-center justify-between px-6 py-5 max-w-7xl mx-auto">
		<div class="flex items-center gap-8">
			<a href="/" class="text-2xl font-serif tracking-tight font-medium">Endex</a>
			<div class="hidden md:flex gap-6 text-sm text-gray-400">
				<a href="#security" class="hover:text-white transition-colors">Security</a>
				<a href="#careers" class="hover:text-white transition-colors">Careers</a>
			</div>
		</div>
		<a href="#sales" class="text-sm text-white hover:text-gray-300 transition-colors">Enterprise sales</a>
	</nav>

	<!-- Hero Section -->
	<section class="pt-20 pb-32 px-4 text-center max-w-5xl mx-auto relative z-10">
		<h1 class="text-5xl md:text-7xl font-serif mb-6 tracking-tight">AI Built For Excel</h1>
		<p class="text-gray-400 text-lg md:text-xl mb-10 max-w-2xl mx-auto font-light">
			An Excel-native AI Agent that accelerates financial modeling and data analysis
		</p>

		<div class="flex flex-col sm:flex-row items-center justify-center gap-2 mb-4 max-w-md mx-auto">
			<input 
				type="email" 
				placeholder="Email" 
				bind:value={email}
				class="w-full sm:w-64 bg-[#0A1F1E] border border-white/10 rounded px-4 py-2.5 text-sm text-white placeholder-gray-500 focus:outline-none focus:border-brand-green/50 transition-colors"
			/>
			<button class="w-full sm:w-auto bg-white text-dark-bg px-6 py-2.5 rounded text-sm font-medium hover:bg-gray-100 transition-colors">
				Request Access
			</button>
		</div>
		
		<a href="#sales" class="text-xs text-gray-500 hover:text-gray-400 underline decoration-gray-700 underline-offset-4">contact sales for accelerated team access</a>
	</section>

	<!-- Hero Image/Video Placeholder -->
	<div class="relative max-w-6xl mx-auto px-4 -mt-16 mb-32">
		<div class="rounded-lg overflow-hidden border border-white/10 shadow-2xl bg-[#1a1a1a] aspect-[16/9] relative group cursor-pointer">
			<!-- Fake Spreadsheet UI -->
			<div class="absolute inset-0 bg-white text-black text-xs font-mono overflow-hidden opacity-90">
				<div class="w-full h-8 bg-[#107C41] flex items-center px-2">
					<div class="w-4 h-4 bg-white/20 rounded-full mr-2"></div>
					<span class="text-white font-sans font-semibold">Book1 - Excel</span>
				</div>
				<div class="w-full h-8 bg-[#F3F2F1] border-b border-[#E1DFDD] flex items-center px-4 gap-4 text-gray-600">
					<span>File</span> <span>Home</span> <span>Insert</span> <span>Draw</span> <span class="text-[#107C41] border-b-2 border-[#107C41]">Endex</span>
				</div>
				<div class="p-4 grid grid-cols-12 gap-0">
					<!-- Just a visual representation of a grid -->
					{#each Array(20) as _, i}
						<div class="border border-gray-100 p-2 text-right text-gray-400">{i+1}</div>
						<div class="col-span-11 border border-gray-100 p-2"></div>
					{/each}
				</div>
				<!-- Overlay Image to look like the screenshot -->
				<img src="https://placehold.co/1200x675/white/black?text=Spreadsheet+UI+Demo" alt="Endex Demo" class="absolute inset-0 w-full h-full object-cover opacity-50" />
			</div>

			<!-- Play Button -->
			<div class="absolute inset-0 flex items-center justify-center">
				<div class="w-20 h-20 bg-black rounded-full flex items-center justify-center pl-1 transition-transform group-hover:scale-105">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg">
						<path d="M5 3L19 12L5 21V3Z" />
					</svg>
				</div>
			</div>
		</div>
		<!-- Gradient Glows -->
		<div class="absolute -top-20 -left-20 w-96 h-96 bg-brand-green/10 rounded-full blur-[100px] -z-10"></div>
		<div class="absolute -bottom-20 -right-20 w-96 h-96 bg-blue-500/10 rounded-full blur-[100px] -z-10"></div>
	</div>

	<!-- Auditable Section -->
	<section class="bg-white text-dark-bg py-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-16 items-center">
			<div>
				<h2 class="text-4xl md:text-5xl font-serif mb-6 leading-tight">Auditable from Start to Finish</h2>
				<p class="text-gray-600 text-lg leading-relaxed">
					Endex provides integrated citations, augmenting outputs with attribution to underlying sources.
				</p>
			</div>
			<div class="relative">
				<!-- Spreadsheet graphic -->
				<div class="bg-white rounded-lg shadow-xl border border-gray-200 overflow-hidden transform rotate-1">
					<div class="grid grid-cols-5 text-xs text-gray-500 border-b border-gray-200 bg-gray-50">
						<div class="p-2 text-center border-r">A</div>
						<div class="p-2 text-center border-r">B</div>
						<div class="p-2 text-center border-r">C</div>
						<div class="p-2 text-center border-r">D</div>
						<div class="p-2 text-center">E</div>
					</div>
					<div class="p-4 space-y-2 font-mono text-xs">
						<div class="flex justify-between border-b border-gray-100 pb-1">
							<span>Revenue</span> <span>$1,200</span>
						</div>
						<div class="flex justify-between border-b border-gray-100 pb-1">
							<span>Cost</span> <span>$800</span>
						</div>
						<div class="flex justify-between font-bold bg-green-50 p-1 rounded relative group cursor-help">
							<span>Profit</span> <span>$400</span>
							<!-- Tooltip/Citation -->
							<div class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2 w-48 bg-white shadow-lg rounded p-3 border border-gray-200 text-[10px] font-sans text-gray-600 hidden group-hover:block z-10">
								<div class="font-semibold text-black mb-1">Source: Q3 Report</div>
								<div class="text-gray-400">Page 42, Table 3.2</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Grid Section -->
	<section class="bg-white text-dark-bg pb-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-8">
			<!-- Card 1 -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<h3 class="text-2xl font-serif mb-4">LLMs engineered for finance</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					Custom-built models designed to understand the intricacies of financial documents - from detailed accounting methods, reconciling disagreeing sources, and complex financial charts.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-8 h-48 flex items-center justify-center relative overflow-hidden">
					<!-- Checkerboard pattern -->
					<div class="grid grid-cols-4 gap-0 border border-gray-100">
						{#each Array(16) as _, i}
							<div class="w-8 h-8 border border-gray-50 flex items-center justify-center text-[8px] text-gray-300">
								{#if i === 9}
									<div class="w-full h-full bg-black flex items-center justify-center">
										<div class="w-4 h-4 bg-white/20 grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div>
									</div>
								{:else}
									<!-- Empty -->
								{/if}
							</div>
						{/each}
					</div>
					<!-- Floating labels/tooltips simulation -->
					<div class="absolute top-4 left-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-gray-100 text-gray-400">Same store sales (YoY)</div>
					<div class="absolute bottom-4 right-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-gray-100 text-gray-400">Firm value</div>
				</div>
			</div>
			<!-- Card 2 -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<h3 class="text-2xl font-serif mb-4">Reason over all of your data</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					Endex unifies your internal files, external data, and trusted sources into a single searchable plane - giving you and your AI agents a complete picture at your fingertips.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-6 h-48 flex items-center justify-center relative">
					<!-- Chart graphic -->
					<div class="w-full h-full flex items-end justify-between gap-4 px-4 pb-2 border-l border-b border-gray-100">
						<div class="w-full bg-gray-100 h-[30%] rounded-t-sm relative group">
							<div class="absolute -top-6 left-1/2 -translate-x-1/2 text-[8px] text-gray-400 opacity-0 group-hover:opacity-100 transition-opacity">$4.5B</div>
						</div>
						<div class="w-full bg-gray-200 h-[60%] rounded-t-sm relative group">
							<div class="absolute -top-6 left-1/2 -translate-x-1/2 text-[8px] text-gray-400 opacity-0 group-hover:opacity-100 transition-opacity">$8.2B</div>
						</div>
						<div class="w-full bg-black h-[45%] rounded-t-sm relative group">
							<div class="absolute -top-6 left-1/2 -translate-x-1/2 text-[8px] text-gray-400 opacity-0 group-hover:opacity-100 transition-opacity">$6.1B</div>
						</div>
						<div class="w-full bg-gray-300 h-[80%] rounded-t-sm relative group">
							<div class="absolute -top-6 left-1/2 -translate-x-1/2 text-[8px] text-gray-400 opacity-0 group-hover:opacity-100 transition-opacity">$10.5B</div>
						</div>
					</div>
					<!-- Floating icon -->
					<div class="absolute right-4 top-1/2 -translate-y-1/2 w-10 h-10 bg-white shadow-lg rounded border border-gray-100 flex items-center justify-center">
						<div class="w-5 h-5 bg-black grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Testimonial -->
	<section class="bg-dark-bg text-white py-32 relative overflow-hidden">
		<div class="max-w-4xl mx-auto px-6 text-center relative z-10">
			<div class="text-brand-green text-6xl font-serif absolute -top-10 left-0 opacity-50">“</div>
			<blockquote class="text-3xl md:text-4xl font-serif leading-tight mb-12 relative">
				<span class="text-brand-green absolute -left-4 -top-4">“</span>
				I took my hands off the keyboard and it finished my model for me. This is the creepiest thing I've ever seen
				<span class="text-brand-green absolute -right-4 bottom-4">”</span>
			</blockquote>
			<div class="flex items-center justify-between border-t border-white/10 pt-8">
				<div class="text-sm font-mono tracking-wide uppercase text-gray-400">VP at Growth Equity Firm</div>
				<div class="flex gap-2">
					<button class="w-8 h-8 border border-white/20 flex items-center justify-center hover:bg-white/10 transition-colors">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 18l-6-6 6-6"/></svg>
					</button>
					<button class="w-8 h-8 border border-white/20 flex items-center justify-center hover:bg-white/10 transition-colors">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 18l6-6-6-6"/></svg>
					</button>
				</div>
			</div>
		</div>
	</section>

	<!-- Features Grid -->
	<section class="bg-white text-dark-bg py-24">
		<div class="text-center mb-16">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+FEATURES</div>
			<h2 class="text-5xl md:text-6xl font-serif mb-4">
				Built for <br />
				Power <span class="inline-block w-8 h-8 bg-[#107C41] align-middle rounded mx-1 relative top-[-4px]"><svg class="w-5 h-5 text-white absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2" viewBox="0 0 24 24" fill="currentColor"><path d="M14 2H6c-1.1 0-1.99.9-1.99 2L4 20c0 1.1.89 2 1.99 2H18c1.1 0 2-.9 2-2V8l-6-6zm2 16H8v-2h8v2zm0-4H8v-2h8v2zm-3-5V3.5L18.5 9H13z"/></svg></span> Teams
			</h2>
			<p class="text-gray-600 mb-6">Essential capabilities built directly in Excel</p>
			<div class="flex items-center justify-center gap-2 text-gray-500 text-sm font-semibold">
				<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M11.5,0 L12.5,0 L12.5,11 L23.5,11 L23.5,12 L12.5,12 L12.5,23 L11.5,23 L11.5,12 L0.5,12 L0.5,11 L11.5,11 L11.5,0 Z" transform="rotate(45 12 12)"/></svg>
				Microsoft Partner
			</div>
		</div>

		<!-- Feature Nav (Visual only based on screenshot) -->
		<div class="flex flex-wrap justify-center gap-6 text-sm text-gray-400 mb-16 border-b border-gray-100 pb-4 max-w-6xl mx-auto px-6">
			<span>Trace References</span>
			<span>Sheet Navigation</span>
			<span>Data Sources</span>
			<span>Formatting</span>
			<span class="text-black font-medium border-b-2 border-black pb-4 -mb-4.5">Deep Research</span>
			<span>Memories</span>
			<span>LLM Integrations</span>
			<span>Undo</span>
			<span>Conversion</span>
		</div>

		<div class="max-w-6xl mx-auto px-6 space-y-8">
			<!-- Row 1: Trace References -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Trace References</h3>
					<p class="text-gray-600 text-sm leading-relaxed">
						Navigate complex workbooks end-to-end with AI-labeled tracing of cell references
					</p>
				</div>
				<div class="bg-white shadow-lg shadow-gray-200/50 border border-gray-200 rounded-lg p-6 transform rotate-1 transition-transform hover:rotate-0">
					<div class="flex items-center gap-4 mb-4 text-[10px] text-gray-400 border-b border-gray-100 pb-2">
						<div class="w-4 text-center">I</div>
						<div class="w-16 text-center">J</div>
						<div class="w-16 text-center">K</div>
						<div class="w-16 text-center">L</div>
					</div>
					<!-- Fake table -->
					<div class="grid grid-cols-4 gap-y-3 text-xs font-mono">
						<div class="text-gray-400 text-[10px] self-center">21</div> <div class="col-span-1 text-gray-500">PF Revenue</div> <div class="col-span-2 text-right">$110,000</div>
						<div class="text-gray-400 text-[10px] self-center">22</div> <div class="col-span-1 text-gray-500">PF COGS</div> <div class="col-span-2 text-right">$31,252</div>
						<div class="col-span-4 h-px bg-gray-100 my-1"></div>
						<div class="text-gray-400 text-[10px] self-center">23</div> <div class="col-span-1 font-bold text-black">Base Gross Profit</div> <div class="col-span-2 text-right font-bold text-black bg-green-50 px-1 rounded border border-green-100 relative">
							$72,000
							<div class="absolute top-0 right-0 w-1.5 h-1.5 bg-green-500 rounded-full -mt-0.5 -mr-0.5"></div>
						</div>
						<div class="text-gray-400 text-[10px] self-center">24</div> <div class="col-span-1 text-gray-500">FX Gains (add-back)</div> <div class="col-span-2 text-right">$1,200</div>
						<div class="text-gray-400 text-[10px] self-center">25</div> <div class="col-span-1 text-gray-500">Inventory Fair Value</div> <div class="col-span-2 text-right">$2,100</div>
					</div>
				</div>
			</div>

			<!-- Row 2: Navigate & Firm Templates -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-[#E6F4F1] rounded-2xl p-8 md:p-12 relative overflow-hidden">
					<div class="relative z-10">
						<div class="flex items-center gap-2 mb-4">
							<div class="w-6 h-6 bg-black rounded flex items-center justify-center text-white text-xs">E</div>
							<span class="text-xs font-semibold uppercase tracking-wider">Endex • Just now</span>
						</div>
						<p class="text-sm text-gray-800 mb-8 max-w-xs">
							Analyzing your <span class="bg-green-200 px-1 rounded text-green-800 font-mono text-xs">Balance Sheet</span>, total assets in <span class="bg-green-200 px-1 rounded text-green-800 font-mono text-xs">Balance Sheet!B45:G45</span> have grown 6% year-over-year.
						</p>
						<h3 class="text-2xl font-serif mb-2">Navigate Your Spreadsheet</h3>
						<p class="text-gray-600 text-xs">Jump to cells and ranges directly from Endex in-line citations</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
					<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 mb-8 max-w-xs mx-auto">
						<div class="text-xs font-semibold mb-3 border-b border-gray-100 pb-2">Saved Templates</div>
						<div class="space-y-2">
							<div class="flex items-center gap-2 text-xs text-gray-500">
								<div class="w-3 h-3 border border-gray-300"></div> Quarter-End Close Pack
							</div>
							<div class="flex items-center justify-between gap-2 text-xs bg-gray-50 p-2 rounded border border-gray-200">
								<div class="flex items-center gap-2 font-medium">
									<div class="w-3 h-3 border border-gray-400 bg-gray-200"></div> Investor Update
								</div>
								<span class="bg-black text-white px-1.5 py-0.5 rounded text-[10px]">Open</span>
							</div>
						</div>
					</div>
					<h3 class="text-2xl font-serif mb-2">Firm Templates</h3>
					<p class="text-gray-600 text-xs">Create repeatable templates that autocomplete with new input data</p>
				</div>
			</div>

			<!-- Row 3: Formatting Shortcuts -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Formatting Shortcuts</h3>
					<p class="text-gray-600 text-sm leading-relaxed mb-6">
						Apply consistent formatting instantly with keyboard shortcuts customizable by you
					</p>
					<div class="space-y-2 text-xs font-mono text-gray-500">
						<div class="flex justify-between border-b border-gray-200 pb-1"><span>Number Formatting</span> <span>Alt Shift F</span></div>
						<div class="flex justify-between border-b border-gray-200 pb-1"><span>Color & Styles</span> <span>Alt Shift K</span></div>
					</div>
				</div>
				<div class="relative h-48">
					<!-- Keyboard Graphic Placeholder -->
					<div class="absolute inset-0 flex items-center justify-center opacity-20">
						<div class="grid grid-cols-10 gap-1 w-full">
							{#each Array(30) as _}
								<div class="h-8 border border-black rounded"></div>
							{/each}
						</div>
					</div>
				</div>
			</div>

			<!-- Row 4: 3 Cards -->
			<div class="grid md:grid-cols-3 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-4 mb-6 shadow-sm">
						<div class="flex items-center gap-2 mb-2">
							<div class="w-4 h-4 rounded-full bg-black"></div>
							<span class="text-xs font-semibold">Research complete</span>
						</div>
						<div class="flex justify-between items-center text-[10px] text-gray-500">
							<span>28 sources</span>
							<span class="underline">View details</span>
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Deep Research Integration</h3>
					<p class="text-gray-500 text-xs">Native access of OpenAI Deep Research with contextual understanding</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-3 mb-6 shadow-sm max-w-[200px]">
						<div class="text-[10px] text-gray-400 mb-1">Decimal places: 2</div>
						<div class="flex items-center gap-2 text-xs font-medium mb-1">
							<div class="w-4 h-4 bg-black text-white flex items-center justify-center rounded text-[8px]">M</div>
							Saved Preferences
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Memories</h3>
					<p class="text-gray-500 text-xs">Endex will remember your style preferences and favorite workflows</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="flex gap-2 mb-6 justify-center">
						<div class="w-8 h-8 rounded-full bg-gray-200"></div>
						<div class="w-8 h-8 rounded bg-black flex items-center justify-center"><div class="w-4 h-4 bg-white/20 grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div></div>
						<div class="w-8 h-8 rounded-full bg-gray-200"></div>
					</div>
					<h3 class="text-xl font-serif mb-2">Powerful Models</h3>
					<p class="text-gray-500 text-xs">Deeply integrated with all major model providers with zero data retention</p>
				</div>
			</div>

			<!-- Row 5: 2 Cards -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8 flex flex-col justify-between">
					<div class="bg-white border border-gray-200 rounded-full px-4 py-2 shadow-sm self-start mb-8 flex items-center gap-4 text-xs">
						<span class="text-gray-400">Restored Checkpoint 14:21:32</span>
						<span class="font-bold">Undo</span>
					</div>
					<div>
						<h3 class="text-xl font-serif mb-2">Undo Changes</h3>
						<p class="text-gray-500 text-xs">Revert unwanted changes with one-click</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-black text-white rounded px-3 py-1.5 text-xs inline-flex items-center gap-2 mb-4">
						<svg class="w-3 h-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15" /></svg>
						Conversion completed
					</div>
					<div class="flex gap-4 mb-8">
						<div class="w-1/3 bg-white border border-gray-200 h-20 rounded p-2">
							<div class="h-2 w-12 bg-gray-200 mb-2"></div>
							<div class="h-1 w-full bg-gray-100 mb-1"></div>
							<div class="h-1 w-full bg-gray-100 mb-1"></div>
						</div>
						<div class="w-2/3 bg-white border border-gray-200 h-20 rounded p-2 grid grid-cols-3 gap-1">
							<div class="bg-gray-50 h-full"></div>
							<div class="bg-gray-50 h-full"></div>
							<div class="bg-gray-50 h-full"></div>
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">PDF to Table Conversion</h3>
					<p class="text-gray-500 text-xs">Eliminate manual data entry from financial statements, pitch decks, and research reports</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Data Sources -->
	<section class="bg-dark-bg text-white py-24 border-t border-white/5">
		<div class="max-w-4xl mx-auto px-6 text-center">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+DATA SOURCES</div>
			<h2 class="text-3xl md:text-5xl font-serif mb-6">Endex integrates natively with internal data and external sources</h2>
			<p class="text-gray-400 mb-12">Build and contextualize models with verifiable sources</p>

			<div class="bg-[#0A1F1E] border border-white/10 rounded-xl overflow-hidden max-w-md mx-auto relative">
				<div class="p-4 flex items-center gap-4 border-b border-white/5 bg-[#0F2928] relative z-10">
					<div class="w-8 h-8 bg-white rounded flex items-center justify-center shadow-lg shadow-brand-green/20">
						<div class="w-4 h-4 bg-black grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div>
					</div>
					<div class="text-left">
						<div class="text-sm font-medium text-white">Endex for Excel</div>
						<div class="text-[10px] text-brand-green flex items-center gap-1">
							<span class="w-1 h-1 bg-brand-green rounded-full animate-pulse"></span>
							Accessing data sources...
						</div>
					</div>
				</div>
				
				<!-- Connecting line visual -->
				<div class="absolute left-8 top-12 bottom-0 w-px bg-gradient-to-b from-white/20 to-transparent z-0"></div>

				<div class="divide-y divide-white/5 text-sm text-gray-400 text-left relative z-10">
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>FactSet</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-green">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>SEC Filings</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-green">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Earnings calls</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-green">Connected</span>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Security -->
	<section id="security" class="bg-white text-dark-bg py-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-16">
			<div>
				<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+SECURITY</div>
				<h2 class="text-4xl md:text-5xl font-serif mb-6">Enterprise-grade security</h2>
				<p class="text-gray-600 mb-8 leading-relaxed">
					Your data is encrypted both in transit and at rest, utilizing the most robust encryption standards: AES-256 for storage and TLS 1.2/1.3 for secure communication
				</p>
				<a href="#" class="inline-flex items-center gap-2 font-medium hover:underline">
					<div class="w-5 h-5 bg-black text-white flex items-center justify-center rounded-sm text-xs">→</div>
					Learn more
				</a>
			</div>
			<div class="grid grid-cols-2 gap-px bg-gray-200 border border-gray-200">
				<!-- SOC 2 -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border-2 border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute inset-1 border border-black rounded-full"></div>
						<div class="text-[8px] uppercase tracking-widest font-semibold mb-1">AICPA</div>
						<div class="text-lg font-bold leading-none">SOC</div>
						<div class="text-[10px] font-bold">2</div>
					</div>
				</div>
				<!-- ISO -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border-2 border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute inset-1 border border-dashed border-black rounded-full"></div>
						<div class="text-xl font-bold">ISO</div>
						<div class="text-[10px] font-bold bg-black text-white px-1 rounded-sm mt-1">27001</div>
					</div>
				</div>
				<!-- CCPA -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border border-black flex flex-col items-center justify-center relative p-2">
						<div class="text-lg font-serif">CCPA</div>
						<div class="text-[8px] uppercase tracking-widest mt-1">Ready</div>
					</div>
				</div>
				<!-- GDPR -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border border-dashed border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute top-2 text-[10px]">* * *</div>
						<div class="text-lg font-bold">GDPR</div>
						<div class="absolute bottom-2 text-[10px]">* * *</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- FAQs -->
	<section class="bg-white text-dark-bg pb-32">
		<div class="max-w-3xl mx-auto px-6">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+FAQS</div>
			<h2 class="text-4xl md:text-5xl font-serif mb-12">FAQs</h2>

			<div class="border-t border-gray-200">
				{#each faqs as faq}
					<details class="group border-b border-gray-200">
						<summary class="flex justify-between items-center py-6 cursor-pointer list-none">
							<span class="font-medium text-lg pr-8">{faq.question}</span>
							<span class="transition group-open:rotate-45">
								<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M12 5v14M5 12h14"/></svg>
							</span>
						</summary>
						<div class="text-gray-600 pb-6 leading-relaxed">
							{faq.answer}
						</div>
					</details>
				{/each}
			</div>
		</div>
	</section>

	<!-- CTA Footer -->
	<section class="bg-dark-bg text-white py-32 relative overflow-hidden">
		<!-- Grid Background Effect -->
		<div class="absolute inset-0 opacity-20 pointer-events-none" 
			 style="background-image: linear-gradient(rgba(255,255,255,0.05) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.05) 1px, transparent 1px); background-size: 50px 50px;">
		</div>
		<div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-brand-green/20 to-transparent pointer-events-none"></div>

		<div class="max-w-4xl mx-auto px-6 relative z-10">
			<div class="text-[10px] uppercase tracking-widest text-brand-green mb-4">+PUT ENDEX TO WORK</div>
			<h2 class="text-5xl md:text-7xl font-serif mb-12 leading-tight">
				Hire your firm's first AI financial analyst
			</h2>
			<div class="flex flex-wrap gap-4">
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Enterprise sales
				</button>
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Join Waitlist
				</button>
			</div>
		</div>
	</section>

	<!-- Footer -->
	<footer class="bg-[#030e0e] text-gray-400 py-12 border-t border-white/5 relative overflow-hidden">
		<div class="max-w-7xl mx-auto px-6 relative z-10">
			<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-24 text-sm">
				<div>
					<h4 class="text-white font-semibold mb-4">Product</h4>
				</div>
				<div></div>
				<div></div>
				<div class="text-right">
					<h4 class="text-white font-semibold mb-4">Security</h4>
				</div>
				<div>
					<h4 class="text-white font-semibold mb-4">Legal</h4>
				</div>
				<div class="col-span-3 text-right">
					<div class="space-x-4">
						<a href="#" class="hover:text-white">Privacy</a>
						<span>/</span>
						<a href="#" class="hover:text-white">Terms</a>
						<span>/</span>
						<a href="#" class="hover:text-white">End User License Agreement</a>
					</div>
				</div>
			</div>

			<div class="flex justify-between items-end border-t border-white/5 pt-8">
				<div class="flex items-center gap-4">
					<span class="text-white font-serif text-xl">Endex</span>
					<span class="text-xs text-gray-600">Endex 2025. All Rights Reserved</span>
				</div>
				<div class="flex items-center gap-4 text-xs">
					<a href="#" class="hover:text-white">LinkedIn</a>
					<span>/</span>
					<a href="#" class="hover:text-white">X</a>
				</div>
			</div>
		</div>

		<!-- Big Watermark -->
		<div class="absolute bottom-0 left-0 right-0 flex justify-center pointer-events-none overflow-hidden">
			<div class="text-[20vw] font-serif text-white/5 leading-none -mb-10 select-none">
				Endex
			</div>
		</div>
	</footer>
</div>

<style>
	/* Custom scrollbar for details/summary if needed, but default is fine */
	details > summary {
		list-style: none;
	}
	details > summary::-webkit-details-marker {
		display: none;
	}
</style>

