<template>
    <div id="app" class="font-sans bg-white text-gray-900 overflow-x-hidden">
        <AppNavigation />

        <!-- Hero Section -->
        <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-16 lg:pt-0">
            <!-- Sophisticated Background Effects -->
            <div class="absolute inset-0 bg-gradient-to-br from-gray-50 via-white to-slate-50"></div>

            <!-- Floating geometric elements -->
            <div class="absolute top-20 left-1/6 w-64 h-64 bg-gradient-to-br from-teal-100/40 to-blue-100/40 rounded-full blur-3xl animate-pulse opacity-60"></div>
            <div class="absolute bottom-32 right-1/6 w-80 h-80 bg-gradient-to-br from-purple-100/30 to-teal-100/30 rounded-full blur-3xl animate-pulse delay-2000 opacity-50"></div>
            <div class="absolute top-1/3 right-1/4 w-32 h-32 bg-gradient-to-br from-gray-200/50 to-slate-200/50 rounded-2xl blur-2xl animate-float opacity-40"></div>

            <!-- Grid Pattern Overlay -->
            <div class="absolute inset-0 opacity-[0.02]" style="background-image: radial-gradient(circle at 1px 1px, rgba(0, 0, 0, 0.15) 1px, transparent 0); background-size: 20px 20px"></div>

            <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <div class="flex flex-col lg:flex-row items-center gap-12 max-w-6xl mx-auto">
                    <div class="flex-1 text-left">
                        <h1 class="text-3xl sm:text-4xl lg:text-5xl font-light text-gray-900 mb-6 leading-tight tracking-tight">
                            Let AI handle the busywork —
                            <span class="relative font-normal">
                                <span class="mr-1">inside</span>
                                <span class="relative inline-block min-w-[140px] sm:min-w-[180px] lg:min-w-[220px]">
                                    <Transition name="channel-slide" mode="out-in">
                                        <span :key="currentChannelIndex" class="block bg-gradient-to-r from-teal-600 via-blue-600 to-purple-600 bg-clip-text text-transparent">
                                            {{ channels[currentChannelIndex] }}
                                        </span>
                                    </Transition>
                                </span>
                                <div class="absolute -inset-1 bg-gradient-to-r from-teal-500/10 via-blue-500/10 to-purple-500/10 blur-lg -z-10"></div>
                            </span>
                        </h1>

                        <p class="text-lg text-gray-600 mb-8 leading-relaxed">Stop wasting 20+ hours per week on manual coordination. <span class="font-medium text-gray-900">AI employees complete entire business processes</span> through conversation - with human oversight when you need it.</p>

                        <!-- Simple Setup Process Integration -->
                        <div class="mb-8 p-6 bg-gradient-to-r from-teal-50 to-blue-50 rounded-2xl border border-teal-200">
                            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 text-left">
                                <div class="space-y-3">
                                    <h4 class="font-medium text-gray-900 text-sm">1. Tell Us What You Need</h4>
                                    <p class="text-sm text-gray-600">"Help with car rentals - check availability, handle payments, but call me for expensive bookings"</p>
                                </div>
                                <div class="space-y-3">
                                    <h4 class="font-medium text-gray-900 text-sm">2. We Create Your AI Employee</h4>
                                    <p class="text-sm text-gray-600">Ready in minutes, works across WhatsApp, LINE, Email, Telegram</p>
                                </div>
                            </div>
                        </div>

                        <div class="flex flex-col sm:flex-row gap-4 mb-8">
                            <button class="group bg-teal-100 text-teal-600 font-medium px-8 py-4 rounded-xl text-base hover:bg-teal-200 hover:text-teal-700 transition-all duration-300 shadow-md hover:shadow-lg hover:scale-105 relative overflow-hidden">
                                <div class="absolute inset-0 bg-gradient-to-r from-teal-500/10 to-blue-500/10 translate-x-[-100%] group-hover:translate-x-0 transition-transform duration-500"></div>
                                <div class="relative flex items-center gap-3 justify-center">
                                    <Rocket class="w-5 h-5" />
                                    Start Free Trial
                                </div>
                            </button>
                            <button class="group border-2 border-gray-200 bg-white text-gray-700 px-8 py-4 rounded-xl font-medium text-base hover:border-gray-300 hover:bg-gray-50 transition-all duration-300 hover:shadow-md relative overflow-hidden">
                                <div class="absolute inset-0 bg-gradient-to-r from-gray-100/50 to-slate-100/50 translate-x-[-100%] group-hover:translate-x-0 transition-transform duration-500"></div>
                                <div class="relative flex items-center gap-3 justify-center">
                                    <Play class="w-5 h-5" />
                                    Watch Demo
                                </div>
                            </button>
                        </div>
                    </div>

                    <div class="flex-1">
                        <!-- Workflow Builder Preview -->
                        <div class="relative">
                            <div class="absolute inset-0 bg-white/70 backdrop-blur-xl rounded-3xl border border-white/20 shadow-2xl"></div>

                            <div class="relative bg-white/90 backdrop-blur-sm rounded-2xl shadow-xl border border-gray-200/50 overflow-hidden">
                                <!-- Header -->
                                <div class="bg-gradient-to-r from-gray-900 to-gray-800 text-white p-4 flex items-center justify-between">
                                    <div class="flex items-center gap-3">
                                        <div class="flex gap-2">
                                            <div class="w-3 h-3 bg-red-400 rounded-full"></div>
                                            <div class="w-3 h-3 bg-yellow-400 rounded-full"></div>
                                            <div class="w-3 h-3 bg-green-400 rounded-full"></div>
                                        </div>
                                        <span class="font-medium">AI Employee Builder</span>
                                    </div>
                                    <div class="flex items-center gap-2">
                                        <div class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                                        <span class="text-sm text-gray-300">Live</span>
                                    </div>
                                </div>

                                <!-- Workflow Builder Content -->
                                <div class="p-6 space-y-4">
                                    <div class="text-sm text-gray-600 mb-4">Describe your workflow in plain language:</div>

                                    <div class="bg-gray-50 rounded-lg p-4 text-sm text-gray-800 border-l-4 border-teal-400">"Create an AI employee for consultation booking. Ask for preferred dates, confirm payment, send reminders, but require human approval for discounts over 20%"</div>

                                    <div class="flex items-center gap-2 py-2">
                                        <div class="w-6 h-6 bg-teal-500 rounded-full flex items-center justify-center">
                                            <Zap class="w-3 h-3 text-white" />
                                        </div>
                                        <span class="text-sm text-gray-600">AI building workflow...</span>
                                    </div>

                                    <!-- Generated Steps -->
                                    <div class="space-y-2">
                                        <div class="flex items-center gap-3 p-2 bg-green-50 rounded-lg text-sm">
                                            <CheckCircle class="w-4 h-4 text-green-500" />
                                            <span>Customer inquiry → Collect requirements</span>
                                        </div>
                                        <div class="flex items-center gap-3 p-2 bg-green-50 rounded-lg text-sm">
                                            <CheckCircle class="w-4 h-4 text-green-500" />
                                            <span>Check availability → Present options</span>
                                        </div>
                                        <div class="flex items-center gap-3 p-2 bg-yellow-50 rounded-lg text-sm">
                                            <AlertCircle class="w-4 h-4 text-yellow-500" />
                                            <span>Discount >20% → Human approval</span>
                                        </div>
                                        <div class="flex items-center gap-3 p-2 bg-green-50 rounded-lg text-sm">
                                            <CheckCircle class="w-4 h-4 text-green-500" />
                                            <span>Payment → Confirmation → Reminders</span>
                                        </div>
                                    </div>

                                    <div class="bg-teal-50 rounded-lg p-3 border border-teal-200">
                                        <div class="text-sm font-medium text-teal-800 mb-1">Ready to deploy</div>
                                        <div class="text-xs text-teal-600">Works across WhatsApp, LINE, WeChat, Email</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Trust Indicators -->
                <div class="text-center mt-12">
                    <p class="text-sm text-gray-500 mb-4">Trusted by growing businesses across Southeast Asia</p>
                    <div class="flex flex-wrap justify-center items-center gap-6 opacity-60">
                        <div class="text-gray-400 font-medium">TechStart</div>
                        <div class="text-gray-400 font-medium">InnovateCorp</div>
                        <div class="text-gray-400 font-medium">HealthPlus</div>
                        <div class="text-gray-400 font-medium">EventPro</div>
                        <div class="text-gray-400 font-medium">CarRental+</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Problem Statement Section -->
        <section class="py-20 bg-gradient-to-b from-gray-50 to-white relative">
            <div class="relative max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <div class="inline-flex items-center gap-2 bg-red-50 border border-red-200 rounded-full px-4 py-2 mb-6">
                        <AlertTriangle class="w-4 h-4 text-red-500" />
                        <span class="text-red-700 font-medium text-sm">The Hidden Cost Crisis</span>
                    </div>

                    <h2 class="text-2xl sm:text-3xl font-normal text-gray-900 mb-6 leading-tight">Indonesian Businesses Are <span class="text-red-600 font-medium">Drowning in Manual Work</span></h2>

                    <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed"><strong class="text-gray-900">87% of Indonesian businesses</strong> waste 15-20 hours per week on processes that should take minutes, losing an average of <strong class="text-red-600">Rp 50 million per month</strong></p>
                </div>

                <!-- Problem Showcase Grid -->
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-16">
                    <!-- Event Management Problem -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-red-500/10 to-orange-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white/80 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 hover:shadow-2xl transition-all duration-500 hover:scale-105">
                            <div class="w-12 h-12 bg-gradient-to-br from-red-500 to-orange-500 rounded-xl flex items-center justify-center mb-4 shadow-lg">
                                <Calendar class="w-6 h-6 text-white" />
                            </div>
                            <h3 class="text-lg font-medium text-gray-900 mb-3">Event Organizers</h3>
                            <div class="space-y-3 mb-6">
                                <div class="flex justify-between items-center p-3 bg-red-50 rounded-lg border border-red-100">
                                    <span class="text-sm text-gray-600">Before AI Employee</span>
                                    <span class="font-bold text-red-600 text-lg">2-3 days</span>
                                </div>
                                <div class="flex justify-between items-center p-3 bg-green-50 rounded-lg border border-green-100">
                                    <span class="text-sm text-gray-600">With AI Employee</span>
                                    <span class="font-bold text-green-600 text-lg">15 minutes</span>
                                </div>
                            </div>
                            <p class="text-gray-600 leading-relaxed">Booth registration coordination that should be automated, not manual.</p>
                        </div>
                    </div>

                    <!-- Car Rental Problem -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-blue-500/10 to-cyan-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white/80 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 hover:shadow-2xl transition-all duration-500 hover:scale-105">
                            <div class="w-12 h-12 bg-gradient-to-br from-blue-500 to-cyan-500 rounded-xl flex items-center justify-center mb-4 shadow-lg">
                                <Car class="w-6 h-6 text-white" />
                            </div>
                            <h3 class="text-lg font-medium text-gray-900 mb-3">Car Rental Services</h3>
                            <div class="space-y-3 mb-6">
                                <div class="flex justify-between items-center p-3 bg-red-50 rounded-lg border border-red-100">
                                    <span class="text-sm text-gray-600">Customer Loss Rate</span>
                                    <span class="font-bold text-red-600 text-lg">40%</span>
                                </div>
                                <div class="flex justify-between items-center p-3 bg-orange-50 rounded-lg border border-orange-100">
                                    <span class="text-sm text-gray-600">Response Time</span>
                                    <span class="font-bold text-orange-600 text-lg">Too Slow</span>
                                </div>
                            </div>
                            <p class="text-gray-600 leading-relaxed">Losing customers due to complex booking processes and slow responses.</p>
                        </div>
                    </div>

                    <!-- Healthcare Problem -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-emerald-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white/80 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 hover:shadow-2xl transition-all duration-500 hover:scale-105">
                            <div class="w-12 h-12 bg-gradient-to-br from-green-500 to-emerald-500 rounded-xl flex items-center justify-center mb-4 shadow-lg">
                                <Heart class="w-6 h-6 text-white" />
                            </div>
                            <h3 class="text-lg font-medium text-gray-900 mb-3">Healthcare Clinics</h3>
                            <div class="space-y-3 mb-6">
                                <div class="flex justify-between items-center p-3 bg-red-50 rounded-lg border border-red-100">
                                    <span class="text-sm text-gray-600">Booking Method</span>
                                    <span class="font-bold text-red-600 text-lg">Physical Visit</span>
                                </div>
                                <div class="flex justify-between items-center p-3 bg-green-50 rounded-lg border border-green-100">
                                    <span class="text-sm text-gray-600">Should Be</span>
                                    <span class="font-bold text-green-600 text-lg">Digital</span>
                                </div>
                            </div>
                            <p class="text-gray-600 leading-relaxed">Patients still need to visit physically just for appointments and records.</p>
                        </div>
                    </div>
                </div>

                <!-- Cost Impact Visualization -->
                <div class="bg-gradient-to-r from-red-50 via-orange-50 to-yellow-50 rounded-2xl p-6 border border-red-100">
                    <div class="text-center">
                        <h3 class="text-xl font-medium text-gray-900 mb-6">The Real Cost of Manual Processes</h3>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                            <div class="text-center">
                                <div class="text-3xl font-bold text-red-600 mb-2">20+</div>
                                <div class="text-gray-700 text-sm">Hours wasted per week</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-orange-600 mb-2">Rp 50M</div>
                                <div class="text-gray-700 text-sm">Monthly losses</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-yellow-600 mb-2">87%</div>
                                <div class="text-gray-700 text-sm">Of businesses affected</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Meet Your AI Employees -->
        <section class="mt-16 container mx-auto">
            <div class="text-center mb-12">
                <div class="inline-flex items-center gap-2 bg-gradient-to-r from-purple-50 to-pink-50 border border-purple-200 rounded-full px-4 py-2 mb-6">
                    <Users class="w-4 h-4 text-purple-600" />
                    <span class="text-purple-700 font-medium text-sm">Meet Your New Team</span>
                </div>
                <h3 class="text-2xl sm:text-3xl font-normal text-gray-900 mb-6 leading-tight">Hire Your <span class="bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent font-medium">AI Employees</span> in Minutes</h3>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed">Each AI employee is designed for specific roles and can handle complex tasks while knowing when to involve humans.</p>
            </div>

            <!-- AI Employee Cards -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Alfred - Executive Assistant -->
                <div class="group relative">
                    <div class="absolute inset-0 bg-gradient-to-br from-purple-500/10 to-blue-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                    <div class="relative bg-white border border-gray-200/50 rounded-3xl p-6 hover:shadow-2xl transition-all duration-500">
                        <div class="text-center mb-6">
                            <div class="w-20 h-20 bg-gradient-to-br from-gray-200 to-gray-300 rounded-full mx-auto mb-4 flex items-center justify-center relative overflow-hidden">
                                <!-- Simple AI avatar representation -->
                                <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center">
                                    <div class="flex gap-1">
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                    </div>
                                </div>
                                <!-- Purple bow tie -->
                                <div class="absolute bottom-2 w-6 h-3 bg-purple-500 rounded-sm transform rotate-12"></div>
                            </div>
                            <h4 class="text-lg font-medium text-purple-600 mb-1">Alfred</h4>
                            <p class="text-sm text-gray-600">AI Executive Assistant</p>
                        </div>

                        <div class="mb-4">
                            <h5 class="font-medium text-gray-900 mb-3 text-sm">What I can do:</h5>
                            <div class="grid grid-cols-1 gap-2">
                                <div class="bg-purple-50 border border-purple-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-purple-700 font-medium">Schedule Calendar</span>
                                </div>
                                <div class="bg-purple-50 border border-purple-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-purple-700 font-medium">Prioritize Tasks</span>
                                </div>
                                <div class="bg-purple-50 border border-purple-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-purple-700 font-medium">Reply to Emails</span>
                                </div>
                                <div class="bg-purple-50 border border-purple-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-purple-700 font-medium">Takes Notes</span>
                                </div>
                            </div>
                        </div>
                        <p class="text-xs text-gray-500 italic">and hundreds more skills...</p>
                    </div>
                </div>

                <!-- Chip - Sales Representative -->
                <div class="group relative">
                    <div class="absolute inset-0 bg-gradient-to-br from-blue-500/10 to-cyan-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                    <div class="relative bg-white border border-gray-200/50 rounded-3xl p-6 hover:shadow-2xl transition-all duration-500">
                        <div class="text-center mb-6">
                            <div class="w-20 h-20 bg-gradient-to-br from-gray-200 to-gray-300 rounded-full mx-auto mb-4 flex items-center justify-center relative overflow-hidden">
                                <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center">
                                    <div class="flex gap-1">
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                    </div>
                                </div>
                                <!-- Red tie -->
                                <div class="absolute bottom-2 w-2 h-8 bg-red-500 rounded-sm"></div>
                                <!-- Thumbs up -->
                                <div class="absolute -right-1 bottom-6 w-4 h-4 bg-white rounded-full border-2 border-gray-300"></div>
                            </div>
                            <h4 class="text-lg font-medium text-blue-600 mb-1">Chip</h4>
                            <p class="text-sm text-gray-600">AI Sales Representative</p>
                        </div>

                        <div class="mb-4">
                            <h5 class="font-medium text-gray-900 mb-3 text-sm">What I can do:</h5>
                            <div class="grid grid-cols-1 gap-2">
                                <div class="bg-blue-50 border border-blue-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-blue-700 font-medium">Update CRM</span>
                                </div>
                                <div class="bg-blue-50 border border-blue-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-blue-700 font-medium">Chase Opportunities</span>
                                </div>
                                <div class="bg-blue-50 border border-blue-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-blue-700 font-medium">Find Leads</span>
                                </div>
                                <div class="bg-blue-50 border border-blue-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-blue-700 font-medium">Personalized Outreach</span>
                                </div>
                            </div>
                        </div>
                        <p class="text-xs text-gray-500 italic">and hundreds more skills...</p>
                    </div>
                </div>

                <!-- Clide - Customer Support -->
                <div class="group relative">
                    <div class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-emerald-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                    <div class="relative bg-white border border-gray-200/50 rounded-3xl p-6 hover:shadow-2xl transition-all duration-500">
                        <div class="text-center mb-6">
                            <div class="w-20 h-20 bg-gradient-to-br from-gray-200 to-gray-300 rounded-full mx-auto mb-4 flex items-center justify-center relative overflow-hidden">
                                <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center">
                                    <div class="flex gap-1">
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                    </div>
                                </div>
                                <!-- Headset -->
                                <div class="absolute top-1 w-12 h-2 bg-black rounded-full"></div>
                                <div class="absolute bottom-2 right-2 w-3 h-2 bg-black rounded-full"></div>
                            </div>
                            <h4 class="text-lg font-medium text-green-600 mb-1">Clide</h4>
                            <p class="text-sm text-gray-600">AI Customer Support</p>
                        </div>

                        <div class="mb-4">
                            <h5 class="font-medium text-gray-900 mb-3 text-sm">What I can do:</h5>
                            <div class="grid grid-cols-1 gap-2">
                                <div class="bg-green-50 border border-green-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-green-700 font-medium">Respond to Tickets</span>
                                </div>
                                <div class="bg-green-50 border border-green-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-green-700 font-medium">Escalate Issues</span>
                                </div>
                                <div class="bg-green-50 border border-green-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-green-700 font-medium">Take Actions</span>
                                </div>
                                <div class="bg-green-50 border border-green-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-green-700 font-medium">Solve Problems</span>
                                </div>
                            </div>
                        </div>
                        <p class="text-xs text-gray-500 italic">and hundreds more skills...</p>
                    </div>
                </div>

                <!-- Suki - Marketing Associate -->
                <div class="group relative">
                    <div class="absolute inset-0 bg-gradient-to-br from-yellow-500/10 to-orange-500/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                    <div class="relative bg-white border border-gray-200/50 rounded-3xl p-6 hover:shadow-2xl transition-all duration-500">
                        <div class="text-center mb-6">
                            <div class="w-20 h-20 bg-gradient-to-br from-gray-200 to-gray-300 rounded-full mx-auto mb-4 flex items-center justify-center relative overflow-hidden">
                                <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center">
                                    <div class="flex gap-1">
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                        <div class="w-2 h-2 bg-gray-800 rounded-full"></div>
                                    </div>
                                </div>
                                <!-- Blonde hair -->
                                <div class="absolute -top-1 left-1 w-6 h-6 bg-yellow-400 rounded-full"></div>
                                <div class="absolute -top-1 right-1 w-6 h-6 bg-yellow-400 rounded-full"></div>
                            </div>
                            <h4 class="text-lg font-medium text-yellow-600 mb-1">Suki</h4>
                            <p class="text-sm text-gray-600">AI Marketing Associate</p>
                        </div>

                        <div class="mb-4">
                            <h5 class="font-medium text-gray-900 mb-3 text-sm">What I can do:</h5>
                            <div class="grid grid-cols-1 gap-2">
                                <div class="bg-yellow-50 border border-yellow-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-yellow-700 font-medium">Write Blog Posts</span>
                                </div>
                                <div class="bg-yellow-50 border border-yellow-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-yellow-700 font-medium">Run SEO</span>
                                </div>
                                <div class="bg-yellow-50 border border-yellow-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-yellow-700 font-medium">Manage Social Media</span>
                                </div>
                                <div class="bg-yellow-50 border border-yellow-200 rounded-lg p-2 text-center">
                                    <span class="text-xs text-yellow-700 font-medium">Write with Brand Voice</span>
                                </div>
                            </div>
                        </div>
                        <p class="text-xs text-gray-500 italic">and hundreds more skills...</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Multi-Channel Platform Section -->
        <section class="py-20 bg-gradient-to-b from-gray-50 to-white relative">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <div class="inline-flex items-center gap-2 bg-gradient-to-r from-blue-50 to-purple-50 border border-blue-200 rounded-full px-4 py-2 mb-6">
                        <Globe class="w-4 h-4 text-blue-600" />
                        <span class="text-blue-700 font-medium text-sm">Multi-Channel AI Platform</span>
                    </div>

                    <h2 class="text-2xl sm:text-3xl font-normal text-gray-900 mb-6 leading-tight">One AI Workforce, <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent font-medium">Every Channel</span></h2>

                    <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed">Your AI employees work seamlessly across <strong class="text-gray-900">WhatsApp, LINE, WeChat, Telegram</strong>, and more - adapting to your customers' preferred communication channels.</p>
                </div>

                <!-- Channel Showcase -->
                <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6 mb-16">
                    <!-- WhatsApp -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-green-500/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <FontAwesomeIcon :icon="['fab', 'whatsapp']" class="text-green-500 mx-auto mb-3" style="font-size: 3rem" />
                            <div class="font-semibold text-gray-900 text-sm">WhatsApp</div>
                            <div class="text-xs text-gray-600 mt-1">Indonesia, Singapore</div>
                        </div>
                    </div>

                    <!-- LINE -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-green-400/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <FontAwesomeIcon :icon="['fab', 'line']" class="text-green-400 mx-auto mb-3" style="font-size: 3rem" />
                            <div class="font-semibold text-gray-900 text-sm">LINE</div>
                            <div class="text-xs text-gray-600 mt-1">Japan, Thailand, Taiwan</div>
                        </div>
                    </div>

                    <!-- WeChat -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-green-600/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <FontAwesomeIcon :icon="['fab', 'weixin']" class="text-green-600 mx-auto mb-3" style="font-size: 3rem" />
                            <div class="font-semibold text-gray-900 text-sm">WeChat</div>
                            <div class="text-xs text-gray-600 mt-1">China</div>
                        </div>
                    </div>

                    <!-- Telegram -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-blue-500/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <FontAwesomeIcon :icon="['fab', 'telegram']" class="text-blue-500 mx-auto mb-3" style="font-size: 3rem" />
                            <div class="font-semibold text-gray-900 text-sm">Telegram</div>
                            <div class="text-xs text-gray-600 mt-1">Malaysia, Philippines</div>
                        </div>
                    </div>

                    <!-- Email -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-purple-500/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <Mail class="w-12 h-12 text-purple-500 mx-auto mb-3" />
                            <div class="font-semibold text-gray-900 text-sm">Email</div>
                            <div class="text-xs text-gray-600 mt-1">Global</div>
                        </div>
                    </div>

                    <!-- SMS -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-orange-500/10 rounded-2xl blur-lg group-hover:blur-xl transition-all duration-300"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-2xl p-6 hover:shadow-lg transition-all duration-300 hover:scale-105 text-center">
                            <Phone class="w-12 h-12 text-orange-500 mx-auto mb-3" />
                            <div class="font-semibold text-gray-900 text-sm">SMS</div>
                            <div class="text-xs text-gray-600 mt-1">Universal</div>
                        </div>
                    </div>
                </div>

                <!-- Platform Benefits -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Benefits List -->
                    <div class="space-y-8">
                        <div class="flex gap-4 group">
                            <div class="w-12 h-12 bg-gradient-to-br from-teal-500 to-teal-600 rounded-xl flex items-center justify-center flex-shrink-0 shadow-lg group-hover:scale-110 transition-transform duration-300">
                                <Settings class="w-6 h-6 text-white" />
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900 mb-2">One Workflow, All Channels</h3>
                                <p class="text-gray-600 leading-relaxed">Define your business process once, deploy across all messaging platforms with channel-specific optimizations.</p>
                            </div>
                        </div>

                        <div class="flex gap-4 group">
                            <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-purple-600 rounded-xl flex items-center justify-center flex-shrink-0 shadow-lg group-hover:scale-110 transition-transform duration-300">
                                <Shield class="w-6 h-6 text-white" />
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900 mb-2">Compliance & Security</h3>
                                <p class="text-gray-600 leading-relaxed">Built-in compliance for PDPA, local regulations, and enterprise security requirements across all markets.</p>
                            </div>
                        </div>

                        <div class="flex gap-4 group">
                            <div class="w-12 h-12 bg-gradient-to-br from-blue-500 to-blue-600 rounded-xl flex items-center justify-center flex-shrink-0 shadow-lg group-hover:scale-110 transition-transform duration-300">
                                <Globe class="w-6 h-6 text-white" />
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900 mb-2">Multi-Language Support</h3>
                                <p class="text-gray-600 leading-relaxed">Built-in support for Indonesian, English, and local languages across 8 Asian markets.</p>
                            </div>
                        </div>

                        <div class="flex gap-4 group">
                            <div class="w-12 h-12 bg-gradient-to-br from-green-500 to-green-600 rounded-xl flex items-center justify-center flex-shrink-0 shadow-lg group-hover:scale-110 transition-transform duration-300">
                                <TrendingUp class="w-6 h-6 text-white" />
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900 mb-2">Scale Without Limits</h3>
                                <p class="text-gray-600 leading-relaxed">Handle thousands of conversations simultaneously across channels while maintaining human oversight quality.</p>
                            </div>
                        </div>
                    </div>

                    <!-- Platform Visualization -->
                    <div class="relative">
                        <div class="absolute inset-0 bg-gradient-to-r from-blue-500/10 via-purple-500/10 to-teal-500/10 rounded-3xl blur-2xl"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 shadow-2xl">
                            <div class="text-center mb-6">
                                <h3 class="text-2xl font-bold text-gray-900 mb-2">Multi-Channel Dashboard</h3>
                                <p class="text-gray-600">Unified control for all your AI employees</p>
                            </div>

                            <!-- Mock Channel Stats -->
                            <div class="grid grid-cols-2 gap-4 mb-6">
                                <div class="bg-gradient-to-br from-green-50 to-emerald-50 p-4 rounded-xl border border-green-100">
                                    <div class="flex items-center gap-2 mb-2">
                                        <FontAwesomeIcon :icon="['fab', 'whatsapp']" class="text-green-500" style="font-size: 1rem" />
                                        <span class="text-sm font-medium text-gray-700">WhatsApp</span>
                                    </div>
                                    <div class="text-2xl font-bold text-green-700">1,248</div>
                                    <div class="text-xs text-gray-600">Active conversations</div>
                                </div>
                                <div class="bg-gradient-to-br from-blue-50 to-cyan-50 p-4 rounded-xl border border-blue-100">
                                    <div class="flex items-center gap-2 mb-2">
                                        <FontAwesomeIcon :icon="['fab', 'line']" class="text-blue-500" style="font-size: 1rem" />
                                        <span class="text-sm font-medium text-gray-700">LINE</span>
                                    </div>
                                    <div class="text-2xl font-bold text-blue-700">892</div>
                                    <div class="text-xs text-gray-600">Active conversations</div>
                                </div>
                                <div class="bg-gradient-to-br from-purple-50 to-pink-50 p-4 rounded-xl border border-purple-100">
                                    <div class="flex items-center gap-2 mb-2">
                                        <Mail class="w-4 h-4 text-purple-500" />
                                        <span class="text-sm font-medium text-gray-700">Email</span>
                                    </div>
                                    <div class="text-2xl font-bold text-purple-700">543</div>
                                    <div class="text-xs text-gray-600">Active conversations</div>
                                </div>
                                <div class="bg-gradient-to-br from-orange-50 to-red-50 p-4 rounded-xl border border-orange-100">
                                    <div class="flex items-center gap-2 mb-2">
                                        <FontAwesomeIcon :icon="['fab', 'telegram']" class="text-orange-500" style="font-size: 1rem" />
                                        <span class="text-sm font-medium text-gray-700">Telegram</span>
                                    </div>
                                    <div class="text-2xl font-bold text-orange-700">367</div>
                                    <div class="text-xs text-gray-600">Active conversations</div>
                                </div>
                            </div>

                            <!-- Unified Success Rate -->
                            <div class="bg-gradient-to-r from-green-50 to-emerald-50 rounded-2xl p-4 border border-green-200">
                                <div class="text-center">
                                    <div class="text-3xl font-bold text-green-700 mb-1">97.8%</div>
                                    <div class="text-green-600 text-sm">Success rate across all channels</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Pricing Section -->
        <section class="py-20 bg-gradient-to-b from-white to-gray-50 relative">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <div class="inline-flex items-center gap-2 bg-gradient-to-r from-purple-50 to-pink-50 border border-purple-200 rounded-full px-4 py-2 mb-6">
                        <DollarSign class="w-4 h-4 text-purple-600" />
                        <span class="text-purple-700 font-medium text-sm">Enterprise-Grade Pricing</span>
                    </div>

                    <h2 class="text-2xl sm:text-3xl font-normal text-gray-900 mb-6 leading-tight">Choose Your <span class="bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent font-medium">AI Workforce</span></h2>

                    <p class="text-lg text-gray-600 max-w-3xl mx-auto leading-relaxed">Scale from simple automation to enterprise-grade AI employees. All plans include <strong class="text-gray-900">human oversight and multi-channel support</strong>.</p>
                </div>

                <!-- Pricing Grid -->
                <div class="grid grid-cols-1 lg:grid-cols-4 gap-8 mb-16">
                    <!-- Starter Tier -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-gray-500/5 to-slate-500/5 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 hover:shadow-2xl transition-all duration-500">
                            <div class="text-center mb-8">
                                <h3 class="text-2xl font-bold text-gray-900 mb-2">Starter</h3>
                                <div class="text-5xl font-bold text-gray-700 mb-2">$149</div>
                                <div class="text-gray-600">per month</div>
                            </div>

                            <ul class="space-y-4 mb-8">
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Up to 5-step workflows</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">1,000 conversations/month</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">2 human intervention points</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Multi-channel support</span>
                                </li>
                            </ul>

                            <button class="w-full bg-teal-100 text-teal-600 font-bold py-4 rounded-2xl hover:bg-teal-200 hover:text-teal-700 transition-all duration-300">Start Free Trial</button>

                            <div class="text-center mt-4">
                                <span class="text-xs text-gray-500">Perfect for small businesses</span>
                            </div>
                        </div>
                    </div>

                    <!-- Professional Tier (Popular) -->
                    <div class="group relative">
                        <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 z-10">
                            <span class="bg-gradient-to-r from-teal-500 to-blue-500 text-white px-4 py-2 rounded-full text-sm font-medium shadow-lg">Most Popular</span>
                        </div>
                        <div class="absolute inset-0 bg-gradient-to-br from-teal-500/20 to-blue-500/20 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white backdrop-blur-sm border-2 border-teal-200 rounded-3xl p-8 pt-12 shadow-2xl hover:shadow-3xl transition-all duration-500">
                            <div class="text-center mb-6">
                                <h3 class="text-lg font-medium text-gray-900 mb-3">Professional</h3>
                                <div class="text-3xl font-bold text-teal-700 mb-2">$399</div>
                                <div class="text-gray-600 text-sm">per month</div>
                            </div>

                            <ul class="space-y-4 mb-8">
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Up to 15-step workflows</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">5,000 conversations/month</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Unlimited human oversight</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Advanced integrations</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Team collaboration dashboard</span>
                                </li>
                            </ul>

                            <button class="w-full bg-gradient-to-r from-teal-500 to-blue-500 text-white font-bold py-4 rounded-2xl hover:from-teal-600 hover:to-blue-600 transition-all duration-300 shadow-lg hover:shadow-xl">Start Free Trial</button>

                            <div class="text-center mt-4">
                                <span class="text-xs text-gray-500">Ideal for growing companies</span>
                            </div>
                        </div>
                    </div>

                    <!-- Enterprise Tier -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-purple-500/5 to-pink-500/5 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-white/90 backdrop-blur-sm border border-gray-200/50 rounded-3xl p-8 hover:shadow-2xl transition-all duration-500">
                            <div class="text-center mb-8">
                                <h3 class="text-2xl font-bold text-gray-900 mb-2">Enterprise</h3>
                                <div class="text-5xl font-bold text-purple-700 mb-2">$999</div>
                                <div class="text-gray-600">per month</div>
                            </div>

                            <ul class="space-y-4 mb-8">
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Up to 50-step workflows</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">25,000 conversations/month</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Advanced analytics</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">White-label options</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-500 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-600">Dedicated success manager</span>
                                </li>
                            </ul>

                            <button class="w-full bg-teal-100 text-teal-600 font-bold py-4 rounded-2xl hover:bg-teal-200 hover:text-teal-700 transition-all duration-300">Contact Sales</button>

                            <div class="text-center mt-4">
                                <span class="text-xs text-gray-500">For large organizations</span>
                            </div>
                        </div>
                    </div>

                    <!-- Custom Tier -->
                    <div class="group relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-gray-900/10 to-black/10 rounded-3xl blur-xl group-hover:blur-2xl transition-all duration-500"></div>
                        <div class="relative bg-gradient-to-br from-gray-900 to-gray-800 text-white rounded-3xl p-8 hover:shadow-2xl transition-all duration-500">
                            <div class="text-center mb-8">
                                <h3 class="text-2xl font-bold mb-2">Custom</h3>
                                <div class="text-5xl font-bold mb-2">$2,500+</div>
                                <div class="text-gray-300">per month</div>
                            </div>

                            <ul class="space-y-4 mb-8">
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-400 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-300">Unlimited complexity</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-400 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-300">Custom AI training</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-400 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-300">Dedicated implementation</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-400 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-300">On-premise deployment</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <CheckCircle class="w-5 h-5 text-green-400 flex-shrink-0 mt-0.5" />
                                    <span class="text-sm text-gray-300">24/7 priority support</span>
                                </li>
                            </ul>

                            <button class="w-full bg-white text-gray-900 font-bold py-4 rounded-2xl hover:bg-gray-100 transition-all duration-300">Contact Enterprise</button>

                            <div class="text-center mt-4">
                                <span class="text-xs text-gray-400">Government & large enterprises</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ROI Calculator -->
                <div class="relative">
                    <div class="absolute inset-0 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-3xl blur-2xl"></div>
                    <div class="relative bg-gradient-to-r from-green-50 to-emerald-50 rounded-3xl p-12 border border-green-200">
                        <div class="text-center mb-8">
                            <h3 class="text-3xl font-bold text-gray-900 mb-4">Calculate Your Savings</h3>
                            <p class="text-gray-600 text-lg">See how much time and money you'll save with AI employees</p>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
                            <div class="bg-white p-8 rounded-2xl shadow-lg border border-green-200">
                                <div class="text-4xl font-bold text-red-600 mb-3">20+</div>
                                <div class="text-gray-700 font-medium">Hours saved per week</div>
                                <div class="text-sm text-gray-500 mt-2">Manual work eliminated</div>
                            </div>
                            <div class="bg-white p-8 rounded-2xl shadow-lg border border-green-200">
                                <div class="text-4xl font-bold text-green-600 mb-3">Rp 50M+</div>
                                <div class="text-gray-700 font-medium">Monthly savings</div>
                                <div class="text-sm text-gray-500 mt-2">From process automation</div>
                            </div>
                            <div class="bg-white p-8 rounded-2xl shadow-lg border border-green-200">
                                <div class="text-4xl font-bold text-blue-600 mb-3">85%</div>
                                <div class="text-gray-700 font-medium">Faster completion</div>
                                <div class="text-sm text-gray-500 mt-2">Compared to manual</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section class="py-20 bg-gradient-to-br from-gray-900 via-gray-800 to-black text-white relative overflow-hidden">
            <!-- Premium Background Effects -->
            <div class="absolute top-0 left-1/4 w-96 h-96 bg-gradient-to-r from-teal-500/20 to-blue-500/20 rounded-full blur-3xl animate-pulse"></div>
            <div class="absolute bottom-0 right-1/4 w-80 h-80 bg-gradient-to-r from-purple-500/20 to-pink-500/20 rounded-full blur-3xl animate-pulse delay-2000"></div>
            <div class="absolute inset-0 pattern-dots-white opacity-30"></div>

            <div class="relative z-10 max-w-4xl mx-auto text-center px-4 sm:px-6 lg:px-8">
                <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full px-4 py-2 mb-6">
                    <Zap class="w-4 h-4 text-yellow-400" />
                    <span class="text-white font-medium text-sm">Ready to Transform Your Business?</span>
                </div>

                <h2 class="text-3xl sm:text-4xl font-light mb-6 leading-tight">Stop Wasting Time on <span class="bg-gradient-to-r from-teal-400 via-blue-400 to-purple-400 bg-clip-text text-transparent font-normal">Manual Processes</span></h2>

                <p class="text-lg mb-10 text-gray-300 max-w-3xl mx-auto leading-relaxed">
                    Join Indonesian businesses already using AI employees to handle customer processes across multiple channels.
                    <strong class="text-white">Start your free trial today</strong> and see results in 24 hours.
                </p>

                <div class="flex flex-col sm:flex-row gap-4 justify-center mb-12">
                    <button class="group bg-white text-gray-900 font-medium px-8 py-4 rounded-xl text-base hover:bg-gray-100 transition-all duration-300 shadow-lg hover:shadow-xl hover:scale-105 relative overflow-hidden">
                        <div class="absolute inset-0 bg-gradient-to-r from-teal-500/10 to-blue-500/10 translate-x-[-100%] group-hover:translate-x-0 transition-transform duration-500"></div>
                        <div class="relative flex items-center gap-3 justify-center">
                            <Rocket class="w-5 h-5" />
                            Start Free Trial
                        </div>
                    </button>
                    <button class="group border-2 border-white/30 text-white px-8 py-4 rounded-xl font-medium text-base hover:border-white hover:bg-white/10 transition-all duration-300 backdrop-blur-sm relative overflow-hidden">
                        <div class="absolute inset-0 bg-white/5 translate-x-[-100%] group-hover:translate-x-0 transition-transform duration-500"></div>
                        <div class="relative flex items-center gap-3 justify-center">
                            <Phone class="w-5 h-5" />
                            Schedule Demo
                        </div>
                    </button>
                </div>

                <!-- Trust Indicators -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
                    <div class="flex items-center justify-center gap-2">
                        <CheckCircle class="w-5 h-5 text-green-400" />
                        <span class="text-gray-300 text-sm">No setup fees</span>
                    </div>
                    <div class="flex items-center justify-center gap-2">
                        <CheckCircle class="w-5 h-5 text-green-400" />
                        <span class="text-gray-300 text-sm">14-day free trial</span>
                    </div>
                    <div class="flex items-center justify-center gap-2">
                        <CheckCircle class="w-5 h-5 text-green-400" />
                        <span class="text-gray-300 text-sm">Cancel anytime</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="bg-gray-900 text-white py-16 relative">
            <div class="absolute inset-0 bg-gradient-to-b from-gray-800 to-gray-900"></div>
            <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-12">
                    <div class="flex items-center justify-center space-x-3 mb-6">
                        <div class="w-12 h-12 bg-gradient-to-br from-teal-400 to-blue-500 rounded-2xl flex items-center justify-center shadow-lg">
                            <MessageSquare class="w-7 h-7 text-white font-bold" />
                        </div>
                        <span class="text-3xl font-bold">Akksi</span>
                    </div>
                    <p class="text-gray-400 max-w-3xl mx-auto text-lg leading-relaxed">Transforming Southeast Asian businesses through AI employees that work 24/7 across multiple channels, with human oversight when you need it most.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                    <div>
                        <h4 class="font-semibold mb-6 text-lg">Product</h4>
                        <ul class="space-y-3 text-gray-400">
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Features</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Pricing</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Multi-Channel Support</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Integrations</a></li>
                        </ul>
                    </div>

                    <div>
                        <h4 class="font-semibold mb-6 text-lg">Solutions</h4>
                        <ul class="space-y-3 text-gray-400">
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Event Management</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Healthcare</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Financial Services</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">E-commerce</a></li>
                        </ul>
                    </div>

                    <div>
                        <h4 class="font-semibold mb-6 text-lg">Resources</h4>
                        <ul class="space-y-3 text-gray-400">
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Documentation</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">API Reference</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Case Studies</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Blog</a></li>
                        </ul>
                    </div>

                    <div>
                        <h4 class="font-semibold mb-6 text-lg">Company</h4>
                        <ul class="space-y-3 text-gray-400">
                            <li><a href="#" class="hover:text-white transition-colors duration-200">About</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Careers</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Contact</a></li>
                            <li><a href="#" class="hover:text-white transition-colors duration-200">Privacy</a></li>
                        </ul>
                    </div>
                </div>

                <div class="border-t border-gray-800 pt-8 text-center text-gray-400">
                    <p>&copy; {{ new Date().getFullYear() }} Akksi. All rights reserved.</p>
                </div>
            </div>
        </footer>
    </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import AppNavigation from "./components/AppNavigation.vue";
