<script lang="ts">
	// FAQ Data
	let faqs = $state([
		{ q: 'How do I get started with Nolla?', a: 'Download the Nolla app on iOS and follow a simple guided scan using your phone\'s camera. In just a few steps, you\'ll receive AI-powered insights and a personalized care plan from a licensed doctor. No waiting rooms. No referrals.', open: true },
		{ q: 'Who is Nolla for?', a: 'Nolla is for anyone looking for accessible, personalized skin care.', open: false },
		{ q: 'Is my diagnosis reviewed by a real doctor?', a: 'Yes, every diagnosis is reviewed by a board-certified dermatologist.', open: false },
		{ q: 'Does Nolla require insurance?', a: 'No, Nolla is designed to be affordable without insurance.', open: false },
		{ q: 'What\'s next for Nolla?', a: 'We are expanding to more conditions soon.', open: false }
	]);

	function toggleFaq(index: number) {
		faqs[index].open = !faqs[index].open;
	}
</script>

<svelte:head>
	<title>Nolla - Skip the clinic</title>
</svelte:head>

<div class="w-full overflow-hidden bg-[#F9F8F6]">
	<!-- Hero Section -->
	<section class="relative pt-32 pb-0 text-center px-4 md:px-6 max-w-7xl mx-auto">
		<h1 class="text-5xl md:text-7xl font-serif text-[#1A1A1A] mb-8 leading-tight tracking-tight">
			Skip the clinic<br />with Nolla
		</h1>
		<p class="text-lg md:text-xl text-gray-600 mb-10 max-w-2xl mx-auto font-sans leading-relaxed">
			Get personalized skin treatment, powered by AI<br class="hidden md:block" /> and real doctors.
		</p>
		<button class="bg-[#1A1A1A] text-white px-10 py-4 rounded-full font-medium hover:bg-gray-800 transition-all hover:scale-105 mb-20 shadow-lg">
			Start Your Assessment
		</button>

		<div class="relative w-full max-w-5xl mx-auto mt-8">
			<!-- Main Couple Image Placeholder -->
			<div class="relative z-10 mx-auto">
				<img 
					src="https://images.unsplash.com/photo-1629249726222-6c3c53324639?q=80&w=2070&auto=format&fit=crop" 
					alt="Couple smiling" 
					class="w-full max-w-2xl mx-auto rounded-t-[3rem] object-cover h-[400px] md:h-[550px]"
					style="mask-image: linear-gradient(to bottom, black 70%, transparent 100%); -webkit-mask-image: linear-gradient(to bottom, black 70%, transparent 100%);"
				/>
			</div>

			<!-- Floating UI Elements (Mockups) -->
			<!-- Left Card: Acne Score -->
			<div class="absolute top-20 left-0 md:left-4 bg-white p-5 rounded-3xl shadow-[0_20px_50px_rgba(0,0,0,0.1)] z-20 w-56 hidden lg:block transform -rotate-3 transition-transform hover:rotate-0 duration-500">
				<div class="flex justify-between items-center mb-4">
					<span class="text-xs font-bold text-gray-900">Acne Score</span>
					<div class="w-5 h-5 bg-blue-50 rounded-full flex items-center justify-center text-[10px] text-blue-600 font-bold">?</div>
				</div>
				<div class="h-2 bg-gray-100 rounded-full mb-3 overflow-hidden">
					<div class="h-full bg-blue-500 w-[53%] rounded-full"></div>
				</div>
				<div class="flex justify-between text-[10px] text-gray-400 mb-1 uppercase tracking-wider font-medium">
					<span>Current</span>
					<span>Goal</span>
				</div>
				<div class="flex justify-between font-serif text-lg text-gray-900">
					<span>53/100</span>
					<span>95/100</span>
				</div>
			</div>

			<!-- Right Card: Intake -->
			<div class="absolute top-32 right-0 md:right-4 bg-white p-5 rounded-3xl shadow-[0_20px_50px_rgba(0,0,0,0.1)] z-20 w-52 hidden lg:block transform rotate-3 transition-transform hover:rotate-0 duration-500">
				<div class="text-center">
					<div class="relative w-16 h-16 mx-auto mb-3 flex items-center justify-center">
                        <!-- Circular progress svg -->
                        <svg class="w-full h-full transform -rotate-90">
                            <circle cx="32" cy="32" r="28" stroke="#f3f4f6" stroke-width="4" fill="none" />
                            <circle cx="32" cy="32" r="28" stroke="#3b82f6" stroke-width="4" fill="none" stroke-dasharray="175" stroke-dashoffset="140" stroke-linecap="round" />
                        </svg>
                        <div class="absolute inset-0 flex items-center justify-center text-blue-500">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                        </div>
                    </div>
					<h3 class="font-serif text-lg mb-1">Start your<br>intake</h3>
				</div>
			</div>
		</div>
	</section>

	<!-- Value Proposition Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto">
		<div class="flex flex-col md:flex-row items-start justify-between gap-12">
			<div class="md:w-1/6 pt-2">
				<!-- Icon placeholder -->
				<div class="w-12 h-12 relative">
					<svg viewBox="0 0 24 24" fill="none" class="w-12 h-12 text-[#D2B48C]">
						<path d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M9 14l2 2 4-4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
				</div>
			</div>
			<div class="md:w-2/3">
				<h2 class="text-3xl md:text-5xl font-serif leading-tight mb-8 text-[#1A1A1A]">
					Nolla combines cutting-edge AI with real doctors to deliver fast, personalized care for you and your health.
				</h2>
				<p class="text-2xl md:text-3xl font-serif text-[#D2B48C] leading-tight opacity-60">
					Get instant analysis, expert review, and seamless treatment delivery - all from your phone.
				</p>
			</div>
			<div class="md:w-1/6 flex justify-end items-end">
				<!-- Product bottles illustration -->
				<div class="flex items-end gap-2">
					<div class="w-10 h-8 bg-[#1A1A1A] rounded-sm"></div>
					<div class="w-6 h-12 bg-[#D2B48C] rounded-t-full opacity-50"></div>
				</div>
			</div>
		</div>
	</section>

	<!-- Products Section -->
	<section class="py-12 px-4 md:px-6 max-w-7xl mx-auto">
		<p class="text-sm text-gray-500 mb-8 font-medium">Our products</p>
		
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			<!-- Acne Treatment Card -->
			<div class="bg-[#E3EFF3] rounded-[2rem] p-8 md:p-12 relative overflow-hidden min-h-[600px] flex flex-col">
				<div class="relative z-10">
					<div class="flex items-center gap-2 mb-4 text-xs font-bold uppercase tracking-wider text-gray-600">
						<span class="w-2 h-2 bg-black rounded-full"></span>
						Nolla Acne
					</div>
					<h3 class="text-3xl font-serif mb-4">Acne Treatment</h3>
					<p class="text-gray-600 mb-8 max-w-xs text-sm">Scan your face, get an AI-powered clinician-reviewed treatment, and track results. All from your phone.</p>
					<div class="flex gap-4 items-center">
						<button class="bg-[#1A1A1A] text-white px-6 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">Learn more</button>
						<button class="bg-white px-4 py-3 rounded-full flex items-center gap-2 text-sm font-medium hover:bg-gray-50 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.23-3.14-2.47-1.72-2.47-3.03-7.01-1.27-10.06 0.86-1.49 2.39-2.43 4.07-2.46 1.3-.03 2.53.88 3.32.88.78 0 2.25-1.09 3.79-.93 1.29.1 2.45.65 3.19 1.71-2.8 1.68-2.33 6.01.6 7.23-.62 1.54-1.46 3.06-2.17 4.12l-.01-.01zM13 3.5c.66-1.6 2.67-2.5 4.38-2.5.34 1.94-1.75 3.91-4.38 2.5z"/></svg>
							App Store
						</button>
					</div>
				</div>
				
				<!-- Phone Mockup -->
				<div class="absolute bottom-[-50px] left-1/2 transform -translate-x-1/2 w-64 md:w-72">
					<div class="bg-white rounded-[2.5rem] border-8 border-white shadow-xl overflow-hidden h-[500px]">
						<!-- Screen Content -->
						<div class="bg-gray-50 h-full p-4 flex flex-col">
							<div class="text-center mt-4 mb-4">
								<h4 class="font-serif text-lg">Treatment plan</h4>
							</div>
							<div class="flex-1 bg-white rounded-xl p-2 shadow-sm mb-2">
								<div class="w-full h-32 bg-gray-200 rounded-lg mb-2 overflow-hidden">
                                    <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover" alt="Face scan" />
                                </div>
								<div class="space-y-2">
									<div class="h-2 bg-gray-100 rounded w-3/4"></div>
									<div class="h-2 bg-gray-100 rounded w-1/2"></div>
								</div>
							</div>
                            <div class="bg-black text-white p-3 rounded-xl text-center text-xs mt-auto">
                                Start Treatment
                            </div>
						</div>
					</div>
				</div>
			</div>

			<!-- Skin Cancer Assessment Card -->
			<div class="bg-[#F3E4D3] rounded-[2rem] p-8 md:p-12 relative overflow-hidden min-h-[600px] flex flex-col">
				<div class="relative z-10">
					<div class="flex items-center gap-2 mb-4 text-xs font-bold uppercase tracking-wider text-gray-600">
						<span class="w-2 h-2 bg-black rounded-full"></span>
						Nolla Moles
					</div>
					<h3 class="text-3xl font-serif mb-4">Skin Cancer Assessment</h3>
					<p class="text-gray-600 mb-8 max-w-xs text-sm">Snap a photo of your mole, get an AI-powered doctor-reviewed risk check and next-step guidance.</p>
					<div class="flex gap-4 items-center">
						<button class="bg-[#1A1A1A] text-white px-6 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">Learn more</button>
						<button class="bg-white px-4 py-3 rounded-full flex items-center gap-2 text-sm font-medium hover:bg-gray-50 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.23-3.14-2.47-1.72-2.47-3.03-7.01-1.27-10.06 0.86-1.49 2.39-2.43 4.07-2.46 1.3-.03 2.53.88 3.32.88.78 0 2.25-1.09 3.79-.93 1.29.1 2.45.65 3.19 1.71-2.8 1.68-2.33 6.01.6 7.23-.62 1.54-1.46 3.06-2.17 4.12l-.01-.01zM13 3.5c.66-1.6 2.67-2.5 4.38-2.5.34 1.94-1.75 3.91-4.38 2.5z"/></svg>
							App Store
						</button>
					</div>
				</div>

				<!-- Phone Mockup -->
				<div class="absolute bottom-[-50px] left-1/2 transform -translate-x-1/2 w-64 md:w-72">
					<div class="bg-white rounded-[2.5rem] border-8 border-white shadow-xl overflow-hidden h-[500px]">
						<!-- Screen Content -->
						<div class="bg-gray-50 h-full p-4 flex flex-col">
                            <div class="text-center mt-4 mb-4">
								<h4 class="font-serif text-lg">Welcome to Nolla</h4>
							</div>
							<div class="bg-blue-600 text-white p-4 rounded-xl mb-3">
                                <h5 class="font-serif text-lg mb-1">Start scanning</h5>
                                <p class="text-[10px] opacity-80">Take a photo of your skin concern</p>
                            </div>
                            <div class="bg-white p-4 rounded-xl shadow-sm mb-3">
                                <h5 class="font-serif text-sm mb-1">Schedule an appointment</h5>
                                <p class="text-[10px] text-gray-500">Book a video call with a dermatologist</p>
                            </div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Future of Nolla Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto">
		<div class="flex flex-col lg:flex-row gap-16">
			<div class="lg:w-1/2">
				<h2 class="text-3xl md:text-4xl font-serif mb-6 text-[#1A1A1A]">The Future of Nolla</h2>
				<p class="text-gray-600 mb-6 leading-relaxed">
					We're starting with skin, the body's most visible health signal, as we build toward a full-spectrum AI doctor that supports your entire health journey.
				</p>
				<p class="text-gray-600 mb-8 leading-relaxed">
					Join our vision to make personalized, accessible care available to everyone—anytime, anywhere.
				</p>
				<button class="bg-[#1A1A1A] text-white px-8 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
					Explore Our Mission
				</button>
			</div>
			
			<div class="lg:w-1/2 flex gap-4 md:gap-6">
				<!-- Acne Care Card -->
				<div class="w-1/2 bg-[#F0F0F0] rounded-[2rem] overflow-hidden relative aspect-[4/5]">
					<img src="https://images.unsplash.com/photo-1531384441138-2736e62e0919?q=80&w=1000&auto=format&fit=crop" alt="Man smiling" class="absolute inset-0 w-full h-full object-cover" />
					<div class="absolute top-6 left-6 z-10">
						<span class="text-sm font-medium text-black">Acne Care</span>
					</div>
					<div class="absolute bottom-6 left-6 z-10">
						<button class="bg-white/90 backdrop-blur-sm px-3 py-1.5 rounded-full flex items-center gap-1 text-[10px] font-bold shadow-sm">
							<svg class="w-3 h-3" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.23-3.14-2.47-1.72-2.47-3.03-7.01-1.27-10.06 0.86-1.49 2.39-2.43 4.07-2.46 1.3-.03 2.53.88 3.32.88.78 0 2.25-1.09 3.79-.93 1.29.1 2.45.65 3.19 1.71-2.8 1.68-2.33 6.01.6 7.23-.62 1.54-1.46 3.06-2.17 4.12l-.01-.01zM13 3.5c.66-1.6 2.67-2.5 4.38-2.5.34 1.94-1.75 3.91-4.38 2.5z"/></svg>
							App Store
						</button>
					</div>
				</div>
				
				<!-- Mole Scan Card -->
				<div class="w-1/2 bg-[#F3E4D3] rounded-[2rem] overflow-hidden relative aspect-[4/5]">
					<img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=1000&auto=format&fit=crop" alt="Woman smiling" class="absolute inset-0 w-full h-full object-cover" />
					<div class="absolute top-6 left-6 z-10">
						<span class="text-sm font-medium text-black">Mole Scan</span>
					</div>
					<div class="absolute bottom-6 left-6 z-10">
						<button class="bg-white/90 backdrop-blur-sm px-3 py-1.5 rounded-full flex items-center gap-1 text-[10px] font-bold shadow-sm">
							<svg class="w-3 h-3" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.23-3.14-2.47-1.72-2.47-3.03-7.01-1.27-10.06 0.86-1.49 2.39-2.43 4.07-2.46 1.3-.03 2.53.88 3.32.88.78 0 2.25-1.09 3.79-.93 1.29.1 2.45.65 3.19 1.71-2.8 1.68-2.33 6.01.6 7.23-.62 1.54-1.46 3.06-2.17 4.12l-.01-.01zM13 3.5c.66-1.6 2.67-2.5 4.38-2.5.34 1.94-1.75 3.91-4.38 2.5z"/></svg>
							App Store
						</button>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Join Our Journey Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto border-t border-gray-200">
		<div class="mb-12">
			<span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs font-medium mb-4 inline-block">Coming soon</span>
			<h2 class="text-3xl md:text-4xl font-serif mb-4 text-[#1A1A1A]">Join Our Journey</h2>
			<p class="text-gray-600 max-w-2xl">
				We're building a care model that evolves with your health - proactively, continuously, and intelligently.
			</p>
		</div>

		<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-3 gap-4">
			{#each ['Birth Control', 'Menopause', 'Allergies', 'Diabetes', 'Cardiology', 'Insomnia', 'Preventative', 'Weight Management', 'Chronic Pain', 'Blood Pressure', 'Vision', 'Hair Loss'] as item}
				<div class="border border-gray-200 rounded-full p-4 flex items-center justify-center hover:border-black hover:bg-white transition-all cursor-default bg-white/50">
					<span class="text-sm text-gray-600 font-medium">{item}</span>
				</div>
			{/each}
		</div>
	</section>

	<!-- Why Nolla Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto bg-[#F9F8F6]">
		<div class="text-center mb-24">
			<span class="bg-white px-4 py-2 rounded-full text-xs font-medium border border-gray-100 shadow-sm mb-6 inline-block">How it works</span>
			<h2 class="text-4xl md:text-5xl font-serif mb-6 text-[#1A1A1A]">Why Nolla?</h2>
			<p class="text-gray-600 max-w-xl mx-auto">
				Our platform is trained on over one million real dermatology cases and supports over 1,600 conditions.
			</p>
		</div>

		<!-- Step 1 -->
		<div class="flex flex-col items-center mb-32">
			<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2">Step 1</span>
			<h3 class="text-xl font-serif mb-12">You scan your skin</h3>
			
			<div class="relative w-full max-w-md h-80 flex items-center justify-center">
				<!-- Abstract Hand holding phone illustration -->
				<div class="relative w-64 h-64">
                    <!-- Simple shapes to represent hand holding phone -->
                    <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-40 h-40 bg-[#E8DCC6] rounded-full opacity-50"></div>
                    <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 w-24 h-48 bg-white rounded-[2rem] border-2 border-gray-100 shadow-lg flex items-center justify-center">
                        <div class="w-16 h-32 bg-gray-50 rounded-xl"></div>
                    </div>
                    <!-- Decorative squares -->
                    <div class="absolute top-0 right-10 w-8 h-8 bg-white opacity-50 rotate-12"></div>
                    <div class="absolute bottom-20 left-0 w-6 h-6 bg-white opacity-50 -rotate-12"></div>
                </div>
			</div>
		</div>

		<!-- Step 2 -->
		<div class="flex flex-col items-center mb-32">
			<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2">Step 2</span>
			<h3 class="text-xl font-serif mb-2 text-center">With the help of AI, we compare your<br>case against thousands of other<br>cases.</h3>
			
			<div class="relative w-full max-w-3xl h-[500px] mt-12">
				<!-- Cloud of faces simulation -->
				<div class="absolute inset-0 flex items-center justify-center">
                    <!-- Central Face -->
                    <div class="w-16 h-16 rounded-full overflow-hidden border-2 border-white shadow-lg z-20">
                         <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=200&auto=format&fit=crop" class="w-full h-full object-cover" alt="Face" />
                    </div>
                    
                    <!-- Ring 1 -->
                    {#each [0, 60, 120, 180, 240, 300] as angle}
                        <div class="absolute w-12 h-12 rounded-full overflow-hidden border-2 border-white shadow-md opacity-80" 
                             style="transform: rotate({angle}deg) translate(80px) rotate(-{angle}deg);">
                             <div class="w-full h-full bg-gray-200"></div>
                        </div>
                    {/each}

                     <!-- Ring 2 -->
                    {#each [15, 45, 75, 105, 135, 165, 195, 225, 255, 285, 315, 345] as angle}
                        <div class="absolute w-10 h-10 rounded-full overflow-hidden border-2 border-white shadow-sm opacity-60" 
                             style="transform: rotate({angle}deg) translate(140px) rotate(-{angle}deg);">
                             <div class="w-full h-full bg-gray-100"></div>
                        </div>
                    {/each}

                     <!-- Ring 3 -->
                    {#each [0, 20, 40, 60, 80, 100, 120, 140, 160, 180, 200, 220, 240, 260, 280, 300, 320, 340] as angle}
                        <div class="absolute w-8 h-8 rounded-full overflow-hidden border border-white opacity-30" 
                             style="transform: rotate({angle}deg) translate(200px) rotate(-{angle}deg);">
                             <div class="w-full h-full bg-gray-50"></div>
                        </div>
                    {/each}
                </div>
			</div>
		</div>

		<!-- Step 3 -->
		<div class="flex flex-col items-center mb-32">
			<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2">Step 3</span>
			<h3 class="text-xl font-serif mb-2 text-center">Our clinicians review your AI<br>assessment and create a personalized<br>treatment plan.</h3>
			
			<div class="relative w-full max-w-md h-[500px] mt-12 flex justify-center">
				<!-- Phone Mockup -->
                <div class="w-64 bg-white rounded-[2.5rem] border-8 border-white shadow-xl overflow-hidden h-full relative z-10">
                    <div class="bg-gray-50 h-full p-4 flex flex-col">
                        <div class="text-center mt-2 mb-4">
                            <h4 class="font-serif text-sm">Evening routine</h4>
                        </div>
                        <div class="flex-1 space-y-3 overflow-hidden">
                            <div class="bg-white p-3 rounded-xl shadow-sm flex gap-3 items-center">
                                <div class="w-10 h-10 bg-blue-100 rounded-lg"></div>
                                <div>
                                    <div class="h-2 bg-gray-200 w-20 rounded mb-1"></div>
                                    <div class="h-2 bg-gray-100 w-12 rounded"></div>
                                </div>
                            </div>
                            <div class="bg-white p-3 rounded-xl shadow-sm flex gap-3 items-center">
                                <div class="w-10 h-10 bg-green-100 rounded-lg"></div>
                                <div>
                                    <div class="h-2 bg-gray-200 w-24 rounded mb-1"></div>
                                    <div class="h-2 bg-gray-100 w-16 rounded"></div>
                                </div>
                            </div>
                             <div class="bg-white p-3 rounded-xl shadow-sm flex gap-3 items-center">
                                <div class="w-10 h-10 bg-purple-100 rounded-lg"></div>
                                <div>
                                    <div class="h-2 bg-gray-200 w-16 rounded mb-1"></div>
                                    <div class="h-2 bg-gray-100 w-10 rounded"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Doctor Illustration behind -->
                <div class="absolute top-20 -right-20 w-64 h-64 z-0 hidden md:block">
                     <!-- Abstract doctor shape -->
                     <svg viewBox="0 0 200 200" class="w-full h-full opacity-80">
                        <circle cx="100" cy="50" r="30" fill="#1A1A1A" />
                        <path d="M40,180 Q100,80 160,180" fill="#1A1A1A" />
                     </svg>
                </div>
			</div>
		</div>

		<!-- Built on Research -->
		<div class="text-center pt-12 border-t border-gray-200 max-w-4xl mx-auto">
			<p class="text-sm text-gray-500 mb-12">Built on Research. Backed by<br>Clinicians. Trusted by Real People.</p>
			
			<div class="grid grid-cols-2 md:grid-cols-3 gap-8 items-center justify-items-center opacity-60 grayscale">
				<!-- Logo Placeholders -->
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
                <div class="h-8 bg-gray-300 w-32 rounded"></div>
			</div>
		</div>
	</section>

	<!-- Social Proof Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto text-center">
		<div class="flex justify-center gap-2 mb-6">
			{#each ['1', '8', '6', '4', '4'] as num}
				<div class="w-12 h-16 bg-[#F9F8F6] flex items-center justify-center text-2xl font-serif text-[#1A1A1A] rounded">
					{num}
				</div>
			{/each}
		</div>
		<h2 class="text-2xl md:text-3xl font-serif mb-8 text-[#1A1A1A]">
			...people trust Nolla for better<br>skin.
		</h2>
		<button class="bg-[#1A1A1A] text-white px-8 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors mb-24">
			Join them
		</button>

		<!-- Testimonial Card -->
		<div class="bg-[#F9F8F6] rounded-[2rem] p-8 max-w-4xl mx-auto flex flex-col md:flex-row items-center gap-8 text-left">
			<div class="flex gap-4">
				<div class="relative">
					<div class="w-32 h-32 rounded-xl overflow-hidden bg-gray-200">
                        <img src="https://images.unsplash.com/photo-1554151228-14d9def656ec?q=80&w=300&auto=format&fit=crop" class="w-full h-full object-cover" alt="Before" />
                    </div>
					<span class="absolute top-2 left-2 bg-white/80 px-2 py-0.5 rounded text-[10px] font-bold">Before</span>
				</div>
				<div class="relative">
					<div class="w-32 h-32 rounded-xl overflow-hidden bg-gray-200">
                        <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=300&auto=format&fit=crop" class="w-full h-full object-cover" alt="After" />
                    </div>
					<span class="absolute top-2 left-2 bg-white/80 px-2 py-0.5 rounded text-[10px] font-bold">After</span>
				</div>
			</div>
			<div class="flex-1">
				<p class="text-xl font-serif mb-4">"Nolla gave me the clearest skin I've had in years. The process was so easy and practical"</p>
				<p class="text-sm text-gray-500 mb-6">Julie, 23</p>
				<div>
					<span class="text-4xl font-serif block mb-1">80%</span>
					<p class="text-xs text-gray-500">Improvement based on initial and last scan after 4 weeks of treatment</p>
				</div>
			</div>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto bg-[#F9F8F6] rounded-[3rem] mb-12">
		<div class="flex flex-col lg:flex-row gap-16 p-8 md:p-12">
			<div class="lg:w-1/3">
				<h2 class="text-3xl md:text-4xl font-serif mb-6 text-[#1A1A1A]">What You<br>Need to Know</h2>
                
                <!-- Man sitting image -->
                <div class="mt-12 relative rounded-2xl overflow-hidden h-64 w-full">
                    <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover object-top" alt="Man sitting" />
                </div>
			</div>
			
			<div class="lg:w-2/3">
				<div class="space-y-4">
                    {#each faqs as item, index}
                        <div class="border-b border-gray-200 py-4">
                            <button class="flex justify-between items-center w-full text-left font-medium text-lg" onclick={() => toggleFaq(index)}>
                                {item.q}
                                <span class="transform transition-transform {item.open ? 'rotate-180' : ''}">
                                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                                </span>
                            </button>
                            {#if item.open}
                                <div class="mt-4 text-gray-600 text-sm leading-relaxed">
                                    {item.a}
                                </div>
                            {/if}
                        </div>
                    {/each}
                    
                    <div class="mt-8">
                        <a href="#" class="text-sm font-medium flex items-center gap-1 hover:underline">
                            View all FAQ 
                            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                        </a>
                    </div>
				</div>
			</div>
		</div>
	</section>

	<!-- Recommended Articles -->
	<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto">
		<h2 class="text-3xl md:text-4xl font-serif mb-12 text-[#1A1A1A]">Recommended articles</h2>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Article 1 -->
			<div class="group cursor-pointer">
				<div class="rounded-2xl overflow-hidden mb-6 h-64 bg-gray-200">
                    <img src="https://images.unsplash.com/photo-1556228552-523cd13b8610?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Skin closeup" />
                </div>
				<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2 block">Research</span>
				<h3 class="text-lg font-medium mb-2 group-hover:text-gray-600 transition-colors">Automated Acne Severity Scoring at Nolla</h3>
				<p class="text-xs text-gray-400">October 06, 2025</p>
			</div>
			
			<!-- Article 2 -->
			<div class="group cursor-pointer">
				<div class="rounded-2xl overflow-hidden mb-6 h-64 bg-gray-200">
                    <img src="https://images.unsplash.com/photo-1616394584738-fc6e612e71b9?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="Treat Acne" />
                </div>
				<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2 block">Announcements</span>
				<h3 class="text-lg font-medium mb-2 group-hover:text-gray-600 transition-colors">Nolla Health Debuts AI-Powered Skin Health Platform In U.S.</h3>
				<p class="text-xs text-gray-400">September 01, 2025</p>
			</div>
			
			<!-- Article 3 -->
			<div class="group cursor-pointer">
				<div class="rounded-2xl overflow-hidden mb-6 h-64 bg-gray-200">
                    <img src="https://images.unsplash.com/photo-1551847677-dc82d764e1eb?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" alt="App screens" />
                </div>
				<span class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-2 block">Announcements</span>
				<h3 class="text-lg font-medium mb-2 group-hover:text-gray-600 transition-colors">What do you feel like you need help with?</h3>
				<p class="text-xs text-gray-400">September 01, 2025</p>
			</div>
		</div>
	</section>

	<!-- Footer CTA -->
	<section class="px-4 md:px-6 max-w-7xl mx-auto mb-12">
		<div class="bg-[#F9F8F6] rounded-[3rem] p-8 md:p-16 flex flex-col md:flex-row items-center justify-between relative overflow-hidden">
			<div class="relative z-10 md:w-1/2">
				<div class="w-8 h-8 bg-black rounded-lg mb-6 flex items-center justify-center">
                    <div class="w-4 h-4 bg-white rounded-sm"></div>
                </div>
				<h2 class="text-4xl md:text-5xl font-serif mb-4 text-[#1A1A1A]">Ready to Try?</h2>
				<p class="text-gray-600 mb-8">Join Nolla Today.</p>
				<button class="bg-[#1A1A1A] text-white px-6 py-3 rounded-full flex items-center gap-2 text-sm font-medium hover:bg-gray-800 transition-colors">
					<svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.23-3.14-2.47-1.72-2.47-3.03-7.01-1.27-10.06 0.86-1.49 2.39-2.43 4.07-2.46 1.3-.03 2.53.88 3.32.88.78 0 2.25-1.09 3.79-.93 1.29.1 2.45.65 3.19 1.71-2.8 1.68-2.33 6.01.6 7.23-.62 1.54-1.46 3.06-2.17 4.12l-.01-.01zM13 3.5c.66-1.6 2.67-2.5 4.38-2.5.34 1.94-1.75 3.91-4.38 2.5z"/></svg>
					App Store
				</button>
			</div>
			
			<div class="md:w-1/2 flex justify-end mt-8 md:mt-0 relative">
                 <!-- Woman smiling -->
                 <img src="https://images.unsplash.com/photo-1531123897727-8f129e1688ce?q=80&w=1000&auto=format&fit=crop" class="w-64 h-64 md:w-80 md:h-80 object-cover rounded-full md:rounded-none md:rounded-l-full" alt="Woman smiling" />
			</div>
		</div>
	</section>

	<!-- Footer Links -->
	<footer class="px-4 md:px-6 max-w-7xl mx-auto py-12 border-t border-gray-100">
		<div class="flex flex-col md:flex-row justify-between gap-12">
			<div class="grid grid-cols-2 md:grid-cols-4 gap-8 md:gap-16 w-full md:w-2/3">
				<div>
					<h4 class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-4">Nolla Products</h4>
					<ul class="space-y-2 text-sm text-gray-600">
						<li><a href="#" class="hover:text-black">Acne Treatment</a></li>
						<li><a href="#" class="hover:text-black">Skin Cancer Assessment</a></li>
					</ul>
				</div>
				<div>
					<h4 class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-4">Nolla Company</h4>
					<ul class="space-y-2 text-sm text-gray-600">
						<li><a href="#" class="hover:text-black">Mission</a></li>
						<li><a href="#" class="hover:text-black">About</a></li>
						<li><a href="#" class="hover:text-black">FAQs</a></li>
						<li><a href="#" class="hover:text-black">Learning</a></li>
						<li><a href="#" class="hover:text-black">Blog</a></li>
					</ul>
				</div>
				<div class="col-span-2">
					<h4 class="text-xs font-bold text-gray-400 uppercase tracking-widest mb-4">Learning</h4>
					<div class="grid grid-cols-2 gap-4">
						<ul class="space-y-2 text-sm text-gray-600">
							<li><a href="#" class="hover:text-black">Lifestyle & Skin Triggers</a></li>
							<li><a href="#" class="hover:text-black">Products & Ingredients</a></li>
							<li><a href="#" class="hover:text-black">Skincare Basics</a></li>
						</ul>
						<ul class="space-y-2 text-sm text-gray-600">
							<li><a href="#" class="hover:text-black">Treatment 101</a></li>
						</ul>
					</div>
				</div>
			</div>
			
			<div class="w-full md:w-1/3">
				<div class="flex gap-2">
					<input type="email" placeholder="Your email address" class="flex-1 bg-gray-50 border border-gray-200 rounded-full px-4 py-2 text-sm focus:outline-none focus:border-gray-400" />
					<button class="bg-gray-100 text-gray-600 px-4 py-2 rounded-full text-xs font-medium hover:bg-gray-200 transition-colors">Subscribe</button>
				</div>
			</div>
		</div>
		
		<div class="flex flex-col md:flex-row justify-between items-center mt-12 pt-8 border-t border-gray-100 gap-4">
			<div class="flex items-center gap-4">
				<a href="#" class="text-gray-400 hover:text-black">
					<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
				</a>
				<a href="#" class="text-gray-400 hover:text-black">
					<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"/></svg>
				</a>
				<div class="text-xs text-gray-400 font-medium">EN</div>
			</div>
			
			<div class="flex gap-6 text-[10px] text-gray-400">
				<a href="#" class="hover:text-gray-600">Privacy Policy</a>
				<a href="#" class="hover:text-gray-600">Terms and Conditions</a>
				<span>© Nolla 2025</span>
			</div>
			
			<div class="flex gap-2 opacity-50 grayscale">
				<!-- Badges -->
				<div class="w-8 h-8 bg-gray-200 rounded-full"></div>
				<div class="w-12 h-8 bg-gray-200 rounded"></div>
			</div>
		</div>
		
		<div class="mt-8 pt-8 border-t border-gray-100 text-[10px] text-gray-400 text-center leading-relaxed">
			Nolla uses advanced AI to support clinical decisions, but all diagnoses and treatments are reviewed by licensed medical professionals. Our services comply with local healthcare regulations and are HIPAA compliant. Nolla is not a substitute for emergency medical care. Availability may vary by region and is subject to regulatory approval.
		</div>
	</footer>

</div>

