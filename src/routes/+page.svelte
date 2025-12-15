<script lang="ts">
	import { onMount } from 'svelte';

	let email = '';
	
	const faqs = [
		{ question: "How does Cleo Health integrate with our existing EHR system?", answer: "Cleo Health seamlessly integrates with major EHR platforms including Epic, Cerner, and Athena through secure API connections, ensuring smooth data flow without disrupting your current workflows." },
		{ question: "Is patient data secure and HIPAA compliant?", answer: "Absolutely. Cleo Health is fully HIPAA compliant with enterprise-grade encryption (AES-256 at rest, TLS 1.3 in transit). We never use patient data for model training and maintain strict data privacy protocols." },
		{ question: "How accurate are the AI-generated clinical notes?", answer: "Cleo's AI is specifically trained on clinical documentation and provides audit trails for all outputs. Our ambient AI captures real-time workflows with high accuracy, and clinicians maintain full control to review and edit all documentation." },
		{ question: "What specialties does Cleo Health support?", answer: "Cleo Health is designed for acute care settings, with particular strength in emergency departments and inpatient care. Our platform adapts to various clinical workflows across different specialties." },
		{ question: "How long does implementation typically take?", answer: "Implementation timelines vary by organization size, but most hospitals can begin pilot programs within 2-4 weeks. Our team provides comprehensive onboarding and training support throughout the process." },
		{ question: "Can Cleo Health help with charge capture and billing?", answer: "Yes, Cleo's platform includes comprehensive charge capture functionality that ensures accurate documentation of billable services, reducing revenue leakage and improving documentation integrity." },
		{ question: "How does Cleo reduce clinician burnout?", answer: "By automating documentation and administrative tasks, Cleo gives clinicians back valuable time to focus on patient care. Our ambient AI captures workflows in real-time, eliminating hours of after-shift charting." },
		{ question: "What kind of ROI can we expect?", answer: "Healthcare organizations typically see ROI through improved provider satisfaction, enhanced patient experience scores, better charge capture, and reduced documentation time. Specific metrics vary by organization size and implementation scope." },
		{ question: "Does Cleo support patient follow-up after discharge?", answer: "Yes, Cleo includes AI-powered patient follow-up call capabilities to ensure continuity of care and improve patient outcomes after discharge." },
		{ question: "How does Cleo handle clinical documentation integrity (CDI)?", answer: "Cleo's platform includes built-in CDI support that helps ensure documentation meets quality standards and accurately reflects the complexity of care provided, supporting appropriate reimbursement." }
	];
</script>

