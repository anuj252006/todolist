<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todoist Clone</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        :root {
            --color-primary: #db4c3f;
            --color-primary-hover: #c53b2e;
        }
        .bg-primary { background-color: var(--color-primary); }
        .text-primary { color: var(--color-primary); }
        .border-primary { border-color: var(--color-primary); }
        .hover\:bg-primary-hover:hover { background-color: var(--color-primary-hover); }
        body { font-family: 'Inter', sans-serif; }
        .sidebar-item:hover, .sidebar-item.active { background-color: #f0f0f0; }
        .task-item .actions { visibility: hidden; }
        .task-item:hover .actions { visibility: visible; }
        .modal-backdrop {
            background-color: rgba(0,0,0,0.5);
            transition: opacity 0.3s ease;
        }
        .hero-bg {
             background-color: #fff9f8;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }
        .listening {
            animation: pulse 1.5s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
    </style>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="bg-white text-gray-800">

    <!-- Landing Page -->
    <div id="landing-page">
        <header class="bg-white border-b border-gray-200 sticky top-0 z-20">
            <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
                <div class="flex items-center gap-2">
                     <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary"><path d="M4.5 12.5L8 16L19.5 4.5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>
                    <span class="font-bold text-xl">TaskMaster</span>
                </div>
                <div class="hidden md:flex items-center space-x-6">
                    <a href="#features" class="text-gray-600 hover:text-primary">Features</a>
                    <a href="#pricing" class="text-gray-600 hover:text-primary">Pricing</a>
                    <a href="#" class="text-gray-600 hover:text-primary">For Teams</a>
                </div>
                <div class="flex items-center space-x-4">
                    <button class="text-gray-600 hover:text-primary enter-app-btn">Log in</button>
                    <button class="bg-primary text-white px-4 py-2 rounded-lg hover:bg-primary-hover enter-app-btn">Start for free</button>
                </div>
            </nav>
        </header>

        <main>
            <!-- Hero Section -->
            <section class="hero-bg py-20">
                <div class="container mx-auto px-6 text-center">
                    <h1 class="text-4xl md:text-6xl font-bold text-gray-800 mb-4">Organize your work and life, finally.</h1>
                    <p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto mb-8">Become focused, organized, and calm with TaskMaster. The world’s #1 task manager and to-do list app.</p>
                    <button class="bg-primary text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-primary-hover enter-app-btn">Get Started - It's Free</button>
                </div>
            </section>
            
            <!-- App Preview Section -->
            <section class="py-16">
                 <div class="container mx-auto px-6">
                    <img src="https://placehold.co/1200x600/f0f0f0/333333?text=App+Interface+Screenshot" alt="App Preview" class="rounded-xl shadow-2xl mx-auto">
                 </div>
            </section>

            <!-- Features Section -->
            <section id="features" class="bg-white py-20">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-16">
                         <h2 class="text-3xl md:text-4xl font-bold">A task manager you can trust for life</h2>
                         <p class="text-gray-600 mt-2 max-w-2xl mx-auto">We’ve been building TaskMaster for 15 years. We are in this for the long haul.</p>
                    </div>
                    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-12">
                        <div class="feature flex items-start gap-4">
                            <i data-lucide="mic" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Add tasks via Voice</h3>
                                <p class="text-gray-600">Simply speak your mind. Our speech-to-text feature lets you add tasks on the go, without typing a word.</p>
                            </div>
                        </div>
                         <div class="feature flex items-start gap-4">
                            <i data-lucide="sparkles" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">AI Project Planner</h3>
                                <p class="text-gray-600">Describe a project, and our AI assistant will generate a complete task list for you in seconds.</p>
                            </div>
                        </div>
                        <div class="feature flex items-start gap-4">
                            <i data-lucide="list-checks" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Task Breakdown</h3>
                                <p class="text-gray-600">Feeling overwhelmed? Our AI can break down large, complex tasks into smaller, manageable steps.</p>
                            </div>
                        </div>
                        <div class="feature flex items-start gap-4">
                            <i data-lucide="calendar-days" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Due Dates & Reminders</h3>
                                <p class="text-gray-600">Never miss a deadline. Add due dates and get timely reminders for all your important tasks.</p>
                            </div>
                        </div>
                         <div class="feature flex items-start gap-4">
                            <i data-lucide="flag" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Prioritize Your Day</h3>
                                <p class="text-gray-600">Use priority levels to highlight your most important tasks and tackle them first.</p>
                            </div>
                        </div>
                         <div class="feature flex items-start gap-4">
                            <i data-lucide="pie-chart" class="w-10 h-10 text-primary shrink-0 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Visualize Your Progress</h3>
                                <p class="text-gray-600">See how much you’ve accomplished with personalized productivity trends and stats.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Pricing Section -->
            <section id="pricing" class="hero-bg py-20">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl md:text-4xl font-bold">Find the right plan for you</h2>
                    </div>
                    <div class="grid lg:grid-cols-3 gap-8 max-w-4xl mx-auto">
                        <!-- Free Plan -->
                        <div class="border rounded-lg p-8 bg-white shadow">
                            <h3 class="font-bold text-2xl mb-4">Free</h3>
                            <p class="text-gray-500 mb-6">For starters</p>
                            <p class="text-4xl font-bold mb-6">₹0</p>
                            <ul class="space-y-3 mb-8 text-left">
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>5 active projects</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>3 collaborators per project</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>5MB file uploads</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Basic AI features</li>
                            </ul>
                            <button class="w-full border border-primary text-primary py-2 rounded-lg hover:bg-primary hover:text-white transition-colors enter-app-btn">Get Started</button>
                        </div>
                        <!-- Pro Plan -->
                        <div class="border-2 border-primary rounded-lg p-8 bg-white shadow-xl relative">
                             <span class="absolute top-0 -translate-y-1/2 bg-primary text-white text-sm font-semibold px-3 py-1 rounded-full">Most Popular</span>
                            <h3 class="font-bold text-2xl mb-4">Pro</h3>
                            <p class="text-gray-500 mb-6">For power users</p>
                            <p class="text-4xl font-bold mb-1">₹249<span class="text-lg font-normal text-gray-500">/month</span></p>
                            <p class="text-sm text-gray-400 mb-6">billed annually</p>
                             <ul class="space-y-3 mb-8 text-left">
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>300 active projects</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>25 collaborators per project</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>100MB file uploads</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Unlimited AI features</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Reminders</li>
                            </ul>
                            <button class="w-full bg-primary text-white py-2 rounded-lg hover:bg-primary-hover enter-app-btn">Start Your Trial</button>
                        </div>
                        <!-- Business Plan -->
                        <div class="border rounded-lg p-8 bg-white shadow">
                            <h3 class="font-bold text-2xl mb-4">Business</h3>
                            <p class="text-gray-500 mb-6">For teams</p>
                            <p class="text-4xl font-bold mb-1">₹499<span class="text-lg font-normal text-gray-500">/user/month</span></p>
                             <p class="text-sm text-gray-400 mb-6">billed annually</p>
                             <ul class="space-y-3 mb-8 text-left">
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>500 active projects per member</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>50 people per project</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Team inbox</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Admin & security roles</li>
                                <li class="flex items-center gap-3"><i data-lucide="check" class="w-5 h-5 text-green-500"></i>Priority support</li>
                            </ul>
                             <button class="w-full border border-primary text-primary py-2 rounded-lg hover:bg-primary hover:text-white transition-colors enter-app-btn">Contact Sales</button>
                        </div>
                    </div>
                </div>
            </section>
        </main>
        
        <footer class="bg-gray-800 text-white py-12">
            <div class="container mx-auto px-6 text-center text-gray-400">
                <p>&copy; 2025 TaskMaster. A Todoist Clone by Gemini.</p>
            </div>
        </footer>
    </div>
    
    <!-- Login Page -->
    <div id="login-page" class="hidden min-h-screen flex items-center justify-center bg-gray-50">
        <div class="max-w-md w-full bg-white p-8 rounded-xl shadow-lg m-4">
            <div class="flex justify-center items-center gap-2 mb-6">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary"><path d="M4.5 12.5L8 16L19.5 4.5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>
                <span class="font-bold text-2xl">TaskMaster</span>
            </div>
            <h2 class="text-2xl font-bold text-center text-gray-800 mb-4">Log in</h2>
            
            <button id="google-login-btn" class="w-full flex items-center justify-center gap-3 py-2.5 border rounded-lg hover:bg-gray-50 mb-4">
                <svg class="w-5 h-5" viewBox="0 0 48 48"><path fill="#FFC107" d="M43.611 20.083H42V20H24v8h11.303c-1.649 4.657-6.08 8-11.303 8c-6.627 0-12-5.373-12-12s5.373-12 12-12c3.059 0 5.842 1.154 7.961 3.039l5.657-5.657C34.046 6.053 29.268 4 24 4C12.955 4 4 12.955 4 24s8.955 20 20 20s20-8.955 20-20c0-1.341-.138-2.65-.389-3.917z"></path><path fill="#FF3D00" d="m6.306 14.691l6.571 4.819C14.655 15.108 18.961 12 24 12c3.059 0 5.842 1.154 7.961 3.039l5.657-5.657C34.046 6.053 29.268 4 24 4C16.318 4 9.656 8.337 6.306 14.691z"></path><path fill="#4CAF50" d="M24 44c5.166 0 9.86-1.977 13.409-5.192l-6.19-5.238A11.91 11.91 0 0 1 24 36c-5.202 0-9.619-3.317-11.283-7.946l-6.522 5.025C9.505 39.556 16.227 44 24 44z"></path><path fill="#1976D2" d="M43.611 20.083H42V20H24v8h11.303c-.792 2.237-2.231 4.166-4.087 5.571l6.19 5.238C39.902 35.636 44 29.891 44 24c0-1.341-.138-2.65-.389-3.917z"></path></svg>
                <span class="font-medium text-gray-700">Continue with Google</span>
            </button>

            <div class="flex items-center my-6">
                <hr class="flex-grow border-gray-300">
                <span class="mx-4 text-gray-500 text-sm">OR</span>
                <hr class="flex-grow border-gray-300">
            </div>

            <form id="login-form">
                <div class="mb-4">
                    <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email</label>
                    <input type="email" id="email" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-1 focus:ring-primary" placeholder="Enter your email...">
                </div>
                 <div class="mb-6">
                    <label for="password" class="block text-sm font-medium text-gray-700 mb-1">Password</label>
                    <input type="password" id="password" class="w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-1 focus:ring-primary" placeholder="Enter your password...">
                </div>
                <button id="login-form-submit" type="submit" class="w-full bg-primary text-white py-2.5 rounded-lg hover:bg-primary-hover font-semibold">Log in</button>
            </form>
            <p class="text-center text-sm text-gray-600 mt-6">
                Don't have an account? <a href="#" class="font-medium text-primary hover:underline">Sign up</a>
            </p>
        </div>
    </div>


    <div id="app" class="flex h-screen w-screen hidden">
        <!-- Sidebar -->
        <nav class="w-64 bg-[#fafafa] p-4 border-r border-gray-200 flex flex-col shrink-0">
            <div class="flex items-center justify-between mb-6">
                <div class="flex items-center gap-2">
                    <img src="https://placehold.co/24x24/db4c3f/ffffff?text=T" class="rounded-full" alt="User Avatar">
                    <span class="font-semibold">My Workspace</span>
                </div>
            </div>

            <div class="space-y-1 flex-grow">
                <button id="add-task-quick" class="w-full flex items-center gap-2 px-3 py-2 text-sm font-medium rounded-md bg-primary text-white hover:bg-primary-hover transition-colors">
                    <i data-lucide="plus" class="w-4 h-4"></i>
                    Add task
                </button>
                <div class="sidebar-item flex items-center gap-2 px-3 py-2 text-sm font-medium rounded-md cursor-pointer" data-view-type="inbox" data-view-id="null">
                    <i data-lucide="inbox" class="w-4 h-4 text-blue-500"></i>
                    <span>Inbox</span>
                </div>
                <div class="sidebar-item flex items-center gap-2 px-3 py-2 text-sm font-medium rounded-md cursor-pointer" data-view-type="today" data-view-id="null">
                    <i data-lucide="calendar" class="w-4 h-4 text-green-500"></i>
                    <span>Today</span>
                </div>
                <div class="sidebar-item flex items-center gap-2 px-3 py-2 text-sm font-medium rounded-md cursor-pointer" data-view-type="upcoming" data-view-id="null">
                    <i data-lucide="calendar-days" class="w-4 h-4 text-purple-500"></i>
                    <span>Upcoming</span>
                </div>
            </div>

            <div class="flex-grow overflow-y-auto">
                <div class="flex items-center justify-between px-3 py-2 mt-4">
                    <h2 class="font-semibold text-sm">My Projects</h2>
                    <button id="add-project-btn" class="text-gray-400 hover:text-gray-700">
                        <i data-lucide="plus" class="w-4 h-4"></i>
                    </button>
                </div>
                <ul id="project-list" class="space-y-1 mt-2">
                    <!-- Projects will be rendered here -->
                </ul>
            </div>
            
            <div id="productivity-btn" class="mt-auto pt-4 border-t border-gray-200">
                 <div class="sidebar-item flex items-center gap-2 px-3 py-2 text-sm font-medium rounded-md cursor-pointer">
                    <i data-lucide="pie-chart" class="w-4 h-4 text-orange-500"></i>
                    <span>Productivity</span>
                </div>
            </div>
        </nav>

        <!-- Main Content -->
        <main class="flex-1 flex flex-col">
            <header class="flex items-center justify-between p-4 border-b border-gray-200 bg-white">
                <h1 id="view-title" class="text-xl font-bold">Inbox</h1>
                <div>
                    <!-- Header Actions can go here -->
                </div>
            </header>
            <div id="task-area" class="flex-1 p-8 overflow-y-auto">
                <div id="task-list" class="space-y-2">
                    <!-- Tasks will be rendered here -->
                </div>

                <button id="add-task-main" class="mt-4 flex items-center gap-2 text-gray-500 hover:text-primary transition-colors">
                    <i data-lucide="plus-circle" class="w-5 h-5 text-primary"></i>
                    <span class="text-sm font-medium">Add task</span>
                </button>
            </div>
        </main>
    </div>

    <!-- Add Task Modal -->
    <div id="task-modal" class="fixed inset-0 z-30 hidden items-center justify-center modal-backdrop">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-lg p-6">
            <form id="task-form">
                <input type="hidden" id="task-id">
                <input id="task-name" type="text" class="w-full text-lg p-2 border-none focus:ring-0" placeholder="Task name">
                <textarea id="task-description" class="w-full text-sm p-2 mt-1 border-none focus:ring-0 text-gray-600" placeholder="Description"></textarea>
                <div class="flex items-center gap-4 mt-4">
                    <input type="date" id="task-due-date" class="border rounded-md px-2 py-1 text-sm">
                    <select id="task-priority" class="border rounded-md px-2 py-1 text-sm">
                        <option value="4">Priority 4</option>
                        <option value="3">Priority 3</option>
                        <option value="2">Priority 2</option>
                        <option value="1">Priority 1</option>
                    </select>
                    <div class="relative flex-grow">
                         <button type="button" id="project-dropdown-btn" class="w-full text-left border rounded-md px-2 py-1 text-sm flex items-center justify-between">
                            <span id="selected-project-name">Inbox</span>
                            <i data-lucide="chevron-down" class="w-4 h-4"></i>
                        </button>
                        <div id="project-dropdown-list" class="hidden absolute bottom-full mb-1 w-full bg-white border rounded-md shadow-lg max-h-40 overflow-y-auto z-10">
                           <!-- Project options rendered here -->
                        </div>
                    </div>
                     <button type="button" id="voice-to-task-btn" class="p-2 border rounded-md text-gray-600 hover:bg-gray-100 shrink-0">
                        <i data-lucide="mic" class="w-5 h-5"></i>
                    </button>
                </div>
                <div class="flex justify-end items-center gap-2 mt-6">
                    <button type="button" id="cancel-task-btn" class="px-4 py-2 text-sm rounded-md bg-gray-100 hover:bg-gray-200">Cancel</button>
                    <button type="button" id="breakdown-task-btn" class="px-4 py-2 text-sm rounded-md bg-purple-600 text-white hover:bg-purple-700 flex items-center justify-center gap-2">
                         <span class="btn-text">✨ Breakdown</span>
                         <div class="loader hidden animate-spin rounded-full h-4 w-4 border-b-2 border-white"></div>
                    </button>
                    <button type="submit" id="submit-task-btn" class="px-4 py-2 text-sm rounded-md bg-primary text-white hover:bg-primary-hover">Add task</button>
                </div>
            </form>
        </div>
    </div>
    
    <!-- Add Project Modal -->
    <div id="project-modal" class="fixed inset-0 z-30 hidden items-center justify-center modal-backdrop">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md p-6">
            <h3 class="text-lg font-semibold mb-4">Add new project</h3>
            <form id="project-form">
                <input id="project-name" type="text" class="w-full border-gray-300 rounded-md p-2" placeholder="Project name" required>
                <div class="flex justify-end gap-2 mt-6">
                    <button type="button" id="cancel-project-btn" class="px-4 py-2 text-sm rounded-md bg-gray-100 hover:bg-gray-200">Cancel</button>
                    <button type="submit" class="px-4 py-2 text-sm rounded-md bg-primary text-white hover:bg-primary-hover">Add</button>
                    <button type="button" id="add-project-with-ai-btn" class="px-4 py-2 text-sm rounded-md bg-purple-600 text-white hover:bg-purple-700 flex items-center justify-center gap-2">
                        <span class="btn-text">✨ Generate Plan</span>
                        <div class="loader hidden animate-spin rounded-full h-4 w-4 border-b-2 border-white"></div>
                    </button>
                </div>
            </form>
        </div>
    </div>
    
    <!-- Productivity Modal -->
    <div id="productivity-modal" class="fixed inset-0 z-30 hidden items-center justify-center modal-backdrop">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md p-6">
            <div class="flex justify-between items-center mb-4">
                <h3 class="text-lg font-semibold">Productivity</h3>
                <button id="close-productivity-btn" class="text-gray-400 hover:text-gray-700">&times;</button>
            </div>
            <div class="space-y-4">
                <div>
                    <h4 class="font-medium">Task Completion</h4>
                    <div class="w-full bg-gray-200 rounded-full h-2.5 mt-1">
                        <div id="completion-bar" class="bg-green-500 h-2.5 rounded-full" style="width: 0%"></div>
                    </div>
                    <p id="completion-text" class="text-sm text-gray-600 mt-1 text-center">0 of 0 tasks completed</p>
                </div>
                <div>
                    <h4 class="font-medium">Tasks Due Today</h4>
                    <p id="due-today-count" class="text-2xl font-bold text-primary">0</p>
                </div>
                <div>
                    <h4 class="font-medium">Total Projects</h4>
                    <p id="total-projects-count" class="text-2xl font-bold text-purple-500">0</p>
                </div>
            </div>
        </div>
    </div>


<script>
document.addEventListener('DOMContentLoaded', () => {
    // --- LANDING PAGE & LOGIN LOGIC ---
    const landingPage = document.getElementById('landing-page');
    const loginPage = document.getElementById('login-page');
    const appContainer = document.getElementById('app');
    const enterAppButtons = document.querySelectorAll('.enter-app-btn');
    const loginForm = document.getElementById('login-form');
    const googleLoginBtn = document.getElementById('google-login-btn');


    function showLoginPage() {
        landingPage.classList.add('hidden');
        loginPage.classList.remove('hidden');
    }

    function showApp(e) {
        if(e) e.preventDefault(); // Prevent form submission
        loginPage.classList.add('hidden');
        landingPage.classList.add('hidden');
        appContainer.classList.remove('hidden');
        document.body.classList.remove('bg-white');
        document.body.classList.add('bg-gray-50');
    }

    enterAppButtons.forEach(btn => btn.addEventListener('click', showLoginPage));
    loginForm.addEventListener('submit', showApp);
    googleLoginBtn.addEventListener('click', showApp);


    // --- MAIN APP LOGIC ---
    lucide.createIcons();
    
    // --- STATE MANAGEMENT ---
    let state = {
        projects: [
            { id: 1, name: 'Personal' },
            { id: 2, name: 'Work' },
            { id: 3, name: 'Learn Something' }
        ],
        tasks: [
            { id: 1, content: 'Design the new landing page', description: '', projectId: 2, dueDate: getTodayString(), priority: 1, completed: false },
            { id: 2, content: 'Book flight tickets', description: '', projectId: 1, dueDate: getTodayString(), priority: 2, completed: false },
            { id: 3, content: 'Finish JavaScript course', description: '', projectId: 3, dueDate: getTomorrowString(), priority: 3, completed: true },
            { id: 4, content: 'Buy groceries', description: '', projectId: null, dueDate: null, priority: 4, completed: false }
        ],
        currentView: { type: 'inbox', id: null, name: 'Inbox' },
        nextProjectId: 4,
        nextTaskId: 5,
    };

    // --- DOM ELEMENTS ---
    const projectList = document.getElementById('project-list');
    const taskList = document.getElementById('task-list');
    const viewTitle = document.getElementById('view-title');
    const addTaskMainBtn = document.getElementById('add-task-main');
    const addTaskQuickBtn = document.getElementById('add-task-quick');
    const sidebarItems = document.querySelectorAll('.sidebar-item');

    // Modals
    const taskModal = document.getElementById('task-modal');
    const projectModal = document.getElementById('project-modal');
    const productivityModal = document.getElementById('productivity-modal');
    
    // Task Modal Form
    const taskForm = document.getElementById('task-form');
    const taskNameInput = document.getElementById('task-name');
    const taskDescriptionInput = document.getElementById('task-description');
    const taskDueDateInput = document.getElementById('task-due-date');
    const taskPriorityInput = document.getElementById('task-priority');
    const cancelTaskBtn = document.getElementById('cancel-task-btn');
    const breakdownTaskBtn = document.getElementById('breakdown-task-btn');
    const submitTaskBtn = document.getElementById('submit-task-btn');
    const voiceToTaskBtn = document.getElementById('voice-to-task-btn');
    
    // Project Modal Form
    const projectForm = document.getElementById('project-form');
    const projectNameInput = document.getElementById('project-name');
    const addProjectBtn = document.getElementById('add-project-btn');
    const cancelProjectBtn = document.getElementById('cancel-project-btn');
    const addProjectWithAiBtn = document.getElementById('add-project-with-ai-btn');
    
    // Productivity Modal Elements
    const productivityBtn = document.getElementById('productivity-btn');
    const closeProductivityBtn = document.getElementById('close-productivity-btn');
    
    // Project Dropdown in Task Modal
    const projectDropdownBtn = document.getElementById('project-dropdown-btn');
    const selectedProjectNameEl = document.getElementById('selected-project-name');
    const projectDropdownList = document.getElementById('project-dropdown-list');
    let selectedProjectId = null;
    
    // --- GEMINI API INTEGRATION ---
    const GEMINI_API_URL = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=`;

    async function callGeminiAPI(prompt, maxRetries = 3) {
        const apiKey = ""; // This will be provided by the execution environment.
        let attempt = 0;
        while (attempt < maxRetries) {
            try {
                const payload = {
                    contents: [{ parts: [{ text: prompt }] }],
                    generationConfig: {
                        responseMimeType: "application/json",
                    }
                };

                const response = await fetch(GEMINI_API_URL + apiKey, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (!response.ok) {
                    throw new Error(`HTTP error! status: ${response.status}`);
                }

                const result = await response.json();
                
                if (result.candidates && result.candidates[0].content && result.candidates[0].content.parts[0]) {
                    const jsonText = result.candidates[0].content.parts[0].text;
                    return JSON.parse(jsonText);
                } else {
                     console.error("Unexpected API response structure:", result);
                     throw new Error("Invalid response structure from Gemini API.");
                }

            } catch (error) {
                console.error(`Gemini API call failed on attempt ${attempt + 1}:`, error);
                attempt++;
                if (attempt >= maxRetries) {
                    console.error("Gemini API call failed after all retries.");
                    return null;
                }
                const delay = Math.pow(2, attempt) * 1000; // Exponential backoff
                await new Promise(resolve => setTimeout(resolve, delay));
            }
        }
        return null;
    }


    // --- UTILITY FUNCTIONS ---
    function getTodayString() {
        const today = new Date();
        return today.toISOString().split('T')[0];
    }
    
    function getTomorrowString() {
        const tomorrow = new Date();
        tomorrow.setDate(tomorrow.getDate() + 1);
        return tomorrow.toISOString().split('T')[0];
    }

    function formatDate(dateString) {
        if (!dateString) return '';
        const date = new Date(dateString);
        const today = new Date();
        const tomorrow = new Date();
        tomorrow.setDate(today.getDate() + 1);
        
        if (date.toDateString() === today.toDateString()) return 'Today';
        if (date.toDateString() === tomorrow.toDateString()) return 'Tomorrow';
        
        return date.toLocaleDateString('en-US', { month: 'short', day: 'numeric' });
    }

    const priorityColors = {
        1: 'text-red-600',
        2: 'text-orange-500',
        3: 'text-blue-500',
        4: 'text-gray-500'
    };
    
    // --- RENDER FUNCTIONS ---
    function renderProjects() {
        projectList.innerHTML = '';
        state.projects.forEach(project => {
            const li = document.createElement('li');
            li.className = `sidebar-item flex items-center justify-between gap-2 px-3 py-2 text-sm font-medium rounded-md cursor-pointer group`;
            li.dataset.viewType = 'project';
            li.dataset.viewId = project.id;
            li.innerHTML = `
                <div class="flex items-center gap-2">
                    <span class="w-2 h-2 rounded-full bg-gray-300"></span>
                    <span class="flex-1">${project.name}</span>
                </div>
                <button class="delete-project-btn hidden group-hover:block text-gray-400 hover:text-red-500" data-project-id="${project.id}">
                    <i data-lucide="trash-2" class="w-3 h-3"></i>
                </button>
            `;
            projectList.appendChild(li);
        });
        lucide.createIcons();
    }

    function renderTasks() {
        const { type, id } = state.currentView;
        let filteredTasks = [];

        if (type === 'inbox') {
            filteredTasks = state.tasks.filter(t => t.projectId === null);
        } else if (type === 'today') {
            const todayStr = getTodayString();
            filteredTasks = state.tasks.filter(t => t.dueDate === todayStr);
        } else if (type === 'upcoming') {
             filteredTasks = state.tasks.filter(t => t.dueDate && !t.completed);
        } else if (type === 'project') {
            filteredTasks = state.tasks.filter(t => t.projectId === id);
        }
        
        taskList.innerHTML = '';

        if (type === 'upcoming') {
            renderUpcomingTasks(filteredTasks);
        } else {
            const activeTasks = filteredTasks.filter(t => !t.completed);
            const completedTasks = filteredTasks.filter(t => t.completed);

            activeTasks.sort((a,b) => a.priority - b.priority).forEach(task => taskList.appendChild(createTaskElement(task)));
            if (completedTasks.length > 0) {
                const completedHeader = document.createElement('h3');
                completedHeader.className = "text-sm font-semibold mt-6 text-gray-500";
                completedHeader.textContent = "Completed";
                taskList.appendChild(completedHeader);
                completedTasks.forEach(task => taskList.appendChild(createTaskElement(task)));
            }
        }
        lucide.createIcons();
    }
    
    function renderUpcomingTasks(tasks) {
        const groupedTasks = tasks.reduce((acc, task) => {
            const date = task.dueDate || 'No Date';
            if (!acc[date]) {
                acc[date] = [];
            }
            acc[date].push(task);
            return acc;
        }, {});

        const sortedDates = Object.keys(groupedTasks).sort();
        
        sortedDates.forEach(date => {
            const dateHeader = document.createElement('div');
            dateHeader.className = 'mb-4';
            dateHeader.innerHTML = `<h3 class="font-bold border-b pb-1">${formatDate(date)} <span class="text-gray-400 font-normal text-sm">${new Date(date).toLocaleDateString('en-US', { weekday: 'long' })}</span></h3>`;
            taskList.appendChild(dateHeader);
            
            const tasksOnDate = groupedTasks[date];
            tasksOnDate.sort((a,b) => a.priority - b.priority).forEach(task => {
                taskList.appendChild(createTaskElement(task));
            });
        });
    }

    function createTaskElement(task) {
        const div = document.createElement('div');
        div.className = 'task-item flex items-start gap-3 p-2 rounded-md hover:bg-gray-100';
        div.dataset.taskId = task.id;

        const projectName = task.projectId ? state.projects.find(p => p.id === task.projectId)?.name : null;
        
        div.innerHTML = `
            <button class="complete-task-btn mt-1 shrink-0">
                <i data-lucide="${task.completed ? 'check-circle-2' : 'circle'}" class="w-5 h-5 ${priorityColors[task.priority]}"></i>
            </button>
            <div class="flex-1">
                <p class="${task.completed ? 'line-through text-gray-500' : ''}">${task.content}</p>
                <div class="flex items-center gap-4 text-xs text-gray-500 mt-1">
                    ${task.dueDate ? `<span>${formatDate(task.dueDate)}</span>` : ''}
                    ${projectName ? `<span class="flex items-center gap-1"><span class="w-2 h-2 rounded-full bg-gray-300"></span> ${projectName}</span>` : ''}
                </div>
            </div>
            <div class="actions flex items-center gap-2">
                <button class="edit-task-btn text-gray-400 hover:text-blue-500" data-task-id="${task.id}">
                    <i data-lucide="edit" class="w-4 h-4"></i>
                </button>
                <button class="delete-task-btn text-gray-400 hover:text-red-500" data-task-id="${task.id}">
                    <i data-lucide="trash-2" class="w-4 h-4"></i>
                </button>
            </div>
        `;
        return div;
    }

    function updateView() {
        viewTitle.textContent = state.currentView.name;
        sidebarItems.forEach(item => {
            const type = item.dataset.viewType;
            const id = item.dataset.viewId;
            if (type === state.currentView.type && (type !== 'project' || id === String(state.currentView.id))) {
                item.classList.add('active');
            } else {
                item.classList.remove('active');
            }
        });
        projectList.querySelectorAll('.sidebar-item').forEach(item => {
             const type = item.dataset.viewType;
             const id = item.dataset.viewId;
             if (type === 'project' && id === String(state.currentView.id)) {
                 item.classList.add('active');
             } else {
                 item.classList.remove('active');
             }
        });
        renderTasks();
    }
    
    // --- EVENT HANDLERS ---
    
    // View Switching
    function handleViewChange(e) {
        const target = e.target.closest('.sidebar-item');
        if (!target) return;
        
        const { viewType, viewId } = target.dataset;
        state.currentView.type = viewType;
        
        if (viewType === 'project') {
            state.currentView.id = parseInt(viewId);
            state.currentView.name = state.projects.find(p => p.id === state.currentView.id)?.name || 'Project';
        } else {
            state.currentView.id = null;
            state.currentView.name = viewType.charAt(0).toUpperCase() + viewType.slice(1);
        }
        updateView();
    }
    document.querySelector('nav').addEventListener('click', handleViewChange);
    
    // Task Operations
    function toggleTaskCompletion(taskId) {
        const task = state.tasks.find(t => t.id === taskId);
        if (task) {
            task.completed = !task.completed;
            renderTasks();
        }
    }
    
    function deleteTask(taskId) {
        state.tasks = state.tasks.filter(t => t.id !== taskId);
        renderTasks();
    }

    function editTask(taskId) {
        const task = state.tasks.find(t => t.id === taskId);
        if (task) {
            openTaskModal(task);
        }
    }
    
    taskList.addEventListener('click', e => {
        const completeBtn = e.target.closest('.complete-task-btn');
        const deleteBtn = e.target.closest('.delete-task-btn');
        const editBtn = e.target.closest('.edit-task-btn');

        if (completeBtn) {
            const taskId = parseInt(e.target.closest('.task-item').dataset.taskId);
            toggleTaskCompletion(taskId);
        } else if (deleteBtn) {
            const taskId = parseInt(deleteBtn.dataset.taskId);
            if (confirm('Are you sure you want to delete this task?')) {
                deleteTask(taskId);
            }
        } else if (editBtn) {
            const taskId = parseInt(editBtn.dataset.taskId);
            editTask(taskId);
        }
    });

    // Project Operations
    function deleteProject(projectId) {
        if(confirm('Deleting this project will also delete all its tasks. Are you sure?')) {
            state.projects = state.projects.filter(p => p.id !== projectId);
            state.tasks = state.tasks.filter(t => t.projectId !== projectId);

            if (state.currentView.type === 'project' && state.currentView.id === projectId) {
                state.currentView = { type: 'inbox', id: null, name: 'Inbox' };
            }
            
            renderProjects();
            updateView();
        }
    }
    
    projectList.addEventListener('click', e => {
        const deleteBtn = e.target.closest('.delete-project-btn');
        if (deleteBtn) {
            e.stopPropagation();
            const projectId = parseInt(deleteBtn.dataset.projectId);
            deleteProject(projectId);
        }
    });

    // Modal Handling
    function openTaskModal(task = null) {
        taskForm.reset();
        document.getElementById('task-id').value = '';
        taskNameInput.focus();
        if (task) { // Editing existing task
            document.getElementById('task-id').value = task.id;
            taskNameInput.value = task.content;
            taskDescriptionInput.value = task.description;
            taskDueDateInput.value = task.dueDate || '';
            taskPriorityInput.value = task.priority;
            selectedProjectId = task.projectId;
            submitTaskBtn.textContent = 'Save changes';
            breakdownTaskBtn.style.display = 'none';

        } else { // Adding new task
            selectedProjectId = state.currentView.type === 'project' ? state.currentView.id : null;
            submitTaskBtn.textContent = 'Add task';
            breakdownTaskBtn.style.display = 'flex';
        }
        updateSelectedProjectDisplay();
        taskModal.style.display = 'flex';
    }
    
    function closeTaskModal() {
        taskModal.style.display = 'none';
    }
    
    function openProjectModal() {
        projectForm.reset();
        projectNameInput.focus();
        projectModal.style.display = 'flex';
    }

    function closeProjectModal() {
        projectModal.style.display = 'none';
    }
    
    addTaskMainBtn.addEventListener('click', () => openTaskModal());
    addTaskQuickBtn.addEventListener('click', () => openTaskModal());
    cancelTaskBtn.addEventListener('click', closeTaskModal);

    addProjectBtn.addEventListener('click', openProjectModal);
    cancelProjectBtn.addEventListener('click', closeProjectModal);
    
    taskForm.addEventListener('submit', e => {
        e.preventDefault();
        const id = parseInt(document.getElementById('task-id').value);
        const taskData = {
            content: taskNameInput.value.trim(),
            description: taskDescriptionInput.value.trim(),
            dueDate: taskDueDateInput.value || null,
            priority: parseInt(taskPriorityInput.value),
            projectId: selectedProjectId,
        };

        if (!taskData.content) {
            taskNameInput.classList.add('border', 'border-red-500');
            setTimeout(() => taskNameInput.classList.remove('border', 'border-red-500'), 2000);
            return;
        }

        if (id) { // Update
            const taskIndex = state.tasks.findIndex(t => t.id === id);
            if (taskIndex > -1) {
                state.tasks[taskIndex] = { ...state.tasks[taskIndex], ...taskData };
            }
        } else { // Create
            state.tasks.push({
                ...taskData,
                id: state.nextTaskId++,
                completed: false,
            });
        }
        
        closeTaskModal();
        renderTasks();
    });

    projectForm.addEventListener('submit', e => {
        e.preventDefault();
        const projectName = projectNameInput.value.trim();
        if(projectName) {
            state.projects.push({
                id: state.nextProjectId++,
                name: projectName
            });
            renderProjects();
            closeProjectModal();
        }
    });
    
    // --- AI & SPEECH FEATURE EVENT LISTENERS ---
    
    addProjectWithAiBtn.addEventListener('click', async () => {
        const projectName = projectNameInput.value.trim();
        if (!projectName) {
            projectNameInput.focus();
            return;
        }

        const btnText = addProjectWithAiBtn.querySelector('.btn-text');
        const loader = addProjectWithAiBtn.querySelector('.loader');
        btnText.classList.add('hidden');
        loader.classList.remove('hidden');
        addProjectWithAiBtn.disabled = true;

        const prompt = `You are a project planning assistant. Generate a list of actionable tasks for a new project called "${projectName}". Provide between 4 and 8 tasks. Return the response as a valid JSON object with a single key "tasks" which is an array of strings. For example: {"tasks": ["First task", "Second task"]}`;
        
        const result = await callGeminiAPI(prompt);
        
        btnText.classList.remove('hidden');
        loader.classList.add('hidden');
        addProjectWithAiBtn.disabled = false;

        if (result && result.tasks && Array.isArray(result.tasks)) {
            const newProject = { id: state.nextProjectId++, name: projectName };
            state.projects.push(newProject);
            
            result.tasks.forEach(taskContent => {
                if (typeof taskContent === 'string' && taskContent.trim() !== '') {
                    state.tasks.push({
                        content: taskContent, description: '', dueDate: null, priority: 4,
                        projectId: newProject.id, id: state.nextTaskId++, completed: false,
                    });
                }
            });

            closeProjectModal();
            renderProjects();
            state.currentView = { type: 'project', id: newProject.id, name: newProject.name };
            updateView();

        } else {
            console.error("Failed to generate project plan. Please add the project manually.");
        }
    });

    breakdownTaskBtn.addEventListener('click', async () => {
        const taskName = taskNameInput.value.trim();
        if (!taskName) {
            taskNameInput.focus();
            return;
        }
        
        const btnText = breakdownTaskBtn.querySelector('.btn-text');
        const loader = breakdownTaskBtn.querySelector('.loader');
        btnText.classList.add('hidden');
        loader.classList.remove('hidden');
        breakdownTaskBtn.disabled = true;
        submitTaskBtn.disabled = true;

        const prompt = `You are a productivity assistant. Break down the task "${taskName}" into smaller, actionable sub-tasks. Provide between 2 and 5 sub-tasks. Return the response as a valid JSON object with a single key "tasks" which is an array of strings. For example: {"tasks": ["First sub-task", "Second sub-task"]}`;
        
        const result = await callGeminiAPI(prompt);

        btnText.classList.remove('hidden');
        loader.classList.add('hidden');
        breakdownTaskBtn.disabled = false;
        submitTaskBtn.disabled = false;

        if (result && result.tasks && Array.isArray(result.tasks)) {
            const taskBase = {
                description: taskDescriptionInput.value.trim(),
                dueDate: taskDueDateInput.value || null,
                priority: parseInt(taskPriorityInput.value),
                projectId: selectedProjectId,
                completed: false,
            };
            
            result.tasks.forEach(taskContent => {
                 if (typeof taskContent === 'string' && taskContent.trim() !== '') {
                    state.tasks.push({ ...taskBase, content: taskContent.trim(), id: state.nextTaskId++ });
                 }
            });

            closeTaskModal();
            renderTasks();

        } else {
            console.error("Failed to breakdown task. Please add it manually.");
        }
    });
    
    // Speech Recognition
    const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
    if (SpeechRecognition) {
        const recognition = new SpeechRecognition();
        recognition.continuous = false;
        recognition.lang = 'en-IN';
        recognition.interimResults = false;
        
        voiceToTaskBtn.addEventListener('click', () => {
            voiceToTaskBtn.classList.add('listening', 'text-primary');
            recognition.start();
        });

        recognition.onresult = (event) => {
            const transcript = event.results[0][0].transcript;
            taskNameInput.value = transcript;
        };

        recognition.onend = () => {
             voiceToTaskBtn.classList.remove('listening', 'text-primary');
        };

        recognition.onerror = (event) => {
            console.error('Speech recognition error:', event.error);
            voiceToTaskBtn.classList.remove('listening', 'text-primary');
        };

    } else {
        voiceToTaskBtn.style.display = 'none';
        console.log("Speech Recognition not supported in this browser.");
    }
    
    // --- STANDARD EVENT LISTENERS (CONTINUED) ---

    // Project Dropdown Logic
    function renderProjectDropdown() {
        projectDropdownList.innerHTML = `<div class="p-2 cursor-pointer hover:bg-gray-100" data-project-id="null">Inbox</div>`;
        state.projects.forEach(p => {
            projectDropdownList.innerHTML += `<div class="p-2 cursor-pointer hover:bg-gray-100" data-project-id="${p.id}">${p.name}</div>`;
        });
    }

    function updateSelectedProjectDisplay() {
        if(selectedProjectId === null) {
            selectedProjectNameEl.textContent = 'Inbox';
        } else {
            const project = state.projects.find(p => p.id === selectedProjectId);
            selectedProjectNameEl.textContent = project ? project.name : 'Inbox';
        }
    }
    
    projectDropdownBtn.addEventListener('click', () => {
        renderProjectDropdown();
        projectDropdownList.classList.toggle('hidden');
    });

    projectDropdownList.addEventListener('click', e => {
        const target = e.target.closest('[data-project-id]');
        if (target) {
            const id = target.dataset.projectId;
            selectedProjectId = id === 'null' ? null : parseInt(id);
            updateSelectedProjectDisplay();
            projectDropdownList.classList.add('hidden');
        }
    });
    
    document.addEventListener('click', e => {
        if (!projectDropdownBtn.contains(e.target) && !projectDropdownList.contains(e.target)) {
            projectDropdownList.classList.add('hidden');
        }
    });
    
    // Productivity Modal
    function openProductivityModal() {
        const totalTasks = state.tasks.length;
        const completedTasks = state.tasks.filter(t => t.completed).length;
        const completionPercentage = totalTasks > 0 ? (completedTasks / totalTasks) * 100 : 0;
        
        document.getElementById('completion-bar').style.width = `${completionPercentage}%`;
        document.getElementById('completion-text').textContent = `${completedTasks} of ${totalTasks} tasks completed`;
        
        const dueTodayCount = state.tasks.filter(t => t.dueDate === getTodayString() && !t.completed).length;
        document.getElementById('due-today-count').textContent = dueTodayCount;
        
        document.getElementById('total-projects-count').textContent = state.projects.length;

        productivityModal.style.display = 'flex';
    }
    
    productivityBtn.addEventListener('click', openProductivityModal);
    closeProductivityBtn.addEventListener('click', () => productivityModal.style.display = 'none');
    
    // Close modals with Escape key
    window.addEventListener('keydown', (e) => {
        if (e.key === 'Escape') {
            closeTaskModal();
            closeProjectModal();
            productivityModal.style.display = 'none';
        }
    });


    // --- INITIALIZATION ---
    function initializeApp() {
        renderProjects();
        updateView();
    }

    initializeApp();
});
</script>

</body>
</html>

