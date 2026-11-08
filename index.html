<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop Expense Tracker with Login</title>
    <!-- Tailwind CSS for sleek layout & design -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Hind Siliguri', Arial, sans-serif;
            box-sizing: border-box;
        }
        body {
            background-color: #f4f7f6;
            color: #333;
            min-height: 100vh;
        }
        /* Custom scrollbar styling */
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }
        .daily-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            padding: 12px;
            margin-bottom: 10px;
            transition: all 0.2s ease;
        }
        .daily-row:hover {
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
        }
        .daily-row.income-row { border-left: 5px solid #22c55e; }
        .daily-row.expense-row { border-left: 5px solid #ef4444; }
        
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0; top: 0; width: 100%; height: 100%;
            background-color: rgba(0,0,0,0.5);
            backdrop-filter: blur(2px);
            justify-content: center; align-items: center;
        }
        .modal-content {
            background: #fff; 
            padding: 20px; 
            border-radius: 12px;
            width: 92%; 
            max-width: 480px; 
            max-height: 85vh; 
            overflow-y: auto;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
        }
        .keep-note-card {
            background: #fef08a;
            border: 1px solid #fde047;
            border-radius: 8px;
            padding: 12px;
            margin-bottom: 10px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="p-3 sm:p-6 flex flex-col justify-between min-h-screen">

    <!-- Toast Notification Message Container -->
    <div id="toast" class="fixed top-5 right-5 z-50 transform transition-all duration-300 translate-y-[-100px] opacity-0 pointer-events-none bg-slate-800 text-white px-4 py-3 rounded-lg shadow-xl text-sm font-medium flex items-center gap-2">
        <span id="toast-icon">ℹ️</span>
        <span id="toast-message">Notification message</span>
    </div>

    <!-- AUTHENTICATION SCREEN (Sign Up / Login) -->
    <div id="auth-container" class="max-w-md w-full mx-auto my-auto bg-white p-6 sm:p-8 rounded-2xl shadow-xl border border-slate-100 text-center">
        <div class="w-16 h-16 bg-emerald-100 text-emerald-600 rounded-full flex items-center justify-center text-3xl mx-auto mb-4">
            🔐
        </div>
        <h2 id="auth-title" class="text-2xl font-bold text-slate-800 mb-2">Shop Tracker Login</h2>
        <p class="text-slate-500 text-sm mb-6">দোকানের সমস্ত হিসাব-নিকাশ রাখুন ডিজিটাল মাধ্যমে</p>

        <form id="auth-form" onsubmit="handleAuth(event)" class="flex flex-col gap-3">
            <div class="text-left">
                <label class="text-xs font-semibold text-slate-600 block mb-1">মোবাইল নম্বর</label>
                <input type="text" id="auth-phone" placeholder="Mobile Number (e.g. 017xxxxxxxx)" required class="w-full px-4 py-3 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:outline-none transition-all" />
            </div>

            <div class="text-left">
                <label class="text-xs font-semibold text-slate-600 block mb-1">পাসওয়ার্ড</label>
                <input type="password" id="auth-pass" placeholder="Password" required class="w-full px-4 py-3 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:outline-none transition-all" />
            </div>

            <button type="submit" id="auth-btn" class="w-full py-3 bg-emerald-600 hover:bg-emerald-700 text-white rounded-lg font-bold text-base transition-colors shadow-md mt-2">
                Login
            </button>
        </form>

        <div class="mt-6 text-sm text-blue-600 hover:text-blue-800 cursor-pointer underline transition-colors" onclick="toggleAuthMode()" id="toggle-text">
            New user? Create an account (Sign Up)
        </div>
    </div>

    <!-- MAIN APP SCREEN -->
    <div class="max-w-xl w-full mx-auto bg-white p-4 sm:p-6 rounded-2xl shadow-lg border border-slate-100" id="app-container" style="display: none;">
        
        <!-- App Header & User Profile -->
        <div class="flex justify-between items-center pb-4 mb-4 border-b border-slate-100">
            <div>
                <h2 class="font-bold text-lg text-slate-800 flex items-center gap-2" id="welcome-user">
                    <span>🏬</span> Shop Tracker
                </h2>
            </div>
            <button type="button" onclick="logout()" class="bg-red-50 hover:bg-red-100 text-red-600 border border-red-200 text-xs px-3 py-1.5 rounded-lg font-bold transition-all flex items-center gap-1">
                <span>🚪</span> Logout
            </button>
        </div>

        <!-- Shop Selector Bar -->
        <div class="flex flex-wrap sm:flex-nowrap gap-2 mb-5 bg-slate-100 p-2.5 rounded-xl items-center">
            <select id="shop-selector" onchange="changeActiveShop()" class="flex-1 bg-white border border-slate-300 font-bold text-slate-700 rounded-lg px-3 py-2 text-sm focus:ring-2 focus:ring-emerald-500 outline-none">
                <!-- Shops loaded dynamically -->
            </select>
            <div class="flex gap-1 w-full sm:w-auto justify-end">
                <button type="button" onclick="editCurrentShop()" class="bg-amber-500 hover:bg-amber-600 text-white text-xs px-2.5 py-2 rounded-lg font-semibold transition-colors">Edit</button>
                <button type="button" onclick="deleteCurrentShop()" class="bg-red-500 hover:bg-red-600 text-white text-xs px-2.5 py-2 rounded-lg font-semibold transition-colors">Delete</button>
                <button type="button" onclick="addNewShop()" class="bg-blue-600 hover:bg-blue-700 text-white text-xs px-3 py-2 rounded-lg font-bold transition-colors flex items-center gap-1">+ Add Shop</button>
            </div>
        </div>

        <!-- Summary Header with Notes Icon -->
        <div class="flex justify-between items-center mb-2">
            <span class="text-xs font-bold uppercase tracking-wider text-slate-500" id="current-shop-title">Financial Summary</span>
            <button type="button" onclick="openKeepModal()" class="bg-amber-400 hover:bg-amber-500 text-slate-900 border border-amber-300 px-3 py-1.5 rounded-full font-bold text-xs flex items-center gap-1.5 shadow-sm transition-all">
                <span>💡</span> Shop Notes
            </button>
        </div>

        <!-- Financial Summary Cards Box -->
        <div class="grid grid-cols-3 gap-2 sm:gap-3 mb-6 bg-slate-50 p-3 sm:p-4 rounded-xl border border-slate-200/60 text-center">
            <div class="bg-white p-2.5 rounded-lg border border-slate-100 shadow-sm">
                <h3 class="text-xs text-slate-500 font-medium">Income</h3>
                <p id="total-income" class="text-sm sm:text-lg font-bold text-emerald-600 mt-1">৳0.00</p>
            </div>
            <div class="bg-white p-2.5 rounded-lg border border-slate-100 shadow-sm">
                <h3 class="text-xs text-slate-500 font-medium">Expense</h3>
                <p id="total-expense" class="text-sm sm:text-lg font-bold text-red-600 mt-1">৳0.00</p>
            </div>
            <div class="bg-white p-2.5 rounded-lg border border-slate-100 shadow-sm">
                <h3 class="text-xs text-slate-500 font-medium">Net Balance</h3>
                <p id="net-balance" class="text-sm sm:text-lg font-bold text-blue-600 mt-1">৳0.00</p>
            </div>
        </div>

        <!-- Add Transaction Form -->
        <form id="tracker-form" class="flex flex-col gap-3 mb-6 bg-slate-50/50 p-4 rounded-xl border border-slate-200">
            <h4 class="text-xs font-bold uppercase tracking-wider text-slate-500 mb-1">Add New Entry</h4>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                <input type="text" id="title" placeholder="Description (e.g. Sales, Rent)" required class="w-full px-3 py-2 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 outline-none" />
                <input type="number" id="amount" placeholder="Amount (Taka)" step="any" min="0.01" required class="w-full px-3 py-2 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 outline-none" />
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                <input type="date" id="entry-date" required class="w-full px-3 py-2 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 outline-none text-slate-700" />
                <select id="type" class="w-full px-3 py-2 text-sm border border-slate-300 rounded-lg focus:ring-2 focus:ring-emerald-500 outline-none text-slate-700 bg-white">
                    <option value="expense">Expense (খরচ)</option>
                    <option value="income">Income (জমা/আয়)</option>
                </select>
            </div>

            <button type="submit" class="w-full py-2.5 bg-emerald-600 hover:bg-emerald-700 text-white rounded-lg font-bold text-sm transition-colors shadow-sm mt-1">
                + Add Transaction
            </button>
        </form>

        <!-- Data Backup & Restore Options -->
        <div class="grid grid-cols-2 gap-3 mb-5">
            <button type="button" onclick="backupData()" class="bg-emerald-600 hover:bg-emerald-700 text-white font-semibold text-xs py-2.5 px-3 rounded-lg flex items-center justify-center gap-1.5 transition-colors shadow-sm">
                <span>☁️</span> Backup File
            </button>
            <button type="button" onclick="document.getElementById('importFile').click()" class="bg-slate-700 hover:bg-slate-800 text-white font-semibold text-xs py-2.5 px-3 rounded-lg flex items-center justify-center gap-1.5 transition-colors shadow-sm">
                <span>📂</span> Restore File
            </button>
            <input type="file" id="importFile" style="display:none" onchange="importData(event)" accept=".json">
        </div>

        <!-- Calendar Filter Section -->
        <div class="flex items-center justify-between gap-2 mb-5 bg-slate-100 p-3 rounded-lg border border-slate-200">
            <div class="flex items-center gap-2 flex-1">
                <label for="filter-date" class="text-xs font-bold text-slate-600 whitespace-nowrap">Filter Date:</label>
                <input type="date" id="filter-date" onchange="updateUI()" class="bg-white border border-slate-300 rounded px-2 py-1 text-xs text-slate-700 outline-none flex-1 max-w-[180px]" />
            </div>
            <button type="button" onclick="clearFilter()" class="px-3 py-1 text-xs bg-slate-500 hover:bg-slate-600 text-white font-medium rounded transition-colors">
                Show All
            </button>
        </div>

        <!-- Transaction History -->
        <div class="text-sm font-bold text-slate-800 pb-2 mb-3 border-b border-slate-200 flex justify-between items-center">
            <span>Transaction History</span>
            <span id="history-count" class="text-xs font-normal text-slate-500">0 records</span>
        </div>
        <div id="history-container" class="space-y-2">
            <!-- Dynamic list of transaction groups -->
        </div>

    </div>

    <!-- Google Keep Style Notes Modal -->
    <div id="keepModal" class="modal">
        <div class="modal-content">
            <div class="flex justify-between items-center pb-3 mb-4 border-b border-slate-200">
                <h3 id="modal-shop-note-title" class="font-bold text-slate-800 text-base flex items-center gap-1.5">
                    💡 Shop Notes
                </h3>
                <button type="button" onclick="closeKeepModal()" class="bg-slate-200 hover:bg-red-500 hover:text-white text-slate-600 font-bold rounded-full w-7 h-7 flex items-center justify-center text-xs transition-colors">
                    ✕
                </button>
            </div>
            
            <form id="keep-note-form" class="mb-4">
                <div class="bg-slate-50 border border-slate-300 rounded-xl p-3 focus-within:ring-2 focus-within:ring-amber-400">
                    <textarea id="keep-content" placeholder="Take a note for this shop..." rows="3" class="w-full border-none bg-transparent outline-none resize-none text-sm text-slate-800 placeholder-slate-400" required></textarea>
                    <div class="flex justify-between items-center mt-2 pt-2 border-t border-slate-200/60">
                        <input type="date" id="keep-date" class="bg-white border border-slate-300 rounded px-2 py-1 text-xs text-slate-700" required />
                        <button type="submit" id="keep-submit-btn" class="px-4 py-1.5 text-xs font-bold bg-amber-500 hover:bg-amber-600 text-white rounded-lg transition-colors shadow-sm">
                            Save Note
                        </button>
                    </div>
                </div>
            </form>

            <div id="keep-notes-container" class="space-y-3 max-h-[300px] overflow-y-auto pr-1">
                <!-- Dynamically rendered notes -->
            </div>
        </div>
    </div>

    <!-- Edit Modal Box for Daily Grouped Transactions -->
    <div id="editModal" class="modal">
        <div class="modal-content">
            <div class="flex justify-between items-center pb-3 mb-4 border-b border-slate-200">
                <h3 id="modal-date-title" class="font-bold text-slate-800 text-sm">Edit Transactions</h3>
                <button type="button" onclick="closeEditModal()" class="bg-slate-200 hover:bg-red-500 hover:text-white text-slate-600 font-bold rounded-full w-7 h-7 flex items-center justify-center text-xs transition-colors">
                    ✕
                </button>
            </div>
            <div id="modal-items-container" class="space-y-3 max-h-[350px] overflow-y-auto pr-1">
                <!-- Dynamically populated transaction edit items -->
            </div>
        </div>
    </div>

    <!-- Footer Credit -->
    <footer class="text-center text-slate-400 text-xs mt-6 mb-2">
        Shop Expense Tracker &copy; Digital Ledger Application
    </footer>

<script>
    // Helper function to show modern toast notifications instead of alerts
    function showToast(message, type = 'info') {
        const toast = document.getElementById('toast');
        const toastMsg = document.getElementById('toast-message');
        const toastIcon = document.getElementById('toast-icon');

        toastMsg.innerText = message;
        if (type === 'error') toastIcon.innerText = '⚠️';
        else if (type === 'success') toastIcon.innerText = '✅';
        else toastIcon.innerText = 'ℹ️';

        toast.classList.remove('translate-y-[-100px]', 'opacity-0', 'pointer-events-none');
        toast.classList.add('translate-y-0', 'opacity-100');

        setTimeout(() => {
            toast.classList.remove('translate-y-0', 'opacity-100');
            toast.classList.add('translate-y-[-100px]', 'opacity-0', 'pointer-events-none');
        }, 3000);
    }

    // Helper: Formats current date to YYYY-MM-DD
    function getTodayDate() {
        const now = new Date();
        const year = now.getFullYear();
        const month = String(now.getMonth() + 1).padStart(2, '0');
        const day = String(now.getDate()).padStart(2, '0');
        return `${year}-${month}-${day}`;
    }

    // Set initial date inputs to today
    document.getElementById('entry-date').value = getTodayDate();
    document.getElementById('keep-date').value = getTodayDate();

    let isSignUpMode = false;
    let currentUser = localStorage.getItem('activeUser') || null;
    let allUsersData = JSON.parse(localStorage.getItem('allUsersData')) || {};
    let currentShop = "Shop 1";
    let editingNoteId = null;

    // Verify session and view initialization
    function checkLoginState() {
        if (currentUser && allUsersData[currentUser]) {
            document.getElementById('auth-container').style.display = 'none';
            document.getElementById('app-container').style.display = 'block';
            document.getElementById('welcome-user').innerHTML = `<span>🏬</span> ${currentUser}`;
            
            let shops = getUserShops();
            const shopKeys = Object.keys(shops);
            if (shopKeys.length > 0 && !shops[currentShop]) {
                currentShop = shopKeys[0];
            }
            renderShopSelector();
            updateUI();
        } else {
            document.getElementById('auth-container').style.display = 'block';
            document.getElementById('app-container').style.display = 'none';
        }
    }

    // Toggle between login and sign up mode
    function toggleAuthMode() {
        isSignUpMode = !isSignUpMode;
        document.getElementById('auth-title').innerText = isSignUpMode ? "📝 Create New Account" : "🔐 Shop Tracker Login";
        document.getElementById('auth-btn').innerText = isSignUpMode ? "Sign Up" : "Login";
        document.getElementById('toggle-text').innerText = isSignUpMode ? "Already have an account? Login" : "New user? Create an account (Sign Up)";
    }

    // Authentication form handler
    function handleAuth(e) {
        e.preventDefault();
        const phone = document.getElementById('auth-phone').value.trim();
        const pass = document.getElementById('auth-pass').value.trim();
        
        if (!phone || !pass) {
            showToast("দয়া করে মোবাইল নম্বর এবং পাসওয়ার্ড প্রদান করুন", "error");
            return;
        }

        if (isSignUpMode) {
            if (allUsersData[phone]) {
                showToast("এই নম্বর দিয়ে আগেই অ্যাকাউন্ট খোলা রয়েছে! লগইন করুন।", "error");
                return;
            }
            allUsersData[phone] = {
                password: pass,
                shops: { "Shop 1": { transactions: [], notes: [] } }
            };
            localStorage.setItem('allUsersData', JSON.stringify(allUsersData));
            showToast("অ্যাকাউন্ট সফলভাবে তৈরি হয়েছে! এখন লগইন করুন।", "success");
            toggleAuthMode();
            document.getElementById('auth-form').reset();
        } else {
            if (!allUsersData[phone] || allUsersData[phone].password !== pass) {
                showToast("ভুল মোবাইল নম্বর অথবা পাসওয়ার্ড!", "error");
                return;
            }
            currentUser = phone;
            localStorage.setItem('activeUser', currentUser);
            document.getElementById('auth-form').reset();
            checkLoginState();
            showToast("সফলভাবে লগইন হয়েছে!", "success");
        }
    }

    // Logout session handler
    function logout() {
        localStorage.removeItem('activeUser');
        currentUser = null;
        checkLoginState();
        showToast("লগআউট করা হয়েছে");
    }

    // Returns active user's shop dataset safely
    function getUserShops() {
        if (!allUsersData[currentUser]) {
            allUsersData[currentUser] = { password: "", shops: { "Shop 1": { transactions: [], notes: [] } } };
        }
        if (!allUsersData[currentUser].shops) {
            allUsersData[currentUser].shops = { "Shop 1": { transactions: [], notes: [] } };
        }
        return allUsersData[currentUser].shops;
    }

    // Sync to LocalStorage
    function saveUserData() {
        localStorage.setItem('allUsersData', JSON.stringify(allUsersData));
    }

    // Populate dropdown with active user's shops
    function renderShopSelector() {
        const selector = document.getElementById('shop-selector');
        selector.innerHTML = '';
        
        const shops = getUserShops();
        let shopKeys = Object.keys(shops);
        
        if (shopKeys.length === 0) {
            shops["Shop 1"] = { transactions: [], notes: [] };
            currentShop = "Shop 1";
            shopKeys = ["Shop 1"];
        }

        if (!shops[currentShop]) {
            currentShop = shopKeys[0];
        }

        shopKeys.forEach(shopName => {
            const option = document.createElement('option');
            option.value = shopName;
            option.innerText = shopName;
            if (shopName === currentShop) option.selected = true;
            selector.appendChild(option);
        });
        
        document.getElementById('current-shop-title').innerText = `${currentShop} Summary`;
    }

    // Change currently selected shop
    function changeActiveShop() {
        const selector = document.getElementById('shop-selector');
        if (selector.value) {
            currentShop = selector.value;
            document.getElementById('current-shop-title').innerText = `${currentShop} Summary`;
            document.getElementById('filter-date').value = '';
            updateUI();
        }
    }

    // Create a new shop
    function addNewShop() {
        let shopName = prompt("নতুন দোকানের নাম লিখুন:");
        if (shopName) {
            shopName = shopName.trim();
            if (!shopName) return;
            
            const shops = getUserShops();
            if (shops[shopName]) {
                showToast("এই নামের দোকান আগেই আছে!", "error");
                return;
            }
            
            shops[shopName] = { transactions: [], notes: [] };
            currentShop = shopName;
            saveUserData();
            renderShopSelector();
            updateUI();
            showToast(`'${shopName}' তৈরি করা হয়েছে`, "success");
        }
    }

    // Rename active shop
    function editCurrentShop() {
        let newName = prompt("দোকানের নতুন নাম লিখুন:", currentShop);
        if (newName) {
            newName = newName.trim();
            if (!newName) return;
            if (newName === currentShop) return;
            
            const shops = getUserShops();
            if (shops[newName]) {
                showToast("এই নামের দোকান ইতিমধ্যে রয়েছে!", "error");
                return;
            }
            shops[newName] = shops[currentShop];
            delete shops[currentShop];
            currentShop = newName;
            saveUserData();
            renderShopSelector();
            updateUI();
            showToast("দোকানের নাম পরিবর্তন করা হয়েছে!", "success");
        }
    }

    // Delete active shop
    function deleteCurrentShop() {
        const shops = getUserShops();
        const shopKeys = Object.keys(shops);
        
        if (shopKeys.length <= 1) {
            showToast("কমপক্ষে একটি দোকান থাকা বাধ্যতামূলক!", "error");
            return;
        }

        if (confirm(`আপনি কি সত্যিই '${currentShop}' দোকানটি এবং এর সমস্ত হিসাব মুছে ফেলতে চান?`)) {
            delete shops[currentShop];
            const remainingKeys = Object.keys(shops);
            currentShop = remainingKeys[0];
            
            saveUserData();
            renderShopSelector();
            updateUI();
            showToast("দোকানটি মুছে ফেলা হয়েছে!", "success");
        }
    }

    // Main UI update engine: updates transaction history & dashboard metrics
    function updateUI() {
        renderShopSelector();
        const historyContainer = document.getElementById('history-container');
        historyContainer.innerHTML = '';
        const filterDate = document.getElementById('filter-date').value;
        const shops = getUserShops();
        
        if (!shops[currentShop]) {
            const keys = Object.keys(shops);
            currentShop = keys.length > 0 ? keys[0] : "Shop 1";
            if (!shops[currentShop]) {
                shops[currentShop] = { transactions: [], notes: [] };
            }
        }
        
        const shopTransactions = shops[currentShop].transactions || [];
        let totalIncomeSum = 0;
        let totalExpenseSum = 0;
        const grouped = {};

        shopTransactions.forEach((item) => {
            const parsedAmount = parseFloat(item.amount) || 0;
            if (item.type === 'income') totalIncomeSum += parsedAmount;
            else totalExpenseSum += parsedAmount;

            if (filterDate && item.date !== filterDate) return;

            const key = `${item.date}_${item.type}`;
            if (!grouped[key]) {
                grouped[key] = { date: item.date, type: item.type, titles: [], totalAmount: 0, ids: [] };
            }
            grouped[key].titles.push(item.title);
            grouped[key].totalAmount += parsedAmount;
            grouped[key].ids.push(item.id);
        });

        const sortedKeys = Object.keys(grouped).sort((a, b) => new Date(b.split('_')[0]) - new Date(a.split('_')[0]));
        
        document.getElementById('history-count').innerText = `${sortedKeys.length} items`;

        if (sortedKeys.length === 0) {
            historyContainer.innerHTML = `
                <div class="text-center py-8 text-slate-400 bg-slate-50 rounded-xl border border-dashed border-slate-200">
                    <p class="text-sm">কোনো লেনদেন পাওয়া যায়নি</p>
                </div>
            `;
        } else {
            sortedKeys.forEach(key => {
                const group = grouped[key];
                const rowDiv = document.createElement('div');
                const isIncome = group.type === 'income';
                rowDiv.className = `daily-row ${isIncome ? 'income-row' : 'expense-row'}`;
                
                const sign = isIncome ? '+' : '-';
                const amountColor = isIncome ? 'text-emerald-600' : 'text-red-600';
                
                rowDiv.innerHTML = `
                    <div>
                        <div class="font-bold text-slate-800 text-xs sm:text-sm flex items-center gap-1.5">
                            <span>📅 ${group.date}</span>
                            <span class="text-[10px] px-1.5 py-0.5 rounded ${isIncome ? 'bg-emerald-100 text-emerald-700' : 'bg-red-100 text-red-700'} font-bold uppercase">${group.type}</span>
                        </div>
                        <div class="text-xs text-slate-500 mt-1">📝 ${group.titles.join(', ')}</div>
                    </div>
                    <div class="flex items-center gap-2">
                        <span class="font-bold text-sm sm:text-base ${amountColor} mr-1">${sign}৳${group.totalAmount.toFixed(2)}</span>
                        <button type="button" class="bg-amber-500 hover:bg-amber-600 text-white px-2 py-1 rounded text-xs font-semibold transition-colors" onclick="openEditModal('${group.date}', '${group.type}')">Edit</button>
                        <button type="button" class="bg-red-500 hover:bg-red-600 text-white px-2 py-1 rounded text-xs font-semibold transition-colors" onclick="deleteGroup('${group.ids.join(",")}')">✕</button>
                    </div>
                `;
                historyContainer.appendChild(rowDiv);
            });
        }

        document.getElementById('total-income').innerText = `৳${totalIncomeSum.toFixed(2)}`;
        document.getElementById('total-expense').innerText = `৳${totalExpenseSum.toFixed(2)}`;
        const net = totalIncomeSum - totalExpenseSum;
        const netElem = document.getElementById('net-balance');
        netElem.innerText = `৳${net.toFixed(2)}`;
        if (net < 0) {
            netElem.className = "text-sm sm:text-lg font-bold text-red-600 mt-1";
        } else {
            netElem.className = "text-sm sm:text-lg font-bold text-blue-600 mt-1";
        }

        saveUserData();
    }

    // Submit new transaction handler
    document.getElementById('tracker-form').addEventListener('submit', function(e) {
        e.preventDefault();
        const title = document.getElementById('title').value.trim();
        const rawAmount = document.getElementById('amount').value;
        const date = document.getElementById('entry-date').value;
        const type = document.getElementById('type').value;

        const numAmount = parseFloat(rawAmount);
        if (isNaN(numAmount) || numAmount <= 0) {
            showToast('সঠিক টাকার পরিমাণ লিখুন!', 'error');
            return;
        }

        const shops = getUserShops();
        if (!shops[currentShop]) {
            shops[currentShop] = { transactions: [], notes: [] };
        }

        shops[currentShop].transactions.push({
            id: Date.now().toString() + Math.random().toString(36).substring(2, 5),
            title, amount: numAmount, type, date
        });

        document.getElementById('filter-date').value = '';
        updateUI();
        document.getElementById('title').value = '';
        document.getElementById('amount').value = '';
        document.getElementById('entry-date').value = getTodayDate();
        showToast('নতুন এনট্রি যুক্ত হয়েছে', 'success');
    });

    // Google Keep Modal Control
    function openKeepModal() {
        document.getElementById('modal-shop-note-title').innerHTML = `💡 ${currentShop} Notes`;
        document.getElementById('keepModal').style.display = 'flex';
        renderKeepNotes();
    }

    function closeKeepModal() {
        document.getElementById('keepModal').style.display = 'none';
        editingNoteId = null;
        document.getElementById('keep-content').value = '';
        document.getElementById('keep-submit-btn').innerText = 'Save Note';
        updateUI();
    }

    // Add or update note logic
    document.getElementById('keep-note-form').addEventListener('submit', function(e) {
        e.preventDefault();
        const content = document.getElementById('keep-content').value.trim();
        const date = document.getElementById('keep-date').value;

        if (!content) return;

        const shops = getUserShops();
        if (!shops[currentShop]) {
            shops[currentShop] = { transactions: [], notes: [] };
        }

        let shopNotes = shops[currentShop].notes;

        if (editingNoteId) {
            const note = shopNotes.find(n => n.id === editingNoteId);
            if (note) {
                note.content = content;
                note.date = date;
            }
            editingNoteId = null;
            document.getElementById('keep-submit-btn').innerText = 'Save Note';
            showToast("নোট আপডেট করা হয়েছে", "success");
        } else {
            shopNotes.push({
                id: Date.now().toString() + Math.random().toString(36).substring(2, 5),
                content, date
            });
            showToast("নতুন নোট যুক্ত হয়েছে", "success");
        }

        document.getElementById('keep-content').value = '';
        document.getElementById('keep-date').value = getTodayDate();
        renderKeepNotes();
        saveUserData();
    });

    // Render list of notes for active shop
    function renderKeepNotes() {
        const container = document.getElementById('keep-notes-container');
        container.innerHTML = '';
        const shops = getUserShops();

        if (!shops[currentShop]) {
            shops[currentShop] = { transactions: [], notes: [] };
        }

        const shopNotes = shops[currentShop].notes || [];
        const sortedNotes = [...shopNotes].sort((a, b) => new Date(b.date) - new Date(a.date));

        if (sortedNotes.length === 0) {
            container.innerHTML = '<p class="text-center text-slate-400 text-xs py-4">এই দোকানের জন্য কোনো নোট নেই</p>';
            return;
        }

        sortedNotes.forEach(note => {
            const card = document.createElement('div');
            card.className = 'keep-note-card';
            card.innerHTML = `
                <div class="text-[11px] font-bold text-amber-800 mb-1 flex items-center justify-between">
                    <span>📅 ${note.date}</span>
                </div>
                <div class="text-xs text-slate-800 whitespace-pre-wrap mb-2 leading-relaxed">${note.content}</div>
                <div class="flex justify-end gap-1 border-t border-amber-300/60 pt-1.5">
                    <button type="button" class="bg-amber-600 hover:bg-amber-700 text-white text-[10px] px-2 py-0.5 rounded font-semibold transition-colors" onclick="editKeepNote('${note.id}')">Edit</button>
                    <button type="button" class="bg-red-500 hover:bg-red-600 text-white text-[10px] px-2 py-0.5 rounded font-semibold transition-colors" onclick="deleteKeepNote('${note.id}')">Delete</button>
                </div>
            `;
            container.appendChild(card);
        });
    }

    function editKeepNote(id) {
        const shopNotes = getUserShops()[currentShop].notes;
        const note = shopNotes.find(n => n.id === id);
        if (!note) return;

        document.getElementById('keep-content').value = note.content;
        document.getElementById('keep-date').value = note.date;
        editingNoteId = id;
        document.getElementById('keep-submit-btn').innerText = 'Update Note';
    }

    function deleteKeepNote(id) {
        getUserShops()[currentShop].notes = getUserShops()[currentShop].notes.filter(n => n.id !== id);
        renderKeepNotes();
        saveUserData();
        showToast("নোট মুছে ফেলা হয়েছে");
    }

    // Daily Transaction Modal Editing Operations
    function openEditModal(date, type) {
        const modal = document.getElementById('editModal');
        const modalTitle = document.getElementById('modal-date-title');
        const container = document.getElementById('modal-items-container');
        container.innerHTML = '';

        modalTitle.innerText = `Edit: ${date} (${type.toUpperCase()})`;
        const shopTransactions = getUserShops()[currentShop].transactions;
        const filteredItems = shopTransactions.filter(item => item.date === date && item.type === type);

        filteredItems.forEach(item => {
            const itemDiv = document.createElement('div');
            itemDiv.className = 'p-3 bg-slate-50 border border-slate-200 rounded-lg flex items-center justify-between gap-2';
            itemDiv.innerHTML = `
                <div class="flex flex-col gap-1.5 flex-1">
                    <input type="text" id="edit-title-${item.id}" value="${item.title}" class="w-full px-2 py-1 text-xs border border-slate-300 rounded focus:ring-1 focus:ring-amber-500 outline-none" />
                    <input type="number" id="edit-amount-${item.id}" value="${item.amount}" step="any" class="w-full px-2 py-1 text-xs border border-slate-300 rounded focus:ring-1 focus:ring-amber-500 outline-none" />
                </div>
                <div class="flex flex-col gap-1">
                    <button type="button" class="bg-emerald-600 hover:bg-emerald-700 text-white text-[11px] px-2.5 py-1 rounded font-semibold transition-colors" onclick="saveSingleItem('${item.id}', '${date}', '${type}')">Save</button>
                    <button type="button" class="bg-red-500 hover:bg-red-600 text-white text-[11px] px-2.5 py-1 rounded font-semibold transition-colors" onclick="deleteSingleItem('${item.id}', '${date}', '${type}')">Delete</button>
                </div>
            `;
            container.appendChild(itemDiv);
        });
        modal.style.display = 'flex';
    }

    function closeEditModal() {
        document.getElementById('editModal').style.display = 'none';
        updateUI();
    }

    function saveSingleItem(id, date, type) {
        const newTitle = document.getElementById(`edit-title-${id}`).value.trim();
        const newAmount = parseFloat(document.getElementById(`edit-amount-${id}`).value);

        if (!newTitle || isNaN(newAmount) || newAmount <= 0) {
            showToast('সঠিক তথ্য দিন!', 'error');
            return;
        }

        const shopTransactions = getUserShops()[currentShop].transactions;
        const item = shopTransactions.find(t => t.id === id);
        if (item) {
            item.title = newTitle;
            item.amount = newAmount;
        }

        showToast('সফলভাবে আপডেট করা হয়েছে!', 'success');
        openEditModal(date, type);
        updateUI();
    }

    function deleteSingleItem(id, date, type) {
        let shopTransactions = getUserShops()[currentShop].transactions;
        getUserShops()[currentShop].transactions = shopTransactions.filter(t => t.id !== id);

        const remaining = getUserShops()[currentShop].transactions.filter(t => t.date === date && t.type === type);
        if (remaining.length === 0) {
            closeEditModal();
        } else {
            openEditModal(date, type);
        }
        updateUI();
        showToast('আইটেম মুছে ফেলা হয়েছে');
    }

    function deleteGroup(idsString) {
        if (!confirm('এই তারিখ ও টাইপের সমস্ত লেনদেন মুছে ফেলতে চান?')) return;
        const idsToDelete = idsString.split(',');
        let shopTransactions = getUserShops()[currentShop].transactions;
        getUserShops()[currentShop].transactions = shopTransactions.filter(item => !idsToDelete.includes(item.id));
        updateUI();
        showToast('গ্রুপ রেকর্ডসমূহ মুছে ফেলা হয়েছে');
    }

    function clearFilter() {
        document.getElementById('filter-date').value = '';
        updateUI();
    }

    // Export current data snapshot into downloadable JSON file
    function backupData() {
        const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(allUsersData));
        const downloadAnchor = document.createElement('a');
        downloadAnchor.setAttribute("href", dataStr);
        downloadAnchor.setAttribute("download", `Shop_Tracker_Backup_${currentUser}_${getTodayDate()}.json`);
        document.body.appendChild(downloadAnchor);
        downloadAnchor.click();
        downloadAnchor.remove();
        showToast('ব্যাকআপ ফাইল ডাউনলোড সফল হয়েছে!', 'success');
    }

    // Import JSON backup data back into local state
    function importData(event) {
        const fileReader = new FileReader();
        fileReader.onload = function() {
            try {
                const imported = JSON.parse(fileReader.result);
                if (imported) {
                    allUsersData = imported;
                    localStorage.setItem('allUsersData', JSON.stringify(allUsersData));
                    checkLoginState();
                    showToast('ডেটা সফলভাবে রিস্টোর হয়েছে!', 'success');
                }
            } catch (e) {
                showToast('ভুল ব্যাকআপ ফাইল!', 'error');
            }
        };
        if (event.target.files[0]) {
            fileReader.readAsText(event.target.files[0]);
        }
    }

    // Initialize application state
    checkLoginState();
</script>
</body>
</html>