import { MessageSquare, Bot, Clock, Users, ArrowRightLeft, CheckCircle, AlertTriangle, Car, Heart, AlertCircle, Zap, Calendar, Building2, ShoppingBag, Truck, Briefcase, MessageSquareText, Settings, Rocket, ArrowRight, Globe, Shield, Plug, BarChart3, FileText, Smartphone, Phone, Menu, X, MessageCircle, Mail, Send, User, Brain, Play, Sparkles, TrendingUp, DollarSign } from "lucide-vue-next";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faWhatsapp, faLine, faWeixin, faTelegram, faFacebook } from "@fortawesome/free-brands-svg-icons";

// Add icons to the library
library.add(faWhatsapp, faLine, faWeixin, faTelegram, faFacebook);

// Register FontAwesome component globally
const components = {
    FontAwesomeIcon,
};

onMounted(() => {
    // Smooth scroll for navigation links
    document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
        anchor.addEventListener("click", function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute("href"));
            if (target) {
                target.scrollIntoView({
                    behavior: "smooth",
                    block: "start",
                });
            }
        });
    });

    // Add sophisticated scroll animations
    const observerOptions = {
        threshold: 0.1,
        rootMargin: "0px 0px -50px 0px",
    };

    const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = "1";
                entry.target.style.transform = "translateY(0)";
            }
        });
    }, observerOptions);

    // Observe elements for scroll animations
    document.querySelectorAll(".group").forEach((el) => {
        el.style.opacity = "0";
        el.style.transform = "translateY(20px)";
        el.style.transition = "opacity 0.6s ease-out, transform 0.6s ease-out";
        observer.observe(el);
    });
});

