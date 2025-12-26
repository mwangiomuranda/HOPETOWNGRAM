[hopetow.html](https://github.com/user-attachments/files/24344741/hopetow.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mwihoko Nitaa - HOPETOWNGRAM</title>
    
    <!-- Fonts & Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* ===== RESET & BASE STYLES ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            /* Instagram-inspired Color Palette */
            --gradient: linear-gradient(45deg, #405DE6, #5851DB, #833AB4, #C13584, #E1306C, #FD1D1D, #F56040, #FCAF45, #FFDC80);
            --primary: #405DE6;
            --secondary: #C13584;
            --accent: #FCAF45;
            --danger: #FD1D1D;
            --success: #00C851;
            --dark: #262626;
            --gray: #8E8E8E;
            --light: #FAFAFA;
            --border: #DBDBDB;
            --shadow: 0 10px 40px rgba(0,0,0,0.1);
            --radius: 16px;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #fafafa;
            color: var(--dark);
            min-height: 100vh;
        }

        .app-container {
            max-width: 100%;
            overflow-x: hidden;
        }

        /* ===== LOGIN PAGE ===== */
        .login-page {
            display: flex;
            min-height: 100vh;
            background: var(--gradient);
            padding: 20px;
        }

        .login-card {
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            margin: auto;
            max-width: 500px;
            width: 100%;
            overflow: hidden;
        }

        .login-header {
            background: var(--gradient);
            padding: 40px;
            text-align: center;
            color: white;
            position: relative;
        }

        .logo-main {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }

        .logo-circle {
            width: 100px;
            height: 100px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .logo-text {
            font-size: 48px;
            font-weight: 900;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo-circle .logo-text {
            font-size: 32px;
        }

        .platform-name {
            font-size: 32px;
            font-weight: 800;
            margin-bottom: 10px;
        }

        .domain {
            font-size: 14px;
            opacity: 0.9;
            letter-spacing: 2px;
        }

        .login-form {
            padding: 40px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-label {
            display: block;
            margin-bottom: 10px;
            font-weight: 500;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .form-input {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid var(--border);
            border-radius: 12px;
            font-size: 16px;
            font-family: 'Poppins', sans-serif;
            background: #fafafa;
            transition: all 0.3s ease;
        }

        .form-input:focus {
            outline: none;
            border-color: var(--primary);
            background: white;
            box-shadow: 0 0 0 3px rgba(64, 93, 230, 0.1);
        }

        .password-container {
            position: relative;
        }

        .password-toggle {
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: var(--gray);
            cursor: pointer;
            font-size: 18px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 14px 28px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Poppins', sans-serif;
            text-decoration: none;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(64, 93, 230, 0.3);
        }

        .btn-block {
            width: 100%;
        }

        .login-info {
            background: #f8f9ff;
            padding: 20px;
            border-radius: 12px;
            margin-top: 30px;
            border-left: 4px solid var(--primary);
        }

        .mpesa-format {
            background: #eef2ff;
            padding: 12px;
            border-radius: 8px;
            font-family: monospace;
            font-size: 13px;
            color: var(--primary);
            margin-top: 10px;
        }

        /* ===== DASHBOARD ===== */
        .dashboard-page {
            display: none;
            min-height: 100vh;
        }

        /* Top Navigation */
        .dashboard-nav {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 0 30px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-brand {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .nav-brand-circle {
            width: 40px;
            height: 40px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 900;
            font-size: 18px;
        }

        .nav-tabs {
            display: flex;
            gap: 5px;
        }

        .nav-tab {
            padding: 12px 20px;
            text-decoration: none;
            color: var(--gray);
            font-size: 14px;
            font-weight: 500;
            border-radius: 12px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            background: none;
            border: none;
            cursor: pointer;
        }

        .nav-tab:hover {
            background: #f8f9ff;
            color: var(--primary);
        }

        .nav-tab.active {
            background: var(--gradient);
            color: white;
            box-shadow: 0 5px 15px rgba(64, 93, 230, 0.3);
        }

        .admin-profile {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .profile-avatar {
            width: 40px;
            height: 40px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 18px;
        }

        /* Dashboard Content */
        .dashboard-content {
            padding: 30px;
        }

        .section {
            display: none;
            animation: fadeIn 0.3s ease;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }

        .section-title {
            font-size: 28px;
            font-weight: 700;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Stats Cards */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: white;
            border-radius: var(--radius);
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            display: flex;
            align-items: center;
            gap: 20px;
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-icon {
            width: 60px;
            height: 60px;
            background: var(--gradient);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
        }

        .stat-content h3 {
            font-size: 14px;
            color: var(--gray);
            margin-bottom: 5px;
        }

        .stat-number {
            font-size: 32px;
            font-weight: 800;
            color: var(--dark);
            margin-bottom: 5px;
        }

        /* Business Table */
        .data-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .data-table th {
            background: #f8f9ff;
            padding: 15px;
            text-align: left;
            font-weight: 600;
            color: var(--dark);
            font-size: 14px;
            border-bottom: 2px solid var(--border);
        }

        .data-table td {
            padding: 15px;
            font-size: 14px;
            color: var(--dark);
            border-bottom: 1px solid var(--border);
        }

        .data-table tr:hover {
            background: #f8f9ff;
        }

        .badge {
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            display: inline-block;
        }

        .badge-success {
            background: var(--success);
            color: white;
        }

        .badge-warning {
            background: var(--accent);
            color: var(--dark);
        }

        .badge-primary {
            background: var(--primary);
            color: white;
        }

        /* Payment Section */
        .payment-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .payment-stat {
            background: white;
            border-radius: var(--radius);
            padding: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .payment-stat h4 {
            font-size: 14px;
            color: var(--gray);
            margin-bottom: 10px;
        }

        .payment-stat .amount {
            font-size: 28px;
            font-weight: 800;
            color: var(--primary);
        }

        /* M-PESA Configuration */
        .mpesa-config {
            background: white;
            border-radius: var(--radius);
            padding: 30px;
            margin-top: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .config-item {
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border);
        }

        .config-item:last-child {
            border-bottom: none;
        }

        .config-label {
            font-weight: 600;
            color: var(--dark);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Settings */
        .settings-tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 30px;
            border-bottom: 1px solid var(--border);
            padding-bottom: 10px;
        }

        .settings-tab {
            padding: 10px 20px;
            background: none;
            border: none;
            color: var(--gray);
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .settings-tab.active {
            background: var(--primary);
            color: white;
        }

        .settings-content {
            display: none;
        }

        .settings-content.active {
            display: block;
        }

        /* Toast Notifications */
        .toast {
            position: fixed;
            top: 20px;
            right: 20px;
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: var(--shadow);
            display: none;
            align-items: center;
            gap: 15px;
            z-index: 10000;
            max-width: 400px;
            animation: slideIn 0.3s ease;
        }

        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        .toast-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: white;
        }

        .toast-success {
            border-left: 4px solid var(--success);
        }

        .toast-success .toast-icon {
            background: var(--success);
        }

        .toast-error {
            border-left: 4px solid var(--danger);
        }

        .toast-error .toast-icon {
            background: var(--danger);
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .dashboard-nav {
                padding: 0 15px;
                flex-direction: column;
                height: auto;
                padding: 15px;
            }

            .nav-tabs {
                flex-wrap: wrap;
                justify-content: center;
                margin: 15px 0;
            }

            .nav-tab {
                padding: 10px 15px;
                font-size: 13px;
            }

            .dashboard-content {
                padding: 15px;
            }

            .stats-grid {
                grid-template-columns: 1fr;
            }

            .section-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }

            .data-table {
                display: block;
                overflow-x: auto;
            }
        }

        @media (max-width: 480px) {
            .login-page {
                padding: 10px;
            }

            .login-card {
                margin: 10px;
            }

            .login-header {
                padding: 30px 20px;
            }

            .login-form {
                padding: 30px 20px;
            }

            .platform-name {
                font-size: 24px;
            }

            .logo-circle {
                width: 80px;
                height: 80px;
            }

            .logo-text {
                font-size: 36px;
            }

            .logo-circle .logo-text {
                font-size: 24px;
            }
        }
    </style>
</head>
<body>
    <div class="app-container">
        <!-- Login Page -->
        <div class="login-page" id="loginPage">
            <div class="login-card">
                <div class="login-header">
                    <div class="logo-main">
                        <div class="logo-circle">
                            <div class="logo-text">MN</div>
                        </div>
                        <div>
                            <h1 class="platform-name">Mwihoko<span style="background: var(--gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">Nitaa</span></h1>
                            <p class="domain">mwihokonimtaa.co.ke</p>
                            <p style="margin-top: 10px; font-size: 14px; opacity: 0.9;">HOPETOWNGRAM Admin Portal</p>
                        </div>
                    </div>
                </div>
                
                <div class="login-form">
                    <h2 style="margin-bottom: 5px; color: var(--dark);"><i class="fas fa-user-shield"></i> Admin Login</h2>
                    <p style="color: var(--gray); margin-bottom: 25px; font-size: 14px;">Access the platform control panel</p>
                    
                    <div class="form-group">
                        <label class="form-label"><i class="fas fa-user"></i> Username</label>
                        <input type="text" class="form-input" id="adminUsername" value="ADMIN HOPETOWNGRAM" readonly>
                    </div>
                    
                    <div class="form-group">
                        <label class="form-label"><i class="fas fa-lock"></i> Password</label>
                        <div class="password-container">
                            <input type="password" class="form-input" id="adminPassword" placeholder="Enter admin password">
                            <button type="button" class="password-toggle" onclick="togglePassword()">
                                <i class="fas fa-eye"></i>
                            </button>
                        </div>
                        <p style="margin-top: 8px; font-size: 12px; color: var(--gray);">
                            <i class="fas fa-info-circle"></i> Default password: <code>622417@Nywila</code>
                        </p>
                    </div>
                    
                    <div class="form-group">
                        <label class="form-label"><i class="fas fa-phone"></i> Admin Phone</label>
                        <input type="text" class="form-input" value="+254745794070" readonly>
                    </div>
                    
                    <button class="btn btn-primary btn-block" onclick="adminLogin()" style="margin-top: 10px;">
                        <i class="fas fa-sign-in-alt"></i> Login to Dashboard
                    </button>
                    
                    <div class="login-info">
                        <h4 style="color: var(--primary); margin-bottom: 10px; display: flex; align-items: center; gap: 10px;">
                            <i class="fas fa-mobile-alt"></i> M-PESA Configuration
                        </h4>
                        <p style="font-size: 14px; margin-bottom: 5px;"><strong>LIPA NA MPESA</strong> → <strong>POCHI LA BIASHARA</strong> → <strong>0745794070</strong></p>
                        <div class="mpesa-format">
                            LIPA NA MPESA-POCHI LA BIASHARA-0745794070-AMOUNT PIN
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Dashboard Page -->
        <div class="dashboard-page" id="dashboardPage">
            <!-- Top Navigation -->
            <nav class="dashboard-nav">
                <div class="nav-brand">
                    <div class="nav-brand-circle">MN</div>
                    <div>
                        <h3 style="font-size: 18px; font-weight: 700;">Mwihoko<span style="background: var(--gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">Nitaa</span></h3>
                        <p style="font-size: 11px; color: var(--gray);">mwihokonimtaa.co.ke</p>
                    </div>
                </div>
                
                <div class="nav-tabs">
                    <button class="nav-tab active" onclick="showSection('overview')">
                        <i class="fas fa-tachometer-alt"></i> Overview
                    </button>
                    <button class="nav-tab" onclick="showSection('businesses')">
                        <i class="fas fa-store"></i> Businesses
                    </button>
                    <button class="nav-tab" onclick="showSection('payments')">
                        <i class="fas fa-money-bill-wave"></i> Payments
                    </button>
                    <button class="nav-tab" onclick="showSection('mpesa')">
                        <i class="fas fa-mobile-alt"></i> M-PESA
                    </button>
                    <button class="nav-tab" onclick="showSection('settings')">
                        <i class="fas fa-cog"></i> Settings
                    </button>
                </div>
                
                <div class="admin-profile">
                    <div class="profile-avatar">
                        <i class="fas fa-crown"></i>
                    </div>
                    <div>
                        <p style="font-weight: 600; font-size: 14px;">ADMIN HOPETOWNGRAM</p>
                        <p style="font-size: 12px; color: var(--gray);">Super Admin</p>
                    </div>
                    <button class="btn" onclick="adminLogout()" style="margin-left: 10px; background: #f8f9ff; color: var(--primary);">
                        <i class="fas fa-sign-out-alt"></i>
                    </button>
                </div>
            </nav>

            <!-- Dashboard Content -->
            <div class="dashboard-content">
                <!-- Overview Section -->
                <section class="section active" id="overviewSection">
                    <div class="section-header">
                        <h1 class="section-title"><i class="fas fa-tachometer-alt"></i> Dashboard Overview</h1>
                        <p style="color: var(--gray); font-size: 14px;" id="currentTime">Loading...</p>
                    </div>
                    
                    <div class="stats-grid">
                        <div class="stat-card">
                            <div class="stat-icon">
                                <i class="fas fa-users"></i>
                            </div>
                            <div class="stat-content">
                                <h3>Total Users</h3>
                                <div class="stat-number" id="totalUsers">1,247</div>
                                <p style="font-size: 12px; color: var(--gray);">+12% this week</p>
                            </div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-icon">
                                <i class="fas fa-store"></i>
                            </div>
                            <div class="stat-content">
                                <h3>Businesses</h3>
                                <div class="stat-number" id="totalBusinesses">189</div>
                                <p style="font-size: 12px; color: var(--gray);">8 new today</p>
                            </div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-icon">
                                <i class="fas fa-money-bill-wave"></i>
                            </div>
                            <div class="stat-content">
                                <h3>Total Revenue</h3>
                                <div class="stat-number">KSH <span id="totalRevenue">247,500</span></div>
                                <p style="font-size: 12px; color: var(--gray);">KSH 15,000 today</p>
                            </div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-icon">
                                <i class="fas fa-chart-line"></i>
                            </div>
                            <div class="stat-content">
                                <h3>Active Posts</h3>
                                <div class="stat-number" id="activePosts">3,421</div>
                                <p style="font-size: 12px; color: var(--gray);">142 today</p>
                            </div>
                        </div>
                    </div>
                    
                    <div style="background: white; border-radius: var(--radius); padding: 30px; margin-bottom: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                        <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                            <i class="fas fa-chart-bar"></i> Revenue Analytics
                        </h3>
                        <div style="height: 300px; display: flex; align-items: center; justify-content: center; background: #f8f9ff; border-radius: 12px;">
                            <div style="text-align: center; color: var(--gray);">
                                <i class="fas fa-chart-line" style="font-size: 48px; margin-bottom: 20px; opacity: 0.5;"></i>
                                <p>Revenue chart would display here</p>
                                <p style="font-size: 12px; margin-top: 10px;">Last 7 days: KSH 85,000</p>
                            </div>
                        </div>
                    </div>
                    
                    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
                        <div style="background: white; border-radius: var(--radius); padding: 25px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                            <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; justify-content: space-between;">
                                <span style="display: flex; align-items: center; gap: 10px;">
                                    <i class="fas fa-user-check"></i> Pending Verifications
                                </span>
                                <span class="badge badge-warning">12</span>
                            </h3>
                            <div id="pendingList">
                                <!-- Will be populated by JavaScript -->
                            </div>
                        </div>
                        
                        <div style="background: white; border-radius: var(--radius); padding: 25px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                            <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                <i class="fas fa-mobile-alt"></i> M-PESA Status
                            </h3>
                            <div>
                                <div style="display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid var(--border);">
                                    <span>API Status</span>
                                    <span style="color: var(--success); font-weight: 600;">
                                        <i class="fas fa-circle" style="font-size: 10px;"></i> Active
                                    </span>
                                </div>
                                <div style="display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid var(--border);">
                                    <span>Today's Transactions</span>
                                    <span style="font-weight: 600;">24</span>
                                </div>
                                <div style="display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid var(--border);">
                                    <span>Today's Revenue</span>
                                    <span style="font-weight: 600;">KSH 15,000</span>
                                </div>
                                <div style="display: flex; justify-content: space-between; padding: 10px 0;">
                                    <span>Business Number</span>
                                    <span style="font-weight: 600; color: var(--primary);">0745794070</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Businesses Section -->
                <section class="section" id="businessesSection">
                    <div class="section-header">
                        <h1 class="section-title"><i class="fas fa-store"></i> Business Management</h1>
                        <button class="btn btn-primary" onclick="addNewBusiness()">
                            <i class="fas fa-plus"></i> Add Business
                        </button>
                    </div>
                    
                    <div style="display: flex; gap: 15px; margin-bottom: 20px;">
                        <div style="flex: 1; position: relative;">
                            <i class="fas fa-search" style="position: absolute; left: 15px; top: 50%; transform: translateY(-50%); color: var(--gray);"></i>
                            <input type="text" class="form-input" placeholder="Search businesses..." style="padding-left: 45px;" id="businessSearch" oninput="filterBusinesses()">
                        </div>
                        <select class="form-input" style="width: 200px;" id="statusFilter" onchange="filterBusinesses()">
                            <option value="all">All Status</option>
                            <option value="verified">Verified</option>
                            <option value="pending">Pending</option>
                        </select>
                    </div>
                    
                    <div style="overflow-x: auto;">
                        <table class="data-table">
                            <thead>
                                <tr>
                                    <th>Business Name</th>
                                    <th>Owner</th>
                                    <th>Category</th>
                                    <th>Status</th>
                                    <th>Payment</th>
                                    <th>Date</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="businessTable">
                                <!-- Will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </section>

                <!-- Payments Section -->
                <section class="section" id="paymentsSection">
                    <div class="section-header">
                        <h1 class="section-title"><i class="fas fa-money-bill-wave"></i> Payment Management</h1>
                        <button class="btn btn-primary" onclick="exportPayments()">
                            <i class="fas fa-download"></i> Export
                        </button>
                    </div>
                    
                    <div class="payment-stats">
                        <div class="payment-stat">
                            <h4>Total Revenue</h4>
                            <div class="amount">KSH 247,500</div>
                        </div>
                        <div class="payment-stat">
                            <h4>This Month</h4>
                            <div class="amount">KSH 45,000</div>
                        </div>
                        <div class="payment-stat">
                            <h4>Today</h4>
                            <div class="amount">KSH 15,000</div>
                        </div>
                        <div class="payment-stat">
                            <h4>Pending</h4>
                            <div class="amount">KSH 3,500</div>
                        </div>
                    </div>
                    
                    <div style="overflow-x: auto;">
                        <table class="data-table">
                            <thead>
                                <tr>
                                    <th>Transaction ID</th>
                                    <th>Business</th>
                                    <th>Type</th>
                                    <th>Amount</th>
                                    <th>Phone</th>
                                    <th>Status</th>
                                    <th>Date</th>
                                    <th>Receipt</th>
                                </tr>
                            </thead>
                            <tbody id="paymentTable">
                                <!-- Will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                    
                    <div class="mpesa-config">
                        <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                            <i class="fas fa-info-circle"></i> M-PESA Payment Instructions
                        </h3>
                        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-bottom: 20px;">
                            <div>
                                <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; font-weight: 700; margin-bottom: 10px;">1</div>
                                <p style="font-size: 14px;">Go to <strong>LIPA NA M-PESA</strong></p>
                            </div>
                            <div>
                                <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; font-weight: 700; margin-bottom: 10px;">2</div>
                                <p style="font-size: 14px;">Select <strong>POCHI LA BIASHARA</strong></p>
                            </div>
                            <div>
                                <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; font-weight: 700; margin-bottom: 10px;">3</div>
                                <p style="font-size: 14px;">Enter: <strong>0745794070</strong></p>
                            </div>
                            <div>
                                <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; font-weight: 700; margin-bottom: 10px;">4</div>
                                <p style="font-size: 14px;">Enter Amount & PIN</p>
                            </div>
                        </div>
                        <div style="background: #f8f9ff; padding: 15px; border-radius: 12px; border-left: 4px solid var(--primary);">
                            <h4 style="color: var(--primary); margin-bottom: 10px; font-size: 14px;">API Format:</h4>
                            <code style="font-family: monospace; font-size: 13px; color: var(--primary);">
                                LIPA NA MPESA-POCHI LA BIASHARA-0745794070-AMOUNT PIN
                            </code>
                        </div>
                    </div>
                </section>

                <!-- M-PESA Section -->
                <section class="section" id="mpesaSection">
                    <div class="section-header">
                        <h1 class="section-title"><i class="fas fa-mobile-alt"></i> M-PESA Integration</h1>
                        <button class="btn btn-primary" onclick="testMpesaAPI()">
                            <i class="fas fa-bolt"></i> Test Connection
                        </button>
                    </div>
                    
                    <div class="mpesa-config">
                        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin-bottom: 30px;">
                            <div>
                                <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                    <i class="fas fa-cog"></i> API Configuration
                                </h3>
                                <div class="form-group">
                                    <label class="form-label">Business Short Code</label>
                                    <input type="text" class="form-input" value="174379" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">POCHI LA BIASHARA Number</label>
                                    <input type="text" class="form-input" value="0745794070" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">API Key</label>
                                    <div class="password-container">
                                        <input type="password" class="form-input" value="mpesa_api_key_2024" readonly id="apiKey">
                                        <button type="button" class="password-toggle" onclick="toggleField('apiKey')">
                                            <i class="fas fa-eye"></i>
                                        </button>
                                    </div>
                                </div>
                                <button class="btn btn-primary" onclick="saveMpesaConfig()" style="margin-top: 10px;">
                                    <i class="fas fa-save"></i> Save Configuration
                                </button>
                            </div>
                            
                            <div>
                                <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                    <i class="fas fa-exchange-alt"></i> Transaction Flow
                                </h3>
                                <div style="display: flex; flex-direction: column; gap: 15px;">
                                    <div style="display: flex; align-items: center; gap: 15px;">
                                        <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 12px; display: flex; align-items: center; justify-content: center; color: white; flex-shrink: 0;">
                                            <i class="fas fa-user"></i>
                                        </div>
                                        <div>
                                            <p style="font-weight: 600; font-size: 14px;">Customer Initiation</p>
                                            <p style="font-size: 12px; color: var(--gray);">Select LIPA NA MPESA</p>
                                        </div>
                                    </div>
                                    <div style="display: flex; align-items: center; gap: 15px;">
                                        <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 12px; display: flex; align-items: center; justify-content: center; color: white; flex-shrink: 0;">
                                            <i class="fas fa-building"></i>
                                        </div>
                                        <div>
                                            <p style="font-weight: 600; font-size: 14px;">POCHI LA BIASHARA</p>
                                            <p style="font-size: 12px; color: var(--gray);">Select option</p>
                                        </div>
                                    </div>
                                    <div style="display: flex; align-items: center; gap: 15px;">
                                        <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 12px; display: flex; align-items: center; justify-content: center; color: white; flex-shrink: 0;">
                                            <i class="fas fa-phone"></i>
                                        </div>
                                        <div>
                                            <p style="font-weight: 600; font-size: 14px;">Enter Number</p>
                                            <p style="font-size: 12px; color: var(--gray);">Input: 0745794070</p>
                                        </div>
                                    </div>
                                    <div style="display: flex; align-items: center; gap: 15px;">
                                        <div style="width: 40px; height: 40px; background: var(--gradient); border-radius: 12px; display: flex; align-items: center; justify-content: center; color: white; flex-shrink: 0;">
                                            <i class="fas fa-money-bill"></i>
                                        </div>
                                        <div>
                                            <p style="font-weight: 600; font-size: 14px;">Amount & PIN</p>
                                            <p style="font-size: 12px; color: var(--gray);">Complete payment</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <h3 style="margin-bottom: 20px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                            <i class="fas fa-code"></i> API Request Format
                        </h3>
                        <div style="background: #1e1e1e; border-radius: 12px; padding: 20px; overflow-x: auto;">
                            <pre style="color: #d4d4d4; font-family: 'Courier New', monospace; font-size: 13px; line-height: 1.5; margin: 0;">
POST https://api.safaricom.co.ke/mpesa/stkpush/v1/processrequest
{
  "BusinessShortCode": "174379",
  "Password": "MTc0Mzc5YmZiMjc5ZjlhYTliZGJjZjE1OGU5N2RkNzFhNDY3Y2QyZTBjODkzMDU5YjEwZjc4ZTZiNzJhZGExZWQyYzkxOTIwMjQxMjI2MTIzMDM3",
  "Timestamp": "20241226123037",
  "TransactionType": "CustomerPayBillOnline",
  "Amount": "500",
  "PartyA": "254745794070",
  "PartyB": "174379",
  "PhoneNumber": "254745794070",
  "CallBackURL": "https://mwihokonimtaa.co.ke/api/mpesa-callback",
  "AccountReference": "HOPETOWNGRAM",
  "TransactionDesc": "POCHI LA BIASHARA Payment"
}</pre>
                        </div>
                    </div>
                </section>

                <!-- Settings Section -->
                <section class="section" id="settingsSection">
                    <div class="section-header">
                        <h1 class="section-title"><i class="fas fa-cog"></i> Platform Settings</h1>
                    </div>
                    
                    <div class="settings-tabs">
                        <button class="settings-tab active" onclick="showSettingsTab('general')">General</button>
                        <button class="settings-tab" onclick="showSettingsTab('security')">Security</button>
                        <button class="settings-tab" onclick="showSettingsTab('payment')">Payment</button>
                    </div>
                    
                    <div class="settings-content active" id="generalTab">
                        <div style="background: white; border-radius: var(--radius); padding: 30px; margin-top: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                            <h3 style="margin-bottom: 25px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                <i class="fas fa-sliders-h"></i> General Settings
                            </h3>
                            <div class="form-group">
                                <label class="form-label">Platform Name</label>
                                <input type="text" class="form-input" value="HOPETOWNGRAM" id="platformName">
                            </div>
                            <div class="form-group">
                                <label class="form-label">Domain</label>
                                <input type="text" class="form-input" value="mwihokonimtaa.co.ke" readonly>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Admin Email</label>
                                <input type="email" class="form-input" value="admin@mwihokonimtaa.co.ke" id="adminEmail">
                            </div>
                            <div class="form-group">
                                <label class="form-label">Business Registration Fee</label>
                                <div style="display: flex;">
                                    <span style="padding: 14px 15px; background: #f8f9ff; border: 2px solid var(--border); border-right: none; border-radius: 12px 0 0 12px; color: var(--gray);">KSH</span>
                                    <input type="number" class="form-input" value="500" style="border-radius: 0 12px 12px 0;" id="registrationFee">
                                </div>
                            </div>
                            <button class="btn btn-primary" onclick="saveSettings()">
                                <i class="fas fa-save"></i> Save Changes
                            </button>
                        </div>
                    </div>
                    
                    <div class="settings-content" id="securityTab">
                        <div style="background: white; border-radius: var(--radius); padding: 30px; margin-top: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
                            <h3 style="margin-bottom: 25px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                <i class="fas fa-shield-alt"></i> Security Settings
                            </h3>
                            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">
                                <div style="background: #f8f9ff; padding: 20px; border-radius: 12px;">
                                    <h4 style="margin-bottom: 10px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                        <i class="fas fa-key"></i> Admin Password
                                    </h4>
                                    <p style="font-size: 14px; color: var(--gray); margin-bottom: 15px;">
                                        Current: <code>622417@Nywila</code>
                                    </p>
                                    <button class="btn" onclick="changePassword()" style="background: var(--success); color: white;">
                                        Change Password
                                    </button>
                                </div>
                                
                                <div style="background: #f8f9ff; padding: 20px; border-radius: 12px;">
                                    <h4 style="margin-bottom: 15px; color: var(--dark); display: flex; align-items: center; gap: 10px;">
                                        <i class="fas fa-user-lock"></i> Login Security
                                    </h4>
                                    <div style="display: flex; flex-direction: column; gap: 10px;">
                                        <label style="display: flex; align-items: center; gap: 10px; cursor: pointer;">
                                            <input type="checkbox" checked style="width: 18px; height: 18px;">
                                            <span style="font-size: 14px;">Require 2FA for admin</span>
                                        </label>
                                        <label style="display: flex; align-items: center; gap: 10px; cursor: pointer;">
                                            <input type="checkbox" checked style="width: 18px; height: 18px;">
                                            <span style="font-size: 14px;">Log all admin activities</span>
                                        </label>
                                        <label style="display: flex; align-items: center; gap: 10px; cursor: pointer;">
                                            <input type="checkbox" style="width: 18px; height: 18px;">
                                            <span style="font-size: 14px;">Auto-lock after 15 minutes</span>
                                        </label>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
            </div>
        </div>

        <!-- Toast Notification -->
        <div class="toast" id="toast">
            <div class="toast-icon">
                <i class="fas fa-check"></i>
            </div>
            <div>
                <h4 id="toastTitle">Success</h4>
                <p id="toastMessage">Operation completed successfully</p>
            </div>
            <button onclick="hideToast()" style="margin-left: auto; background: none; border: none; color: var(--gray); cursor: pointer;">
                <i class="fas fa-times"></i>
            </button>
        </div>
    </div>

    <script>
        // ===== APP DATA =====
        const mockBusinesses = [
            { id: 1, name: "Mwihoko Fresh Grocers", owner: "John Kamau", category: "Retail", status: "verified", payment: "paid", date: "2025-12-20" },
            { id: 2, name: "Choma Zone Restaurant", owner: "Peter Mwangi", category: "Food", status: "verified", payment: "paid", date: "2025-12-19" },
            { id: 3, name: "Green Fields Farm", owner: "Sarah Wambui", category: "Agriculture", status: "pending", payment: "paid", date: "2025-12-26" },
            { id: 4, name: "Tech Solutions Mwihoko", owner: "David Ochieng", category: "Services", status: "pending", payment: "paid", date: "2025-12-25" },
            { id: 5, name: "Mwihoko Hardware", owner: "James Otieno", category: "Services", status: "verified", payment: "paid", date: "2025-12-18" },
            { id: 6, name: "Mama Nthenya Kitchen", owner: "Nthenya Wambui", category: "Food", status: "pending", payment: "unpaid", date: "2025-12-24" }
        ];

        const mockPayments = [
            { id: "MPESA-001", business: "Choma Zone Restaurant", type: "Business Registration", amount: "500", phone: "254712345678", status: "completed", date: "2025-12-26", receipt: "RC123456" },
            { id: "MPESA-002", business: "Mwihoko Fresh Grocers", type: "Promotion", amount: "300", phone: "254723456789", status: "completed", date: "2025-12-25", receipt: "RC123457" },
            { id: "MPESA-003", business: "Green Fields Farm", type: "Business Registration", amount: "500", phone: "254734567890", status: "pending", date: "2025-12-26", receipt: "Pending" },
            { id: "MPESA-004", business: "Tech Solutions Mwihoko", type: "Business Registration", amount: "500", phone: "254745678901", status: "completed", date: "2025-12-25", receipt: "RC123458" },
            { id: "MPESA-005", business: "Mwihoko Hardware", type: "Promotion", amount: "500", phone: "254756789012", status: "completed", date: "2025-12-24", receipt: "RC123459" }
        ];

        const pendingVerifications = [
            { id: 1, name: "Green Fields Farm", category: "Agriculture", date: "Today" },
            { id: 2, name: "Tech Solutions Mwihoko", category: "Services", date: "Yesterday" },
            { id: 3, name: "Mama Nthenya Kitchen", category: "Food", date: "2 days ago" }
        ];

        // ===== APP STATE =====
        let currentAdmin = null;

        // ===== INITIALIZATION =====
        document.addEventListener('DOMContentLoaded', function() {
            updateCurrentTime();
            setInterval(updateCurrentTime, 60000);
            
            loadBusinesses();
            loadPayments();
            loadPendingVerifications();
            
            // Auto-fill password for demo (remove in production)
            setTimeout(() => {
                document.getElementById('adminPassword').value = "622417@Nywila";
            }, 500);
        });

        // ===== TIME FUNCTIONS =====
        function updateCurrentTime() {
            const now = new Date();
            const options = { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric',
                hour: '2-digit',
                minute: '2-digit'
            };
            document.getElementById('currentTime').textContent = now.toLocaleDateString('en-US', options);
        }

        // ===== AUTH FUNCTIONS =====
        function togglePassword() {
            const passwordField = document.getElementById('adminPassword');
            const icon = document.querySelector('.password-toggle i');
            
            if (passwordField.type === 'password') {
                passwordField.type = 'text';
                icon.classList.remove('fa-eye');
                icon.classList.add('fa-eye-slash');
            } else {
                passwordField.type = 'password';
                icon.classList.remove('fa-eye-slash');
                icon.classList.add('fa-eye');
            }
        }

        function toggleField(fieldId) {
            const field = document.getElementById(fieldId);
            const icon = event.currentTarget.querySelector('i');
            
            if (field.type === 'password') {
                field.type = 'text';
                icon.classList.remove('fa-eye');
                icon.classList.add('fa-eye-slash');
            } else {
                field.type = 'password';
                icon.classList.remove('fa-eye-slash');
                icon.classList.add('fa-eye');
            }
        }

        function adminLogin() {
            const password = document.getElementById('adminPassword').value;
            const correctPassword = "622417@Nywila";
            
            if (password === correctPassword) {
                currentAdmin = {
                    name: "ADMIN HOPETOWNGRAM",
                    phone: "+254745794070",
                    lastLogin: new Date()
                };
                
                showToast("Login Successful", "Welcome to HOPETOWNGRAM Dashboard", "success");
                
                // Switch to dashboard
                document.getElementById('loginPage').style.display = 'none';
                document.getElementById('dashboardPage').style.display = 'block';
                
                // Log activity
                logActivity("admin_login", "Admin logged into dashboard");
                
            } else {
                showToast("Login Failed", "Invalid password. Please try again.", "error");
                document.getElementById('adminPassword').focus();
            }
        }

        function adminLogout() {
            if (confirm('Are you sure you want to logout?')) {
                currentAdmin = null;
                document.getElementById('adminPassword').value = '';
                
                document.getElementById('dashboardPage').style.display = 'none';
                document.getElementById('loginPage').style.display = 'flex';
                
                showToast("Logged Out", "You have been logged out successfully.", "success");
                logActivity("admin_logout", "Admin logged out");
            }
        }

        // ===== DASHBOARD FUNCTIONS =====
        function showSection(sectionId) {
            // Hide all sections
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Remove active class from all tabs
            document.querySelectorAll('.nav-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById(sectionId + 'Section').classList.add('active');
            
            // Add active class to clicked tab
            event.currentTarget.classList.add('active');
        }

        function showSettingsTab(tabId) {
            // Hide all settings tabs
            document.querySelectorAll('.settings-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Remove active class from all tab buttons
            document.querySelectorAll('.settings-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Show selected tab
            document.getElementById(tabId + 'Tab').classList.add('active');
            
            // Add active class to clicked tab button
            event.currentTarget.classList.add('active');
        }

        // ===== DATA LOADING =====
        function loadBusinesses() {
            const table = document.getElementById('businessTable');
            if (!table) return;
            
            table.innerHTML = '';
            
            mockBusinesses.forEach(business => {
                const statusBadge = business.status === 'verified' 
                    ? '<span class="badge badge-success">Verified</span>'
                    : '<span class="badge badge-warning">Pending</span>';
                
                const paymentBadge = business.payment === 'paid'
                    ? '<span class="badge badge-primary">Paid</span>'
                    : '<span class="badge badge-warning">Unpaid</span>';
                
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${business.name}</td>
                    <td>${business.owner}</td>
                    <td>${business.category}</td>
                    <td>${statusBadge}</td>
                    <td>${paymentBadge}</td>
                    <td>${business.date}</td>
                    <td>
                        <button class="btn" onclick="viewBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--primary); margin-right: 5px;">
                            <i class="fas fa-eye"></i>
                        </button>
                        <button class="btn" onclick="editBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--accent); margin-right: 5px;">
                            <i class="fas fa-edit"></i>
                        </button>
                        <button class="btn" onclick="deleteBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--danger);">
                            <i class="fas fa-trash"></i>
                        </button>
                    </td>
                `;
                table.appendChild(row);
            });
        }

        function loadPayments() {
            const table = document.getElementById('paymentTable');
            if (!table) return;
            
            table.innerHTML = '';
            
            mockPayments.forEach(payment => {
                const statusBadge = payment.status === 'completed'
                    ? '<span class="badge badge-success">Completed</span>'
                    : '<span class="badge badge-warning">Pending</span>';
                
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${payment.id}</td>
                    <td>${payment.business}</td>
                    <td>${payment.type}</td>
                    <td>KSH ${payment.amount}</td>
                    <td>${payment.phone}</td>
                    <td>${statusBadge}</td>
                    <td>${payment.date}</td>
                    <td>
                        <button class="btn" onclick="viewReceipt('${payment.receipt}')" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--primary);">
                            <i class="fas fa-receipt"></i> ${payment.receipt}
                        </button>
                    </td>
                `;
                table.appendChild(row);
            });
        }

        function loadPendingVerifications() {
            const container = document.getElementById('pendingList');
            if (!container) return;
            
            container.innerHTML = '';
            
            pendingVerifications.forEach(item => {
                const div = document.createElement('div');
                div.style.cssText = 'display: flex; justify-content: space-between; align-items: center; padding: 12px 0; border-bottom: 1px solid var(--border);';
                div.innerHTML = `
                    <div>
                        <p style="font-weight: 600; font-size: 14px;">${item.name}</p>
                        <p style="font-size: 12px; color: var(--gray);">${item.category} • ${item.date}</p>
                    </div>
                    <div style="display: flex; gap: 5px;">
                        <button class="btn" onclick="verifyBusiness(${item.id})" style="padding: 6px 12px; font-size: 12px; background: var(--success); color: white;">
                            <i class="fas fa-check"></i>
                        </button>
                        <button class="btn" onclick="rejectBusiness(${item.id})" style="padding: 6px 12px; font-size: 12px; background: var(--danger); color: white;">
                            <i class="fas fa-times"></i>
                        </button>
                    </div>
                `;
                container.appendChild(div);
            });
        }

        // ===== BUSINESS FUNCTIONS =====
        function filterBusinesses() {
            const searchTerm = document.getElementById('businessSearch').value.toLowerCase();
            const statusFilter = document.getElementById('statusFilter').value;
            
            const filtered = mockBusinesses.filter(business => {
                const matchesSearch = business.name.toLowerCase().includes(searchTerm) || 
                                     business.owner.toLowerCase().includes(searchTerm);
                const matchesStatus = statusFilter === 'all' || business.status === statusFilter;
                
                return matchesSearch && matchesStatus;
            });
            
            const table = document.getElementById('businessTable');
            if (!table) return;
            
            table.innerHTML = '';
            
            filtered.forEach(business => {
                const statusBadge = business.status === 'verified' 
                    ? '<span class="badge badge-success">Verified</span>'
                    : '<span class="badge badge-warning">Pending</span>';
                
                const paymentBadge = business.payment === 'paid'
                    ? '<span class="badge badge-primary">Paid</span>'
                    : '<span class="badge badge-warning">Unpaid</span>';
                
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${business.name}</td>
                    <td>${business.owner}</td>
                    <td>${business.category}</td>
                    <td>${statusBadge}</td>
                    <td>${paymentBadge}</td>
                    <td>${business.date}</td>
                    <td>
                        <button class="btn" onclick="viewBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--primary); margin-right: 5px;">
                            <i class="fas fa-eye"></i>
                        </button>
                        <button class="btn" onclick="editBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--accent); margin-right: 5px;">
                            <i class="fas fa-edit"></i>
                        </button>
                        <button class="btn" onclick="deleteBusiness(${business.id})" style="padding: 6px 12px; font-size: 12px; background: #f8f9ff; color: var(--danger);">
                            <i class="fas fa-trash"></i>
                        </button>
                    </td>
                `;
                table.appendChild(row);
            });
        }

        function addNewBusiness() {
            showToast("New Business", "Opening business registration form...", "success");
            logActivity("new_business", "Started new business registration");
        }

        function viewBusiness(id) {
            showToast("View Business", `Viewing business #${id} details`, "success");
            logActivity("view_business", `Viewed business ID ${id}`);
        }

        function editBusiness(id) {
            showToast("Edit Business", `Editing business #${id}`, "success");
            logActivity("edit_business", `Started editing business ID ${id}`);
        }

        function deleteBusiness(id) {
            if (confirm('Are you sure you want to delete this business? This action cannot be undone.')) {
                showToast("Business Deleted", "Business has been removed successfully", "success");
                logActivity("delete_business", `Deleted business ID ${id}`);
            }
        }

        function verifyBusiness(id) {
            showToast("Business Verified", "Business has been verified successfully", "success");
            logActivity("verify_business", `Verified business ID ${id}`);
        }

        function rejectBusiness(id) {
            showToast("Business Rejected", "Business registration has been rejected", "error");
            logActivity("reject_business", `Rejected business ID ${id}`);
        }

        // ===== PAYMENT FUNCTIONS =====
        function exportPayments() {
            showToast("Export Complete", "Payment data exported successfully", "success");
            logActivity("export_payments", "Exported payment data to CSV");
        }

        function viewReceipt(receipt) {
            showToast("View Receipt", `Showing receipt: ${receipt}`, "success");
            logActivity("view_receipt", `Viewed receipt ${receipt}`);
        }

        // ===== M-PESA FUNCTIONS =====
        function testMpesaAPI() {
            showToast("Testing M-PESA API", "Testing connection to M-PESA API...", "success");
            setTimeout(() => {
                showToast("M-PESA API Test", "Connection test successful!", "success");
            }, 1500);
            logActivity("test_mpesa", "Tested M-PESA API connection");
        }

        function saveMpesaConfig() {
            showToast("Configuration Saved", "M-PESA settings saved successfully", "success");
            logActivity("save_mpesa_config", "Updated M-PESA configuration");
        }

        // ===== SETTINGS FUNCTIONS =====
        function saveSettings() {
            showToast("Settings Saved", "Platform settings updated successfully", "success");
            logActivity("save_settings", "Updated platform settings");
        }

        function changePassword() {
            const current = prompt("Enter current password:");
            if (current !== "622417@Nywila") {
                showToast("Error", "Current password is incorrect", "error");
                return;
            }
            
            const newPass = prompt("Enter new password:");
            const confirmPass = prompt("Confirm new password:");
            
            if (newPass === confirmPass) {
                showToast("Password Changed", "Admin password updated successfully", "success");
                logActivity("change_password", "Changed admin password");
            } else {
                showToast("Error", "Passwords do not match", "error");
            }
        }

        // ===== NOTIFICATION FUNCTIONS =====
        function showToast(title, message, type) {
            const toast = document.getElementById('toast');
            const toastTitle = document.getElementById('toastTitle');
            const toastMessage = document.getElementById('toastMessage');
            const toastIcon = toast.querySelector('.toast-icon i');
            
            // Set content
            toastTitle.textContent = title;
            toastMessage.textContent = message;
            
            // Set type
            toast.className = 'toast';
            toast.classList.add(`toast-${type}`);
            
            // Set icon
            if (type === 'success') {
                toastIcon.className = 'fas fa-check';
            } else if (type === 'error') {
                toastIcon.className = 'fas fa-times';
            } else {
                toastIcon.className = 'fas fa-info-circle';
            }
            
            // Show toast
            toast.style.display = 'flex';
            
            // Auto-hide after 5 seconds
            setTimeout(hideToast, 5000);
        }

        function hideToast() {
            document.getElementById('toast').style.display = 'none';
        }

        // ===== LOGGING =====
        function logActivity(action, details) {
            const timestamp = new Date().toLocaleString();
            console.log(`[${timestamp}] ${action}: ${details}`);
            // In production, send to backend
        }

        // ===== DEMO DATA UPDATES =====
        // Simulate real-time updates
        setInterval(() => {
            // Update user count
            const userCount = document.getElementById('totalUsers');
            if (userCount) {
                const current = parseInt(userCount.textContent);
                userCount.textContent = (current + Math.floor(Math.random() * 3)).toString();
            }
            
            // Update revenue
            const revenue = document.getElementById('totalRevenue');
            if (revenue) {
                const current = parseInt(revenue.textContent.replace(/,/g, ''));
                revenue.textContent = (current + Math.floor(Math.random() * 100)).toLocaleString();
            }
        }, 10000); // Update every 10 seconds
    </script>
</body>
</html>