<div class="min-h-screen bg-dark-bg text-white font-sans selection:bg-brand-primary selection:text-dark-bg">
	
	<!-- Announcement Banner -->
	<div class="w-full bg-dark-bg py-3 text-center text-[10px] tracking-widest uppercase border-b border-white/5">
		<span class="text-gray-400">Transforming</span> <span class="text-brand-primary">Acute Care Documentation</span> <span class="text-gray-400">With AI</span>
	</div>

	<!-- Navigation -->
	<nav class="flex items-center justify-between px-6 py-5 max-w-7xl mx-auto">
		<div class="flex items-center gap-8">
			<a href="/" class="flex items-center gap-2">
				<svg class="w-8 h-8 text-brand-primary" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
					<path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
				</svg>
				<span class="text-2xl font-serif tracking-tight font-medium">Cleo Health</span>
			</a>
			<div class="hidden md:flex gap-6 text-sm text-gray-400">
				<a href="#security" class="hover:text-white transition-colors">Security</a>
				<a href="#careers" class="hover:text-white transition-colors">Careers</a>
			</div>
		</div>
		<a href="#contact" class="text-sm text-white hover:text-gray-300 transition-colors">Contact Sales</a>
	</nav>

	<!-- Hero Section -->
	<section class="pt-20 pb-32 px-4 text-center max-w-5xl mx-auto relative z-10">
		<h1 class="text-5xl md:text-7xl font-serif mb-6 tracking-tight">AI-Native Acute Care Documentation</h1>
		<p class="text-gray-400 text-lg md:text-xl mb-10 max-w-2xl mx-auto font-light">
			Transform chaotic workflows into ambient AI notes. Complete inpatient suite from entry to follow-up.
		</p>

		<div class="flex flex-col sm:flex-row items-center justify-center gap-2 mb-4 max-w-md mx-auto">
			<input 
				type="email" 
				placeholder="Work Email" 
				bind:value={email}
				class="w-full sm:w-64 bg-[#0F1F1F] border border-white/10 rounded px-4 py-2.5 text-sm text-white placeholder-gray-500 focus:outline-none focus:border-brand-primary/50 transition-colors"
			/>
			<button class="w-full sm:w-auto bg-white text-dark-bg px-6 py-2.5 rounded text-sm font-medium hover:bg-gray-100 transition-colors">
				Request Demo
			</button>
		</div>
		
		<a href="#contact" class="text-xs text-gray-500 hover:text-gray-400 underline decoration-gray-700 underline-offset-4">contact sales for hospital-wide deployment</a>
	</section>

	<!-- Hero Image/Video Placeholder -->
	<div class="relative max-w-6xl mx-auto px-4 -mt-16 mb-32">
		<div class="rounded-lg overflow-hidden border border-white/10 shadow-2xl bg-[#1a1a1a] aspect-[16/9] relative group cursor-pointer">
			<!-- Clinical Dashboard UI -->
			<div class="absolute inset-0 bg-gradient-to-br from-gray-900 to-gray-950 text-white text-xs overflow-hidden">
				<div class="w-full h-12 bg-gray-900/90 border-b border-white/10 flex items-center px-4 backdrop-blur">
					<svg class="w-6 h-6 text-brand-primary mr-3" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
						<path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
					</svg>
					<span class="text-white font-sans font-semibold">Cleo Health - Emergency Department</span>
					<div class="ml-auto flex items-center gap-2">
						<span class="text-xs text-brand-primary flex items-center gap-1">
							<span class="w-1.5 h-1.5 bg-brand-primary rounded-full animate-pulse"></span>
							Live Recording
						</span>
					</div>
				</div>
				<div class="p-6 space-y-4">
					<div class="bg-white/5 rounded-lg p-4 border border-white/10">
						<div class="flex items-center justify-between mb-3">
							<span class="text-gray-400 text-xs">Patient: John Smith • MRN: 12345678</span>
							<span class="text-brand-primary text-xs">Ambient AI Active</span>
						</div>
						<div class="space-y-2 text-sm">
							<p class="text-gray-300"><span class="text-brand-primary">Chief Complaint:</span> Chest pain, onset 2 hours ago</p>
							<p class="text-gray-300"><span class="text-brand-primary">HPI:</span> 58-year-old male presents with substernal chest pressure...</p>
							<p class="text-gray-400 text-xs mt-3">AI transcribing in real-time • Auto-syncing to Epic</p>
						</div>
					</div>
					<div class="grid grid-cols-3 gap-3">
						<div class="bg-white/5 rounded p-3 border border-white/10">
							<div class="text-xs text-gray-400 mb-1">Charge Capture</div>
							<div class="text-lg font-bold text-white">$2,847</div>
						</div>
						<div class="bg-white/5 rounded p-3 border border-white/10">
							<div class="text-xs text-gray-400 mb-1">Census</div>
							<div class="text-lg font-bold text-white">42/48</div>
						</div>
						<div class="bg-white/5 rounded p-3 border border-white/10">
							<div class="text-xs text-gray-400 mb-1">Pending CDI</div>
							<div class="text-lg font-bold text-white">7</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Play Button -->
			<div class="absolute inset-0 flex items-center justify-center">
				<div class="w-20 h-20 bg-brand-primary rounded-full flex items-center justify-center pl-1 transition-transform group-hover:scale-105 shadow-2xl shadow-brand-primary/50">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg">
						<path d="M5 3L19 12L5 21V3Z" />
					</svg>
				</div>
			</div>
		</div>
		<!-- Gradient Glows -->
		<div class="absolute -top-20 -left-20 w-96 h-96 bg-brand-primary/10 rounded-full blur-[100px] -z-10"></div>
		<div class="absolute -bottom-20 -right-20 w-96 h-96 bg-brand-primary/5 rounded-full blur-[100px] -z-10"></div>
	</div>

	<!-- Documentation Integrity Section -->
	<section class="bg-white text-dark-bg py-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-16 items-center">
			<div>
				<h2 class="text-4xl md:text-5xl font-serif mb-6 leading-tight">Documentation Integrity You Can Trust</h2>
				<p class="text-gray-600 text-lg leading-relaxed">
					Cleo provides complete audit trails for all AI-generated notes, with real-time verification and clinician oversight at every step.
				</p>
			</div>
			<div class="relative">
				<!-- Clinical Note graphic -->
				<div class="bg-white rounded-lg shadow-xl border border-gray-200 overflow-hidden transform rotate-1">
					<div class="bg-gradient-to-r from-teal-50 to-cyan-50 border-b border-gray-200 p-3">
						<div class="text-xs font-semibold text-gray-700">Clinical Documentation</div>
						<div class="text-[10px] text-gray-500 mt-0.5">Generated by Cleo AI • Verified</div>
					</div>
					<div class="p-4 space-y-3 text-xs">
						<div class="border-l-2 border-gray-200 pl-3">
							<div class="font-semibold text-gray-700 mb-1">Chief Complaint</div>
							<div class="text-gray-600">Chest pain, substernal, 2 hours duration</div>
						</div>
						<div class="border-l-2 border-gray-200 pl-3">
							<div class="font-semibold text-gray-700 mb-1">Assessment</div>
							<div class="text-gray-600">Acute coronary syndrome, rule out MI</div>
						</div>
						<div class="border-l-2 border-teal-400 pl-3 bg-teal-50 p-2 rounded relative group cursor-help">
							<div class="font-semibold text-gray-700 mb-1 flex items-center gap-2">
								<span>Diagnosis Code</span>
								<svg class="w-3 h-3 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
									<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
								</svg>
							</div>
							<div class="text-gray-700 font-mono">I20.0 - Unstable angina</div>
							<!-- Tooltip/Citation -->
							<div class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2 w-56 bg-white shadow-lg rounded p-3 border border-gray-200 text-[10px] font-sans text-gray-600 hidden group-hover:block z-10">
								<div class="font-semibold text-black mb-1">Source: Patient Interview</div>
								<div class="text-gray-400">Timestamp: 14:23:15</div>
								<div class="text-gray-400 mt-1">Verified by: Dr. Johnson</div>
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
				<h3 class="text-2xl font-serif mb-4">AI trained for clinical workflows</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					Purpose-built models designed to understand acute care complexity - from chaotic ED workflows to nuanced clinical documentation standards and real-time patient interactions.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-8 h-48 flex items-center justify-center relative overflow-hidden">
					<!-- Medical icons pattern -->
					<div class="grid grid-cols-4 gap-3">
						{#each Array(16) as _, i}
							<div class="w-8 h-8 border border-gray-100 rounded flex items-center justify-center text-gray-300">
								{#if i === 5}
									<svg class="w-5 h-5 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
										<path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6z"/>
									</svg>
								{:else if i === 10}
									<svg class="w-5 h-5 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
										<path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1z" clip-rule="evenodd"/>
									</svg>
								{/if}
							</div>
						{/each}
					</div>
					<!-- Floating labels -->
					<div class="absolute top-4 left-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-teal-100 text-teal-600">Clinical AI</div>
					<div class="absolute bottom-4 right-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-teal-100 text-teal-600">Real-time</div>
				</div>
			</div>
			<!-- Card 2 -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<h3 class="text-2xl font-serif mb-4">Seamless EHR integration</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					Cleo integrates natively with Epic, Cerner, and Athena - syncing patient data, clinical notes, and charge capture in real-time without disrupting your existing workflows.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-6 h-48 flex items-center justify-center relative">
					<!-- Integration visual -->
					<div class="flex items-center justify-center gap-4">
						<div class="flex flex-col gap-3">
							<div class="w-16 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">EPIC</div>
							<div class="w-16 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">CERNER</div>
							<div class="w-16 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">ATHENA</div>
						</div>
						<div class="flex flex-col gap-1">
							<div class="w-12 h-px bg-teal-400"></div>
							<div class="w-12 h-px bg-teal-400"></div>
							<div class="w-12 h-px bg-teal-400"></div>
						</div>
						<div class="w-20 h-20 bg-gradient-to-br from-teal-500 to-cyan-500 rounded-lg flex items-center justify-center shadow-lg">
							<svg class="w-10 h-10 text-white" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path opacity="0.9" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
								<path opacity="0.9" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
							</svg>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Testimonial -->
	<section class="bg-dark-bg text-white py-32 relative overflow-hidden">
		<div class="max-w-4xl mx-auto px-6 text-center relative z-10">
			<div class="text-brand-primary text-6xl font-serif absolute -top-10 left-0 opacity-50">“</div>
			<blockquote class="text-3xl md:text-4xl font-serif leading-tight mb-12 relative">
				<span class="text-brand-primary absolute -left-4 -top-4">“</span>
				Cleo gave me back hours every shift. I can actually focus on my patients instead of drowning in documentation.
				<span class="text-brand-primary absolute -right-4 bottom-4">”</span>
			</blockquote>
			<div class="flex items-center justify-between border-t border-white/10 pt-8">
				<div class="text-sm font-mono tracking-wide uppercase text-gray-400">Emergency Medicine Physician</div>
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
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+PLATFORM</div>
			<h2 class="text-5xl md:text-6xl font-serif mb-4">
				Complete Acute Care <br />
				Suite
			</h2>
			<p class="text-gray-600 mb-6">From patient entry to follow-up, supporting clinicians throughout the entire stay</p>
			<div class="flex items-center justify-center gap-2 text-gray-500 text-sm font-semibold">
				<svg class="w-4 h-4 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
					<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
				</svg>
				HIPAA Compliant
			</div>
		</div>

		<!-- Feature Nav -->
		<div class="flex flex-wrap justify-center gap-6 text-sm text-gray-400 mb-16 border-b border-gray-100 pb-4 max-w-6xl mx-auto px-6">
			<span>Ambient AI Notes</span>
			<span>Charge Capture</span>
			<span>Census Management</span>
			<span class="text-black font-medium border-b-2 border-black pb-4 -mb-4.5">CDI Support</span>
			<span>Patient Follow-up</span>
			<span>EHR Integration</span>
		</div>

		<div class="max-w-6xl mx-auto px-6 space-y-8">
			<!-- Row 1: Ambient AI Notes -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Ambient AI Documentation</h3>
					<p class="text-gray-600 text-sm leading-relaxed">
						Real-time capture of clinical conversations transformed into structured notes, eliminating hours of after-shift charting
					</p>
				</div>
				<div class="bg-white shadow-lg shadow-gray-200/50 border border-gray-200 rounded-lg p-6 transform rotate-1 transition-transform hover:rotate-0">
					<div class="flex items-center gap-2 mb-4 pb-2 border-b border-gray-100">
						<div class="w-2 h-2 bg-red-500 rounded-full animate-pulse"></div>
						<span class="text-xs text-gray-600 font-medium">Recording Patient Encounter</span>
					</div>
					<div class="space-y-3 text-xs">
						<div class="bg-teal-50 border-l-2 border-teal-400 p-2 rounded">
							<div class="font-semibold text-gray-700 mb-1">Chief Complaint</div>
							<div class="text-gray-600">Chest pain, 2 hours duration</div>
						</div>
						<div class="bg-gray-50 border-l-2 border-gray-300 p-2 rounded">
							<div class="font-semibold text-gray-700 mb-1">History of Present Illness</div>
							<div class="text-gray-600">58M presents with substernal...</div>
						</div>
						<div class="flex items-center gap-2 text-[10px] text-teal-600">
							<svg class="w-3 h-3 animate-spin" fill="none" viewBox="0 0 24 24">
								<circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
								<path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
							</svg>
							<span>AI transcribing...</span>
						</div>
					</div>
				</div>
			</div>

			<!-- Row 2: Charge Capture & Census Management -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-gradient-to-br from-teal-50 to-cyan-50 rounded-2xl p-8 md:p-12 relative overflow-hidden">
					<div class="relative z-10">
						<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 mb-6">
							<div class="flex items-center justify-between mb-3">
								<span class="text-xs font-semibold text-gray-700">Today's Charges</span>
								<span class="text-xs text-teal-600">Auto-captured</span>
							</div>
							<div class="text-2xl font-bold text-gray-900 mb-1">$47,892</div>
							<div class="text-[10px] text-gray-500">23 encounters documented</div>
						</div>
						<h3 class="text-2xl font-serif mb-2">Intelligent Charge Capture</h3>
						<p class="text-gray-600 text-xs">Automatically identify and document billable services, reducing revenue leakage</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
					<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 mb-8 max-w-xs mx-auto">
						<div class="text-xs font-semibold mb-3 border-b border-gray-100 pb-2">Census Overview</div>
						<div class="space-y-3">
							<div class="flex items-center justify-between text-xs">
								<span class="text-gray-600">ED Beds</span>
								<span class="font-bold">42/48</span>
							</div>
							<div class="flex items-center justify-between text-xs">
								<span class="text-gray-600">ICU</span>
								<span class="font-bold">18/20</span>
							</div>
							<div class="flex items-center justify-between text-xs">
								<span class="text-gray-600">Med/Surg</span>
								<span class="font-bold">156/180</span>
							</div>
							<div class="pt-2 border-t border-gray-100">
								<div class="flex items-center gap-2 text-[10px] text-teal-600">
									<svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20">
										<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
									</svg>
									<span>Real-time sync</span>
								</div>
							</div>
						</div>
					</div>
					<h3 class="text-2xl font-serif mb-2">Census Management</h3>
					<p class="text-gray-600 text-xs">Real-time bed tracking and patient flow optimization across all units</p>
				</div>
			</div>

			<!-- Row 3: CDI Support -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Clinical Documentation Integrity</h3>
					<p class="text-gray-600 text-sm leading-relaxed mb-6">
						AI-powered CDI support ensures documentation meets quality standards and accurately reflects care complexity
					</p>
					<div class="space-y-2 text-xs">
						<div class="flex items-center gap-2 text-teal-600">
							<svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
								<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
							</svg>
							<span class="text-gray-700">Automated quality checks</span>
						</div>
						<div class="flex items-center gap-2 text-teal-600">
							<svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
								<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
							</svg>
							<span class="text-gray-700">Coding suggestions</span>
						</div>
					</div>
				</div>
				<div class="relative h-48">
					<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 h-full flex flex-col justify-center">
						<div class="space-y-3">
							<div class="flex items-start gap-2">
								<div class="w-5 h-5 bg-yellow-100 rounded flex items-center justify-center flex-shrink-0 mt-0.5">
									<span class="text-yellow-600 text-xs">!</span>
								</div>
								<div class="text-xs">
									<div class="font-semibold text-gray-700 mb-1">Documentation Gap</div>
									<div class="text-gray-600">Consider documenting severity for more accurate coding</div>
								</div>
							</div>
							<div class="flex items-start gap-2">
								<div class="w-5 h-5 bg-teal-100 rounded flex items-center justify-center flex-shrink-0 mt-0.5">
									<svg class="w-3 h-3 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
										<path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
									</svg>
								</div>
								<div class="text-xs">
									<div class="font-semibold text-gray-700 mb-1">Quality Check Passed</div>
									<div class="text-gray-600">Documentation meets standards</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Row 4: 3 Cards -->
			<div class="grid md:grid-cols-3 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-4 mb-6 shadow-sm">
						<div class="flex items-center gap-2 mb-2">
							<div class="w-4 h-4 rounded-full bg-teal-500"></div>
							<span class="text-xs font-semibold">Follow-up scheduled</span>
						</div>
						<div class="flex justify-between items-center text-[10px] text-gray-500">
							<span>12 patients today</span>
							<span class="underline">View queue</span>
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Patient Follow-up Calls</h3>
					<p class="text-gray-500 text-xs">AI-powered post-discharge follow-up to ensure continuity of care</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-3 mb-6 shadow-sm max-w-[200px]">
						<div class="text-[10px] text-gray-400 mb-1">Preferred format</div>
						<div class="flex items-center gap-2 text-xs font-medium mb-1">
							<div class="w-4 h-4 bg-teal-500 text-white flex items-center justify-center rounded text-[8px]">✓</div>
							Custom Templates
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Clinician Preferences</h3>
					<p class="text-gray-500 text-xs">Cleo learns your documentation style and adapts to your workflow</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="flex gap-2 mb-6 justify-center">
						<div class="w-10 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">EPIC</div>
						<div class="w-10 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">CERNER</div>
						<div class="w-10 h-10 bg-gray-100 rounded border border-gray-200 flex items-center justify-center text-[8px] font-bold text-gray-400">ATHENA</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Major EHR Integration</h3>
					<p class="text-gray-500 text-xs">Seamless bi-directional sync with Epic, Cerner, and Athena</p>
				</div>
			</div>

			<!-- Row 5: 2 Cards -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8 flex flex-col justify-between">
					<div class="bg-white border border-gray-200 rounded-lg px-4 py-3 shadow-sm mb-8">
						<div class="flex items-center gap-2 mb-2">
							<svg class="w-4 h-4 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
								<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
							</svg>
							<span class="text-xs font-semibold">Version Control</span>
						</div>
						<div class="text-[10px] text-gray-500">All changes tracked and reversible</div>
					</div>
					<div>
						<h3 class="text-xl font-serif mb-2">Edit History & Rollback</h3>
						<p class="text-gray-500 text-xs">Complete audit trail with ability to revert any changes</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-teal-600 text-white rounded px-3 py-1.5 text-xs inline-flex items-center gap-2 mb-4">
						<svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20">
							<path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
							<path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
						</svg>
						Voice-to-text active
					</div>
					<div class="bg-white border border-gray-200 rounded-lg p-4 mb-6">
						<div class="flex items-center gap-2 mb-2">
							<div class="w-2 h-2 bg-red-500 rounded-full animate-pulse"></div>
							<span class="text-xs font-medium text-gray-700">Listening...</span>
						</div>
						<div class="space-y-1">
							<div class="h-1 w-full bg-teal-100 rounded"></div>
							<div class="h-1 w-3/4 bg-teal-100 rounded"></div>
							<div class="h-1 w-5/6 bg-teal-100 rounded"></div>
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Voice Recognition</h3>
					<p class="text-gray-500 text-xs">Hands-free documentation with medical-grade speech recognition</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Data Sources -->
	<section class="bg-dark-bg text-white py-24 border-t border-white/5">
		<div class="max-w-4xl mx-auto px-6 text-center">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">\+INTEGRATIONS</div>
			<h2 class="text-3xl md:text-5xl font-serif mb-6">Seamless integration with your EHR</h2>
			<p class="text-gray-400 mb-12">Bi-directional sync with major electronic health record systems</p>

			<div class="bg-[#0A1F1E] border border-white/10 rounded-xl overflow-hidden max-w-md mx-auto relative">
				<div class="p-4 flex items-center gap-4 border-b border-white/5 bg-[#0F2928] relative z-10">
					<div class="w-8 h-8 bg-white rounded flex items-center justify-center shadow-lg shadow-brand-green/20">
						<div class="w-4 h-4 bg-black grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div>
					</div>
					<div class="text-left">
						<div class="text-sm font-medium text-white">Cleo Health Platform</div>
						<div class="text-[10px] text-brand-primary flex items-center gap-1">
							<span class="w-1 h-1 bg-brand-green rounded-full animate-pulse"></span>
							Syncing with EHR...
						</div>
					</div>
				</div>
				
				<!-- Connecting line visual -->
				<div class="absolute left-8 top-12 bottom-0 w-px bg-gradient-to-b from-white/20 to-transparent z-0"></div>

				<div class="divide-y divide-white/5 text-sm text-gray-400 text-left relative z-10">
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Epic</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Cerner</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Athena</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary">Connected</span>
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
				<h2 class="text-4xl md:text-5xl font-serif mb-6">HIPAA-Compliant Security</h2>
				<p class="text-gray-600 mb-8 leading-relaxed">
					Patient data is fully HIPAA compliant with enterprise-grade encryption both in transit and at rest. We utilize AES-256 for storage and TLS 1.3 for secure communication. Your data is never used for model training.
				</p>
				<a href="#" class="inline-flex items-center gap-2 font-medium hover:underline">
					<div class="w-5 h-5 bg-black text-white flex items-center justify-center rounded-sm text-xs">→</div>
					Learn more
				</a>
			</div>
			<div class="grid grid-cols-2 gap-px bg-gray-200 border border-gray-200">
				<!-- HIPAA -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border-2 border-teal-600 flex flex-col items-center justify-center relative p-2">
						<div class="absolute inset-1 border border-teal-600 rounded-full"></div>
						<div class="text-lg font-bold leading-none text-teal-600">HIPAA</div>
						<div class="text-[8px] uppercase tracking-widest font-semibold mt-1">Compliant</div>
					</div>
				</div>
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
		<div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-brand-primary/20 to-transparent pointer-events-none"></div>

		<div class="max-w-4xl mx-auto px-6 relative z-10">
			<div class="text-[10px] uppercase tracking-widest text-brand-primary mb-4">+TRANSFORM YOUR PRACTICE</div>
			<h2 class="text-5xl md:text-7xl font-serif mb-12 leading-tight">
				Give your clinicians back time to focus on patients
			</h2>
			<div class="flex flex-wrap gap-4">
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Schedule Demo
				</button>
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Contact Sales
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
					<div class="flex items-center gap-2">
						<svg class="w-6 h-6 text-brand-primary" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
							<path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
							<path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
						</svg>
						<span class="text-white font-serif text-xl">Cleo Health</span>
					</div>
					<span class="text-xs text-gray-600">© 2025 Cleo Health. All Rights Reserved</span>
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
				Cleo
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