// Hero rotating channels
const channels = ["WhatsApp", "LINE", "Telegram", "WeChat", "Email"];
const currentChannelIndex = ref(0);

setInterval(() => {
    currentChannelIndex.value = (currentChannelIndex.value + 1) % channels.length;
}, 2200); // Slightly slower for better readability
</script>

<style>
/* Import Lexend font */
@import url("https://fonts.googleapis.com/css2?family=Lexend:wght@100..900&display=swap");

.font-sans {
    font-family: "Lexend", ui-sans-serif, system-ui, sans-serif;
}

/* Enhanced animations */
@keyframes float {
    0%,
    100% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(-20px);
    }
}

.animate-float {
    animation: float 6s ease-in-out infinite;
}

@keyframes pulse {
    0%,
    100% {
        opacity: 1;
    }
    50% {
        opacity: 0.7;
    }
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Premium glass morphism effects */
.backdrop-blur-sm {
    backdrop-filter: blur(8px);
}

.backdrop-blur-xl {
    backdrop-filter: blur(40px);
}

/* Smooth scrolling */
html {
    scroll-behavior: smooth;
}

/* Custom gradient text */
.bg-clip-text {
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Enhanced shadow utilities */
.shadow-3xl {
    box-shadow: 0 35px 60px -12px rgba(0, 0, 0, 0.25);
}

/* Sophisticated hover effects */
.group:hover .group-hover\:scale-110 {
    transform: scale(1.1);
}

.group:hover .group-hover\:blur-xl {
    filter: blur(20px);
}

.group:hover .group-hover\:blur-2xl {
    filter: blur(40px);
}

/* Premium button effects */
button {
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

button:hover {
    transform: translateY(-2px);
}

/* Sophisticated scroll animations */
@media (prefers-reduced-motion: no-preference) {
    .group {
        animation: fadeInUp 0.6s ease-out forwards;
    }
}

/* Custom scrollbar */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
    background: linear-gradient(to bottom, #14b8a6, #0891b2);
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: linear-gradient(to bottom, #0d9488, #0e7490);
}

/* Pattern backgrounds */
.pattern-dots {
    background-image: radial-gradient(circle at 1px 1px, rgba(0, 0, 0, 0.15) 1px, transparent 0);
    background-size: 20px 20px;
}

.pattern-dots-white {
    background-image: radial-gradient(circle at 1px 1px, rgba(255, 255, 255, 0.15) 1px, transparent 0);
    background-size: 20px 20px;
}

/* Channel slide animation */
.channel-slide-enter-active,
.channel-slide-leave-active {
    transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
}

.channel-slide-enter-from {
    opacity: 0;
    transform: translateY(20px);
}

.channel-slide-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}

.channel-slide-enter-to,
.channel-slide-leave-from {
    opacity: 1;
    transform: translateY(0);
}
</style>
