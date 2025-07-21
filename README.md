<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PembeYatırım - Profesyonel Yatırım Platformu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS kodu aynı kalacak, değişiklik yapılmadı */
        
         :root {
            --primary: #ff2d95;
            --secondary: #ff66b3;
            --light: #ffe6f2;
            --dark: #8a004c;
            --accent: #ffb3d9;
            --text: #333;
            --white: #fff;
            --success: #4CAF50;
            --warning: #FF9800;
            --danger: #f44336;
            --gray: #f8f9fa;
            --dark-gray: #6c757d;
            --platinum: #e5e4e2;
            --diamond: #b9f2ff;
            --vip: #ffd700;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #fff5f9, #ffe6f2);
            color: var(--text);
            min-height: 100vh;
            padding-bottom: 50px;
        }
        /* Header Styles */
        
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: var(--white);
            padding: 15px 5%;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .logo i {
            color: var(--light);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: all 0.3s;
            padding: 10px 15px;
            border-radius: 30px;
        }
        
        nav a:hover,
        nav a.active {
            background: rgba(255, 255, 255, 0.2);
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .balance {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .user-actions button {
            background: var(--white);
            color: var(--primary);
            border: none;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .user-actions button:hover {
            background: var(--light);
            transform: translateY(-2px);
        }
        /* Main Content */
        
        .container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
        }
        
        .dashboard {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin-bottom: 40px;
        }
        
        .card {
            background: var(--white);
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
        }
        
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--accent);
        }
        
        .card-title {
            color: var(--primary);
            font-size: 1.4rem;
            font-weight: 700;
        }
        
        .card-icon {
            background: var(--light);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.5rem;
        }
        
        .account-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        .detail-item {
            background: var(--light);
            padding: 15px;
            border-radius: 15px;
        }
        
        .detail-label {
            font-size: 0.9rem;
            color: var(--dark);
            margin-bottom: 5px;
        }
        
        .detail-value {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .actions {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .btn {
            flex: 1;
            padding: 12px;
            border-radius: 15px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .btn-primary {
            background: var(--primary);
            color: var(--white);
        }
        
        .btn-secondary {
            background: var(--accent);
            color: var(--dark);
        }
        
        .btn-danger {
            background: var(--danger);
            color: var(--white);
        }
        
        .btn:hover {
            opacity: 0.9;
            transform: scale(1.03);
        }
        /* Packages Section */
        
        .section-title {
            text-align: center;
            margin: 40px 0 30px;
            color: var(--primary);
            font-size: 2rem;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        .packages {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }
        
        .package {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            position: relative;
            border: 2px solid var(--accent);
        }
        
        .package:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border-color: var(--primary);
        }
        
        .package-header {
            color: var(--white);
            padding: 20px;
            text-align: center;
        }
        
        .package-name {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 5px;
        }
        
        .package-range {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .package-body {
            padding: 20px;
        }
        
        .package-feature {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            gap: 10px;
        }
        
        .package-feature i {
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .package-profit {
            text-align: center;
            font-size: 2rem;
            font-weight: 800;
            color: var(--success);
            margin: 20px 0;
        }
        
        .package-cta {
            display: block;
            width: 100%;
            padding: 12px;
            background: var(--primary);
            color: var(--white);
            border: none;
            border-radius: 15px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .package-cta:hover {
            background: var(--dark);
        }
        /* Bonus Section */
        
        .bonus-banner {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: var(--white);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .bonus-banner::before {
            content: '';
            position: absolute;
            top: -50px;
            right: -50px;
            width: 150px;
            height: 150px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        .bonus-banner::after {
            content: '';
            position: absolute;
            bottom: -30px;
            left: -30px;
            width: 100px;
            height: 100px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        .bonus-title {
            font-size: 2.2rem;
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
        }
        
        .bonus-amount {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 25px;
            position: relative;
            z-index: 2;
        }
        
        .bonus-description {
            max-width: 700px;
            margin: 0 auto 25px;
            font-size: 1.1rem;
            opacity: 0.9;
            position: relative;
            z-index: 2;
        }
        /* Footer & Social */
        
        footer {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: var(--white);
            padding: 30px 5%;
            margin-top: 50px;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .social-buttons {
            display: flex;
            gap: 15px;
        }
        
        .social-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--white);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .whatsapp-btn {
            background: #25D366;
            color: white;
        }
        
        .telegram-btn {
            background: #0088cc;
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            margin-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
        }
        /* Responsive Design */
        
        @media (max-width: 900px) {
            .dashboard {
                grid-template-columns: 1fr;
            }
            .account-details {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                gap: 10px;
            }
            nav a {
                padding: 8px 12px;
                font-size: 0.9rem;
            }
            .user-info {
                flex-direction: column;
                gap: 8px;
            }
            .bonus-banner {
                padding: 30px 20px;
            }
            .footer-content {
                flex-direction: column;
                gap: 25px;
            }
        }
        
        @media (max-width: 480px) {
            .header-container {
                flex-direction: column;
                gap: 15px;
            }
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            .actions {
                flex-direction: column;
            }
        }
        /* Auth Pages */
        
        .auth-container {
            display: flex;
            min-height: 100vh;
        }
        
        .auth-left {
            flex: 1;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 50px;
            color: var(--white);
        }
        
        .auth-left-content {
            max-width: 500px;
        }
        
        .auth-left h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .auth-left p {
            font-size: 1.1rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .auth-features {
            margin-top: 40px;
        }
        
        .auth-feature {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            gap: 15px;
        }
        
        .auth-feature i {
            font-size: 1.5rem;
            color: var(--accent);
        }
        
        .auth-right {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 50px;
            background-color: var(--white);
        }
        
        .auth-form-container {
            width: 100%;
            max-width: 400px;
        }
        
        .auth-logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-bottom: 30px;
        }
        
        .auth-logo i {
            font-size: 2rem;
            color: var(--primary);
        }
        
        .auth-logo span {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary);
        }
        
        .auth-form {
            width: 100%;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-group input {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid var(--accent);
            border-radius: 15px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus {
            border-color: var(--primary);
            outline: none;
        }
        
        .auth-btn {
            width: 100%;
            padding: 12px;
            border-radius: 15px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            background: var(--primary);
            color: var(--white);
            margin-top: 10px;
        }
        
        .auth-btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        .auth-footer {
            text-align: center;
            margin-top: 20px;
            color: var(--dark);
        }
        
        .auth-footer a {
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
        }
        
        .auth-footer a:hover {
            text-decoration: underline;
        }
        /* Transaction History */
        
        .transaction-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .transaction-table th,
        .transaction-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid var(--accent);
        }
        
        .transaction-table th {
            background-color: var(--light);
            color: var(--primary);
            font-weight: 600;
        }
        
        .transaction-table tr:hover {
            background-color: rgba(255, 179, 217, 0.1);
        }
        
        .status {
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        .status.success {
            background-color: rgba(76, 175, 80, 0.1);
            color: var(--success);
        }
        
        .status.pending {
            background-color: rgba(255, 152, 0, 0.1);
            color: var(--warning);
        }
        
        .status.rejected {
            background-color: rgba(244, 67, 54, 0.1);
            color: var(--danger);
        }
        /* Support Section */
        
        .support-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        .support-card {
            background: var(--white);
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
        }
        
        .support-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .support-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .support-title {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        /* Promosyonlar */
        
        .promo-section {
            margin: 50px 0;
        }
        
        .promo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .promo-card {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--white);
            border-radius: 20px;
            padding: 25px;
            position: relative;
            overflow: hidden;
            min-height: 200px;
        }
        
        .promo-card:nth-child(2) {
            background: linear-gradient(135deg, #ff6b6b, #ff8e8e);
        }
        
        .promo-card:nth-child(3) {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
        }
        
        .promo-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--white);
            color: var(--primary);
            padding: 5px 10px;
            border-radius: 15px;
            font-weight: 600;
        }
        
        .promo-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .promo-desc {
            margin-bottom: 20px;
            opacity: 0.9;
        }
        
        .promo-btn {
            background: var(--white);
            color: var(--primary);
            border: none;
            padding: 10px 20px;
            border-radius: 15px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .promo-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        /* Bank Account Modal */
        
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            overflow: auto;
        }
        
        .modal-content {
            background-color: var(--white);
            margin: 5% auto;
            padding: 30px;
            border-radius: 20px;
            width: 100%;
            max-width: 500px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .modal-header {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--accent);
        }
        
        .modal-title {
            color: var(--primary);
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .modal-close {
            position: absolute;
            right: 20px;
            top: 20px;
            font-size: 28px;
            font-weight: bold;
            color: var(--dark);
            cursor: pointer;
        }
        
        .modal-close:hover {
            color: var(--primary);
        }
        /* Investment Modal */
        
        .investment-modal-content {
            max-width: 600px;
        }
        
        .investment-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .investment-detail {
            background: var(--light);
            padding: 15px;
            border-radius: 15px;
        }
        
        .investment-label {
            font-size: 0.9rem;
            color: var(--dark);
            margin-bottom: 5px;
        }
        
        .investment-value {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary);
        }
        /* Error Messages */
        
        .error-message {
            color: var(--danger);
            font-size: 0.9rem;
            margin-top: 5px;
            display: none;
        }
        /* Loading Spinner */
        
        .spinner {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--white);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
        }
        /* Responsive Auth Pages */
        
        @media (max-width: 900px) {
            .auth-container {
                flex-direction: column;
            }
            .auth-left {
                padding: 30px;
            }
            .auth-right {
                padding: 30px;
            }
        }
        /* Deposit Info */
        
        .deposit-info {
            background: var(--light);
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
            text-align: center;
        }
        
        .iban-display {
            font-family: monospace;
            font-size: 1.2rem;
            padding: 10px;
            background: var(--white);
            border-radius: 10px;
            margin: 10px 0;
        }
        
        .note {
            font-size: 0.9rem;
            color: var(--dark-gray);
            margin-top: 10px;
        }
        /* Package Colors */
        
        .package-basic {
            background: linear-gradient(to right, var(--primary), var(--secondary));
        }
        
        .package-bronze {
            background: linear-gradient(to right, #cd7f32, #a67b5b);
        }
        
        .package-silver {
            background: linear-gradient(to right, #c0c0c0, #a9a9a9);
        }
        
        .package-gold {
            background: linear-gradient(to right, #ffd700, #daa520);
        }
        
        .package-platinum {
            background: linear-gradient(to right, #e5e4e2, #d3d3d3);
        }
        
        .package-diamond {
            background: linear-gradient(to right, #b9f2ff, #89cff0);
        }
        
        .package-vip {
            background: linear-gradient(to right, #ffd700, #ffa500);
        }
        /* Profit Animation */
        
        .profit-animation {
            animation: pulse 1.5s infinite;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            100% {
                transform: scale(1);
            }
        }
        /* Investment Status */
        
        .investment-status {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid var(--accent);
        }
        
        .status-item {
            text-align: center;
            flex: 1;
        }
        
        .status-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--success);
        }
        
        .status-label {
            font-size: 0.9rem;
            color: var(--dark-gray);
        }
        /* New Styles for Active Investment */
        
        .investment-info {
            background: var(--light);
            border-radius: 15px;
            padding: 15px;
            margin-top: 20px;
        }
        
        .investment-title {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .investment-progress {
            height: 10px;
            background: #e0e0e0;
            border-radius: 5px;
            overflow: hidden;
            margin: 10px 0;
        }
        
        .investment-progress-bar {
            height: 100%;
            background: var(--success);
            width: 0%;
            transition: width 0.5s;
        }
        /* Admin Panel */
        
        .admin-panel {
            background: var(--light);
            border-radius: 15px;
            padding: 20px;
            margin-top: 30px;
        }
        
        .admin-tabs {
            display: flex;
            border-bottom: 2px solid var(--accent);
            margin-bottom: 20px;
        }
        
        .admin-tab {
            padding: 10px 20px;
            cursor: pointer;
            font-weight: 600;
            color: var(--dark);
            border-bottom: 3px solid transparent;
        }
        
        .admin-tab.active {
            color: var(--primary);
            border-bottom-color: var(--primary);
        }
        
        .admin-content {
            display: none;
        }
        
        .admin-content.active {
            display: block;
        }
        
        .admin-table {
            width: 100%;
            border-collapse: collapse;
        }
        
        .admin-table th,
        .admin-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid var(--accent);
        }
        
        .admin-table th {
            background-color: var(--primary);
            color: white;
        }
        
        .admin-actions {
            display: flex;
            gap: 10px;
        }
        
        .admin-btn {
            padding: 5px 10px;
            border-radius: 5px;
            border: none;
            cursor: pointer;
            font-weight: 500;
        }
        
        .approve-btn {
            background: var(--success);
            color: white;
        }
        
        .reject-btn {
            background: var(--danger);
            color: white;
        }
        /* Notification */
        
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--success);
            color: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            display: none;
        }
        
        .notification.error {
            background: var(--danger);
        }
        /* Real-time update indicator */
        
        .real-time-indicator {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--primary);
            color: white;
            padding: 10px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .pulse {
            width: 10px;
            height: 10px;
            background: #4CAF50;
            border-radius: 50%;
            animation: pulse 1.5s infinite;
        }
    </style>
</head>

<body>
    <!-- Main App (shown when logged in) -->
    <div id="appContainer" style="display: none;">
        <!-- Header -->
        <header>
            <div class="header-container">
                <div class="logo">
                    <i class="fas fa-chart-line"></i>
                    <span>PembeYatırım</span>
                </div>

                <nav>
                    <ul>
                        <li><a href="#" class="active" data-page="home"><i class="fas fa-home"></i> Ana Sayfa</a></li>
                        <li><a href="#" data-page="deposit"><i class="fas fa-wallet"></i> Mevduat</a></li>
                        <li><a href="#" data-page="packages"><i class="fas fa-gift"></i> Paketler</a></li>
                        <li><a href="#" data-page="history"><i class="fas fa-history"></i> İşlem Geçmişi</a></li>
                        <li><a href="#" data-page="support"><i class="fas fa-headset"></i> Canlı Destek</a></li>
                        <li id="adminLink" style="display: none;"><a href="#" data-page="admin"><i class="fas fa-user-shield"></i> Admin</a></li>
                    </ul>
                </nav>

                <div class="user-info">
                    <div class="balance">
                        <i class="fas fa-coins"></i>
                        <span id="userBalance">0.00 TL</span>
                    </div>
                    <div class="user-actions">
                        <button id="logoutBtn"><i class="fas fa-sign-out-alt"></i> Çıkış</button>
                    </div>
                </div>
            </div>
        </header>

        <!-- Main Content -->
        <div class="container">
            <!-- Home Page -->
            <div id="homePage" class="page active">
                <!-- Dashboard -->
                <div class="dashboard">
                    <div class="card">
                        <div class="card-header">
                            <h2 class="card-title">Hesap Bilgilerim</h2>
                            <div class="card-icon">
                                <i class="fas fa-user"></i>
                            </div>
                        </div>
                        <div class="account-details">
                            <div class="detail-item">
                                <div class="detail-label">Müşteri Numarası</div>
                                <div class="detail-value" id="customerId">-</div>
                            </div>
                            <div class="detail-item">
                                <div class="detail-label">Toplam Bakiye</div>
                                <div class="detail-value" id="totalBalance">0.00 TL</div>
                            </div>
                            <div class="detail-item">
                                <div class="detail-label">Yatırılan Tutar</div>
                                <div class="detail-value" id="investedAmount">0.00 TL</div>
                            </div>
                            <div class="detail-item">
                                <div class="detail-label">Toplam Kâr</div>
                                <div class="detail-value" id="totalProfit">0.00 TL</div>
                            </div>
                        </div>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <h2 class="card-title">Hızlı İşlemler</h2>
                            <div class="card-icon">
                                <i class="fas fa-exchange-alt"></i>
                            </div>
                        </div>
                        <div class="actions">
                            <button class="btn btn-primary" id="depositBtn">
                                <i class="fas fa-plus-circle"></i> Para Yatır
                            </button>
                            <button class="btn btn-secondary" id="withdrawBtn">
                                <i class="fas fa-minus-circle"></i> Para Çek
                            </button>
                        </div>

                        <div class="card-header" style="margin-top: 20px; border-bottom: none;">
                            <h2 class="card-title">Banka Hesabım</h2>
                            <div class="card-icon">
                                <i class="fas fa-university"></i>
                            </div>
                        </div>
                        <div class="detail-item">
                            <div class="detail-label">Kayıtlı Banka Hesabı</div>
                            <div class="detail-value" id="bankAccount">-</div>
                        </div>
                        <div class="actions" style="margin-top: 20px;">
                            <button class="btn btn-secondary" id="changeBankBtn">
                                <i class="fas fa-edit"></i> Hesap Değiştir
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Bonus Banner -->
                <div class="bonus-banner" id="bonusBanner">
                    <h2 class="bonus-title">Yeni Üyelere Özel!</h2>
                    <div class="bonus-amount">500 TL Hediye Bakiye</div>
                    <p class="bonus-description">Hemen kaydolun, 500 TL hediye bakiyeniz hesabınıza yatırılsın. Yatırım yapmaya hemen başlayın ve kâr elde edin!</p>
                    <button class="btn btn-primary" id="registerPromoBtn" style="background: var(--white); color: var(--primary); padding: 12px 40px;">
                        HEMEN KAYDOL <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Active Investment -->
                <div class="card" id="activeInvestmentCard" style="display: none;">
                    <div class="card-header">
                        <h2 class="card-title">Aktif Yatırım</h2>
                        <div class="card-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                    </div>
                    <div class="investment-info">
                        <div class="investment-title" id="activePackageName">-</div>
                        <div class="investment-progress">
                            <div class="investment-progress-bar" id="investmentProgress"></div>
                        </div>
                        <div class="investment-details">
                            <div class="investment-detail">
                                <div class="investment-label">Kalan Süre</div>
                                <div class="investment-value" id="remainingTime">-</div>
                            </div>
                            <div class="investment-detail">
                                <div class="investment-label">Beklenen Kâr</div>
                                <div class="investment-value" id="expectedProfit">-</div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Packages Section -->
                <h2 class="section-title">Yatırım Paketleri</h2>
                <div class="packages">
                    <!-- Package 1 -->
                    <div class="package" data-package-id="1">
                        <div class="package-header package-basic">
                            <h3 class="package-name">Başlangıç Paketi</h3>
                            <div class="package-range">1,000 TL - 2,499 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-profit">%12</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 2 -->
                    <div class="package" data-package-id="2">
                        <div class="package-header package-bronze">
                            <h3 class="package-name">Bronz Paket</h3>
                            <div class="package-range">2,500 TL - 4,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-profit">%15</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 3 -->
                    <div class="package" data-package-id="3">
                        <div class="package-header package-silver">
                            <h3 class="package-name">Gümüş Paket</h3>
                            <div class="package-range">5,000 TL - 9,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Haftalık Analiz</span>
                            </div>
                            <div class="package-profit">%18</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 4 -->
                    <div class="package" data-package-id="4">
                        <div class="package-header package-gold">
                            <h3 class="package-name">Altın Paket</h3>
                            <div class="package-range">10,000 TL - 24,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Haftalık Analiz</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Risk Yönetimi</span>
                            </div>
                            <div class="package-profit">%22</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>
                </div>

                <!-- Promosyonlar -->
                <div class="promo-section">
                    <h2 class="section-title">Özel Promosyonlar</h2>
                    <div class="promo-grid">
                        <div class="promo-card">
                            <div class="promo-badge">Yeni</div>
                            <h3 class="promo-title">Uzun Vadeli Kazanç</h3>
                            <p class="promo-desc">6 ay ve üzeri yatırımlarda ekstra %3 kazanç fırsatı!</p>
                            <button class="promo-btn">Detaylı Bilgi</button>
                        </div>

                        <div class="promo-card">
                            <div class="promo-badge">Sınırlı</div>
                            <h3 class="promo-title">Arkadaşını Davet Et</h3>
                            <p class="promo-desc">Arkadaşınızı davet edin, her biri için 100 TL bonus kazanın!</p>
                            <button class="promo-btn">Hemen Davet Et</button>
                        </div>

                        <div class="promo-card">
                            <div class="promo-badge">Özel</div>
                            <h3 class="promo-title">VIP Müşteri Avantajları</h3>
                            <p class="promo-desc">50,000 TL üzeri yatırımcılar için özel VIP programı</p>
                            <button class="promo-btn">VIP Ol</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Deposit Page -->
            <div id="depositPage" class="page" style="display: none;">
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title">Para Yatırma İşlemleri</h2>
                        <div class="card-icon">
                            <i class="fas fa-coins"></i>
                        </div>
                    </div>

                    <div class="account-details">
                        <div class="detail-item">
                            <div class="detail-label">Mevcut Bakiye</div>
                            <div class="detail-value" id="depositBalance">0.00 TL</div>
                        </div>
                        <div class="detail-item">
                            <div class="detail-label">Kayıtlı Banka Hesabı</div>
                            <div class="detail-value" id="depositBankAccount">-</div>
                        </div>
                    </div>

                    <div class="form-group" style="margin-top: 20px;">
                        <label for="depositAmount">Yatırılacak Tutar (TL)</label>
                        <input type="number" id="depositAmount" placeholder="Örn: 1000">
                        <div class="error-message" id="depositError"></div>
                    </div>

                    <div class="actions">
                        <button class="btn btn-primary" id="confirmDeposit">
                            <i class="fas fa-check-circle"></i> Para Yatır
                        </button>
                    </div>

                    <div class="deposit-info">
                        <h3>Para Yatırma Bilgileri</h3>
                        <p>Aşağıdaki IBAN numarasına havale/EFT yaparak para yatırabilirsiniz:</p>
                        <div class="iban-display">TR60 0001 0014 3376 0929 5950 01</div>
                        <p class="note">Hesap Sahibi: Canan Atay</p>
                        <p class="note">İşlemleriniz en geç 30 dakika içinde hesabınıza yansıyacaktır.</p>
                    </div>
                </div>

                <div class="card" style="margin-top: 30px;">
                    <div class="card-header">
                        <h2 class="card-title">Para Çekme İşlemleri</h2>
                        <div class="card-icon">
                            <i class="fas fa-money-bill-wave"></i>
                        </div>
                    </div>

                    <div class="account-details">
                        <div class="detail-item">
                            <div class="detail-label">Çekilebilir Bakiye</div>
                            <div class="detail-value" id="withdrawBalance">0.00 TL</div>
                        </div>
                        <div class="detail-item">
                            <div class="detail-label">Kayıtlı Banka Hesabı</div>
                            <div class="detail-value" id="withdrawBankAccount">-</div>
                        </div>
                    </div>

                    <div class="form-group" style="margin-top: 20px;">
                        <label for="withdrawAmount">Çekilecek Tutar (TL)</label>
                        <input type="number" id="withdrawAmount" placeholder="Örn: 500">
                        <div class="error-message" id="withdrawError"></div>
                    </div>

                    <div class="actions">
                        <button class="btn btn-primary" id="confirmWithdraw">
                            <i class="fas fa-check-circle"></i> Para Çek
                        </button>
                    </div>

                    <div class="deposit-info">
                        <h3>Para Çekme Bilgileri</h3>
                        <p>Para çekme işlemleriniz 7/24 yapılabilir. İşlemleriniz 1 iş günü içinde tamamlanır.</p>
                        <p class="note">Para çekme işlemlerinde hiçbir komisyon alınmamaktadır.</p>
                    </div>
                </div>
            </div>

            <!-- Packages Page -->
            <div id="packagesPage" class="page" style="display: none;">
                <h2 class="section-title">Yatırım Paketleri</h2>
                <p style="text-align: center; margin-bottom: 30px; max-width: 800px; margin-left: auto; margin-right: auto;">
                    Yatırım paketlerimizle paranızı en iyi şekilde değerlendirin. Aşağıdaki paketlerden birini seçerek hemen yatırım yapmaya başlayabilirsiniz.
                </p>
                <div class="packages">
                    <!-- Package 1 -->
                    <div class="package" data-package-id="1">
                        <div class="package-header package-basic">
                            <h3 class="package-name">Başlangıç Paketi</h3>
                            <div class="package-range">1,000 TL - 2,499 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-profit">%12</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 2 -->
                    <div class="package" data-package-id="2">
                        <div class="package-header package-bronze">
                            <h3 class="package-name">Bronz Paket</h3>
                            <div class="package-range">2,500 TL - 4,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-profit">%15</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 3 -->
                    <div class="package" data-package-id="3">
                        <div class="package-header package-silver">
                            <h3 class="package-name">Gümüş Paket</h3>
                            <div class="package-range">5,000 TL - 9,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Haftalık Analiz</span>
                            </div>
                            <div class="package-profit">%18</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>

                    <!-- Package 4 -->
                    <div class="package" data-package-id="4">
                        <div class="package-header package-gold">
                            <h3 class="package-name">Altın Paket</h3>
                            <div class="package-range">10,000 TL - 24,999 TL</div>
                        </div>
                        <div class="package-body">
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Günlük Kâr</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>7/24 Destek</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Anlık İşlemler</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Özel Danışman</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Haftalık Analiz</span>
                            </div>
                            <div class="package-feature">
                                <i class="fas fa-check-circle"></i>
                                <span>Risk Yönetimi</span>
                            </div>
                            <div class="package-profit">%22</div>
                            <button class="package-cta invest-btn">Hemen Yatırım Yap</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- History Page -->
            <div id="historyPage" class="page" style="display: none;">
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title">İşlem Geçmişi</h2>
                        <div class="card-icon">
                            <i class="fas fa-history"></i>
                        </div>
                    </div>

                    <table class="transaction-table">
                        <thead>
                            <tr>
                                <th>Tarih</th>
                                <th>İşlem Türü</th>
                                <th>Tutar</th>
                                <th>Durum</th>
                                <th>Detay</th>
                            </tr>
                        </thead>
                        <tbody id="transactionHistory">
                            <!-- İşlem geçmişi buraya eklenecek -->
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- Support Page -->
            <div id="supportPage" class="page" style="display: none;">
                <h2 class="section-title">7/24 Canlı Destek</h2>
                <p style="text-align: center; margin-bottom: 40px; max-width: 800px; margin-left: auto; margin-right: auto;">
                    Her türlü soru, öneri ve şikayetleriniz için canlı destek ekibimiz 7/24 hizmetinizdedir.
                </p>

                <div class="support-container">
                    <div class="support-card">
                        <div class="support-icon">
                            <i class="fab fa-whatsapp"></i>
                        </div>
                        <h3 class="support-title">WhatsApp Destek</h3>
                        <p>Hemen WhatsApp üzerinden destek alın</p>
                        <button class="btn btn-primary" style="margin-top: 20px;">
                            <i class="fab fa-whatsapp"></i> WhatsApp'tan Yaz
                        </button>
                    </div>

                    <div class="support-card">
                        <div class="support-icon">
                            <i class="fab fa-telegram"></i>
                        </div>
                        <h3 class="support-title">Telegram Destek</h3>
                        <p>Telegram üzerinden anında destek alın</p>
                        <button class="btn btn-primary" style="margin-top: 20px; background: #0088cc;">
                            <i class="fab fa-telegram"></i> Telegram'dan Yaz
                        </button>
                    </div>
                </div>

                <div class="card" style="margin-top: 40px;">
                    <div class="card-header">
                        <h2 class="card-title">Sıkça Sorulan Sorular</h2>
                        <div class="card-icon">
                            <i class="fas fa-question-circle"></i>
                        </div>
                    </div>

                    <div class="package-body">
                        <div class="package-feature">
                            <i class="fas fa-question"></i>
                            <span>Yatırım yaptıktan sonra ne zaman kâr almaya başlarım?</span>
                        </div>
                        <div class="package-feature">
                            <i class="fas fa-question"></i>
                            <span>Para çekme işlemi ne kadar sürer?</span>
                        </div>
                        <div class="package-feature">
                            <i class="fas fa-question"></i>
                            <span>Yatırım paketimi nasıl değiştirebilirim?</span>
                        </div>
                        <div class="package-feature">
                            <i class="fas fa-question"></i>
                            <span>Hesabımı nasıl güvende tutabilirim?</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Admin Page -->
            <div id="adminPage" class="page" style="display: none;">
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title">Admin Paneli</h2>
                        <div class="card-icon">
                            <i class="fas fa-user-shield"></i>
                        </div>
                    </div>

                    <div class="admin-panel">
                        <div class="admin-tabs">
                            <div class="admin-tab active" data-tab="deposits">Para Yatırma Talepleri</div>
                            <div class="admin-tab" data-tab="withdrawals">Para Çekme Talepleri</div>
                            <div class="admin-tab" data-tab="investments">Yatırım Talepleri</div>
                            <div class="admin-tab" data-tab="users">Kullanıcılar</div>
                        </div>

                        <div id="depositsTab" class="admin-content active">
                            <table class="admin-table">
                                <thead>
                                    <tr>
                                        <th>ID</th>
                                        <th>Kullanıcı</th>
                                        <th>Tutar</th>
                                        <th>Tarih</th>
                                        <th>Durum</th>
                                        <th>İşlemler</th>
                                    </tr>
                                </thead>
                                <tbody id="depositRequests">
                                    <!-- Para yatırma talepleri buraya eklenecek -->
                                </tbody>
                            </table>
                        </div>

                        <div id="withdrawalsTab" class="admin-content">
                            <table class="admin-table">
                                <thead>
                                    <tr>
                                        <th>ID</th>
                                        <th>Kullanıcı</th>
                                        <th>Tutar</th>
                                        <th>Tarih</th>
                                        <th>Durum</th>
                                        <th>İşlemler</th>
                                    </tr>
                                </thead>
                                <tbody id="withdrawalRequests">
                                    <!-- Para çekme talepleri buraya eklenecek -->
                                </tbody>
                            </table>
                        </div>

                        <div id="investmentsTab" class="admin-content">
                            <table class="admin-table">
                                <thead>
                                    <tr>
                                        <th>ID</th>
                                        <th>Kullanıcı</th>
                                        <th>Paket</th>
                                        <th>Tutar</th>
                                        <th>Tarih</th>
                                        <th>Durum</th>
                                        <th>İşlemler</th>
                                    </tr>
                                </thead>
                                <tbody id="investmentRequests">
                                    <!-- Yatırım talepleri buraya eklenecek -->
                                </tbody>
                            </table>
                        </div>

                        <div id="usersTab" class="admin-content">
                            <table class="admin-table">
                                <thead>
                                    <tr>
                                        <th>ID</th>
                                        <th>Ad Soyad</th>
                                        <th>E-posta</th>
                                        <th>Telefon</th>
                                        <th>Bakiye</th>
                                        <th>Durum</th>
                                        <th>İşlemler</th>
                                    </tr>
                                </thead>
                                <tbody id="usersList">
                                    <!-- Kullanıcı listesi buraya eklenecek -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer>
            <div class="footer-content">
                <div class="footer-info">
                    <h3><i class="fas fa-chart-line"></i> PembeYatırım</h3>
                    <p>Profesyonel yatırım çözümleri ile finansal hedeflerinize ulaşın</p>
                </div>
                <div class="social-buttons">
                    <a href="#" class="social-btn whatsapp-btn">
                        <i class="fab fa-whatsapp"></i>
                    </a>
                    <a href="https://t.me/wotkaa771" class="social-btn telegram-btn">
                        <i class="fab fa-telegram"></i>
                    </a>
                    <a href="#" class="social-btn">
                        <i class="fas fa-headset"></i>
                    </a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 PembeYatırım A.Ş. Tüm hakları saklıdır.</p>
            </div>
        </footer>
    </div>

    <!-- Login Page -->
    <div id="loginPage" class="auth-container">
        <div class="auth-left">
            <div class="auth-left-content">
                <h1>PembeYatırım'a Hoş Geldiniz</h1>
                <p>Profesyonel yatırım çözümleri ile finansal hedeflerinize ulaşın. Yeni üyelerimize 500 TL hediye bakiye!</p>

                <div class="auth-features">
                    <div class="auth-feature">
                        <i class="fas fa-coins"></i>
                        <div>
                            <h3>Yüksek Getiri</h3>
                            <p>%12'ye varan günlük kazanç fırsatı</p>
                        </div>
                    </div>
                    <div class="auth-feature">
                        <i class="fas fa-shield-alt"></i>
                        <div>
                            <h3>Güvenli Yatırım</h3>
                            <p>Para güvenliğiniz bizim için önemli</p>
                        </div>
                    </div>
                    <div class="auth-feature">
                        <i class="fas fa-headset"></i>
                        <div>
                            <h3>7/24 Destek</h3>
                            <p>Her zaman yanınızdayız</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="auth-right">
            <div class="auth-form-container">
                <div class="auth-logo">
                    <i class="fas fa-chart-line"></i>
                    <span>PembeYatırım</span>
                </div>

                <form class="auth-form" id="loginForm">
                    <div class="form-group">
                        <label for="loginEmail">E-posta Adresi</label>
                        <input type="email" id="loginEmail" placeholder="ornek@email.com" required>
                        <div class="error-message" id="loginEmailError"></div>
                    </div>

                    <div class="form-group">
                        <label for="loginPassword">Şifre</label>
                        <input type="password" id="loginPassword" placeholder="Şifrenizi girin" required>
                        <div class="error-message" id="loginPasswordError"></div>
                    </div>

                    <button type="submit" class="auth-btn" id="loginSubmit">
                        <span id="loginBtnText">Giriş Yap</span>
                        <span id="loginSpinner" class="spinner" style="display: none;"></span>
                    </button>

                    <div class="auth-footer">
                        Hesabınız yok mu? <a href="#" id="showRegisterBtn">Hemen kaydolun</a>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Register Page -->
    <div id="registerPage" class="auth-container" style="display: none;">
        <div class="auth-left">
            <div class="auth-left-content">
                <h1>PembeYatırım'a Katılın</h1>
                <p>Hemen kaydolun ve 500 TL hediye bakiyenizi alarak yatırıma başlayın!</p>

                <div class="auth-features">
                    <div class="auth-feature">
                        <i class="fas fa-gift"></i>
                        <div>
                            <h3>500 TL Hediye</h3>
                            <p>Yeni üyelere özel hediye bakiye</p>
                        </div>
                    </div>
                    <div class="auth-feature">
                        <i class="fas fa-chart-line"></i>
                        <div>
                            <h3>Kazanç Garantisi</h3>
                            <p>%12'ye varan günlük kazanç</p>
                        </div>
                    </div>
                    <div class="auth-feature">
                        <i class="fas fa-lock"></i>
                        <div>
                            <h3>Güvenli</h3>
                            <p>Bankalar düzeyinde güvenlik</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="auth-right">
            <div class="auth-form-container">
                <div class="auth-logo">
                    <i class="fas fa-chart-line"></i>
                    <span>PembeYatırım</span>
                </div>

                <form class="auth-form" id="registerForm">
                    <div class="form-group">
                        <label for="registerName">Ad Soyad</label>
                        <input type="text" id="registerName" placeholder="Adınız soyadınız" required>
                        <div class="error-message" id="registerNameError"></div>
                    </div>

                    <div class="form-group">
                        <label for="registerEmail">E-posta Adresi</label>
                        <input type="email" id="registerEmail" placeholder="ornek@email.com" required>
                        <div class="error-message" id="registerEmailError"></div>
                    </div>

                    <div class="form-group">
                        <label for="registerPhone">Telefon Numarası</label>
                        <input type="tel" id="registerPhone" placeholder="05xx xxx xxxx" required>
                        <div class="error-message" id="registerPhoneError"></div>
                    </div>

                    <div class="form-group">
                        <label for="registerPassword">Şifre</label>
                        <input type="password" id="registerPassword" placeholder="Şifrenizi oluşturun" required>
                        <div class="error-message" id="registerPasswordError"></div>
                    </div>

                    <div class="form-group">
                        <label for="registerConfirmPassword">Şifre Tekrar</label>
                        <input type="password" id="registerConfirmPassword" placeholder="Şifrenizi tekrar girin" required>
                        <div class="error-message" id="registerConfirmPasswordError"></div>
                    </div>

                    <button type="submit" class="auth-btn" id="registerSubmit">
                        <span id="registerBtnText">Kayıt Ol</span>
                        <span id="registerSpinner" class="spinner" style="display: none;"></span>
                    </button>

                    <div class="auth-footer">
                        Zaten hesabınız var mı? <a href="#" id="showLoginBtn">Giriş yapın</a>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Bank Account Modal -->
    <div id="bankModal" class="modal">
        <div class="modal-content">
            <span class="modal-close">&times;</span>

            <div class="modal-header">
                <h2 class="modal-title">Banka Hesabı Ekle/Değiştir</h2>
            </div>

            <div class="form-group">
                <label for="bankName">Banka Adı</label>
                <input type="text" id="bankName" placeholder="Örn: Ziraat Bankası">
                <div class="error-message" id="bankNameError"></div>
            </div>

            <div class="form-group">
                <label for="ibanNumber">IBAN Numarası</label>
                <input type="text" id="ibanNumber" placeholder="TR00 0000 0000 0000 0000 0000 00">
                <div class="error-message" id="ibanError"></div>
            </div>

            <div class="form-group">
                <label for="accountHolder">Hesap Sahibi Adı</label>
                <input type="text" id="accountHolder" placeholder="Hesap sahibinin adı soyadı">
                <div class="error-message" id="accountHolderError"></div>
            </div>

            <button class="btn btn-primary" id="saveBankBtn" style="width: 100%;">
                <i class="fas fa-save"></i> Kaydet
            </button>
        </div>
    </div>

    <!-- Investment Modal -->
    <div id="investmentModal" class="modal">
        <div class="modal-content investment-modal-content">
            <span class="modal-close">&times;</span>

            <div class="modal-header">
                <h2 class="modal-title" id="investmentModalTitle">Yatırım Yap</h2>
            </div>

            <div class="investment-details">
                <div class="investment-detail">
                    <div class="investment-label">Paket Adı</div>
                    <div class="investment-value" id="modalPackageName">-</div>
                </div>
                <div class="investment-detail">
                    <div class="investment-label">Kâr Oranı</div>
                    <div class="investment-value" id="modalProfitRate">-</div>
                </div>
                <div class="investment-detail">
                    <div class="investment-label">Minimum Tutar</div>
                    <div class="investment-value" id="modalMinAmount">-</div>
                </div>
                <div class="investment-detail">
                    <div class="investment-label">Maksimum Tutar</div>
                    <div class="investment-value" id="modalMaxAmount">-</div>
                </div>
            </div>

            <div class="form-group">
                <label for="investmentAmount">Yatırım Tutarı (TL)</label>
                <input type="number" id="investmentAmount" placeholder="Yatırım yapmak istediğiniz tutar">
                <div class="error-message" id="investmentAmountError"></div>
            </div>

            <div class="actions">
                <button class="btn btn-primary" id="confirmInvestment">
                    <i class="fas fa-check-circle"></i> Yatırım Yap
                </button>
            </div>
        </div>
    </div>

    <!-- Notification -->
    <div id="notification" class="notification">
        <div id="notificationMessage"></div>
    </div>

    <!-- Real-time indicator -->
    <div id="realTimeIndicator" class="real-time-indicator" style="display: none;">
        <div class="pulse"></div>
        <span>Gerçek zamanlı güncelleniyor</span>
    </div>

    <script>
        // User data and state management
        const state = {
            currentUser: null,
            users: JSON.parse(localStorage.getItem('users')) || [],
            transactions: JSON.parse(localStorage.getItem('transactions')) || [],
            pendingDeposits: JSON.parse(localStorage.getItem('pendingDeposits')) || [],
            pendingWithdrawals: JSON.parse(localStorage.getItem('pendingWithdrawals')) || [],
            pendingInvestments: JSON.parse(localStorage.getItem('pendingInvestments')) || [],
            packages: [{
                id: 1,
                name: "Başlangıç Paketi",
                minAmount: 1000,
                maxAmount: 2499,
                profitRate: 12,
                features: [
                    "Günlük Kâr",
                    "7/24 Destek",
                    "Anlık İşlemler"
                ]
            }, {
                id: 2,
                name: "Bronz Paket",
                minAmount: 2500,
                maxAmount: 4999,
                profitRate: 15,
                features: [
                    "Günlük Kâr",
                    "7/24 Destek",
                    "Anlık İşlemler",
                    "Özel Danışman"
                ]
            }, {
                id: 3,
                name: "Gümüş Paket",
                minAmount: 5000,
                maxAmount: 9999,
                profitRate: 18,
                features: [
                    "Günlük Kâr",
                    "7/24 Destek",
                    "Anlık İşlemler",
                    "Özel Danışman",
                    "Haftalık Analiz"
                ]
            }, {
                id: 4,
                name: "Altın Paket",
                minAmount: 10000,
                maxAmount: 24999,
                profitRate: 22,
                features: [
                    "Günlük Kâr",
                    "7/24 Destek",
                    "Anlık İşlemler",
                    "Özel Danışman",
                    "Haftalık Analiz",
                    "Risk Yönetimi"
                ]
            }],
            currentPackage: null,
            activeInvestment: null,
            adminUsers: ['admin@pembeyatirim.com'], // Admin e-posta listesi
            realTimeUpdates: false
        };

        // DOM Elements
        const appContainer = document.getElementById('appContainer');
        const loginPage = document.getElementById('loginPage');
        const registerPage = document.getElementById('registerPage');
        const bonusBanner = document.getElementById('bonusBanner');
        const activeInvestmentCard = document.getElementById('activeInvestmentCard');
        const activePackageName = document.getElementById('activePackageName');
        const investmentProgress = document.getElementById('investmentProgress');
        const remainingTime = document.getElementById('remainingTime');
        const expectedProfit = document.getElementById('expectedProfit');
        const adminLink = document.getElementById('adminLink');

        // Login Page Elements
        const loginForm = document.getElementById('loginForm');
        const loginEmail = document.getElementById('loginEmail');
        const loginPassword = document.getElementById('loginPassword');
        const loginSubmit = document.getElementById('loginSubmit');
        const loginBtnText = document.getElementById('loginBtnText');
        const loginSpinner = document.getElementById('loginSpinner');
        const showRegisterBtn = document.getElementById('showRegisterBtn');

        // Register Page Elements
        const registerForm = document.getElementById('registerForm');
        const registerName = document.getElementById('registerName');
        const registerEmail = document.getElementById('registerEmail');
        const registerPhone = document.getElementById('registerPhone');
        const registerPassword = document.getElementById('registerPassword');
        const registerConfirmPassword = document.getElementById('registerConfirmPassword');
        const registerSubmit = document.getElementById('registerSubmit');
        const registerBtnText = document.getElementById('registerBtnText');
        const registerSpinner = document.getElementById('registerSpinner');
        const showLoginBtn = document.getElementById('showLoginBtn');

        // App Elements
        const logoutBtn = document.getElementById('logoutBtn');
        const userBalance = document.getElementById('userBalance');
        const customerId = document.getElementById('customerId');
        const totalBalance = document.getElementById('totalBalance');
        const investedAmount = document.getElementById('investedAmount');
        const totalProfit = document.getElementById('totalProfit');
        const bankAccount = document.getElementById('bankAccount');
        const depositBalance = document.getElementById('depositBalance');
        const depositBankAccount = document.getElementById('depositBankAccount');
        const withdrawBalance = document.getElementById('withdrawBalance');
        const withdrawBankAccount = document.getElementById('withdrawBankAccount');
        const depositAmount = document.getElementById('depositAmount');
        const withdrawAmount = document.getElementById('withdrawAmount');
        const confirmDeposit = document.getElementById('confirmDeposit');
        const confirmWithdraw = document.getElementById('confirmWithdraw');
        const changeBankBtn = document.getElementById('changeBankBtn');
        const transactionHistory = document.getElementById('transactionHistory');
        const investButtons = document.querySelectorAll('.invest-btn');
        const registerPromoBtn = document.getElementById('registerPromoBtn');

        // Modal Elements
        const bankModal = document.getElementById('bankModal');
        const investmentModal = document.getElementById('investmentModal');
        const bankName = document.getElementById('bankName');
        const ibanNumber = document.getElementById('ibanNumber');
        const accountHolder = document.getElementById('accountHolder');
        const saveBankBtn = document.getElementById('saveBankBtn');
        const modalPackageName = document.getElementById('modalPackageName');
        const modalProfitRate = document.getElementById('modalProfitRate');
        const modalMinAmount = document.getElementById('modalMinAmount');
        const modalMaxAmount = document.getElementById('modalMaxAmount');
        const investmentAmount = document.getElementById('investmentAmount');
        const confirmInvestment = document.getElementById('confirmInvestment');

        // Admin Elements
        const adminTabs = document.querySelectorAll('.admin-tab');
        const adminContents = document.querySelectorAll('.admin-content');
        const depositRequests = document.getElementById('depositRequests');
        const withdrawalRequests = document.getElementById('withdrawalRequests');
        const investmentRequests = document.getElementById('investmentRequests');
        const usersList = document.getElementById('usersList');

        // Notification Elements
        const notification = document.getElementById('notification');
        const notificationMessage = document.getElementById('notificationMessage');
        const realTimeIndicator = document.getElementById('realTimeIndicator');

        // Error Messages
        const errorMessages = {
            loginEmailError: document.getElementById('loginEmailError'),
            loginPasswordError: document.getElementById('loginPasswordError'),
            registerNameError: document.getElementById('registerNameError'),
            registerEmailError: document.getElementById('registerEmailError'),
            registerPhoneError: document.getElementById('registerPhoneError'),
            registerPasswordError: document.getElementById('registerPasswordError'),
            registerConfirmPasswordError: document.getElementById('registerConfirmPasswordError'),
            depositError: document.getElementById('depositError'),
            withdrawError: document.getElementById('withdrawError'),
            bankNameError: document.getElementById('bankNameError'),
            ibanError: document.getElementById('ibanError'),
            accountHolderError: document.getElementById('accountHolderError'),
            investmentAmountError: document.getElementById('investmentAmountError')
        };

        // Navigation
        const navLinks = document.querySelectorAll('nav a');
        const pages = {
            home: document.getElementById('homePage'),
            deposit: document.getElementById('depositPage'),
            packages: document.getElementById('packagesPage'),
            history: document.getElementById('historyPage'),
            support: document.getElementById('supportPage'),
            admin: document.getElementById('adminPage')
        };

        // Initialize the app
        document.addEventListener('DOMContentLoaded', function() {
            // Check if user is logged in
            const loggedInUser = localStorage.getItem('currentUser');
            if (loggedInUser) {
                state.currentUser = JSON.parse(loggedInUser);
                showApp();
            } else {
                showLoginPage();
            }

            // Setup event listeners
            setupEventListeners();

            // Check for pending transactions every 5 seconds
            setInterval(checkForUpdates, 5000);
        });

        function showApp() {
            appContainer.style.display = 'block';
            loginPage.style.display = 'none';
            registerPage.style.display = 'none';

            // Hide bonus banner for logged-in users
            if (bonusBanner) {
                bonusBanner.style.display = 'none';
            }

            // Show admin link if user is admin
            if (state.currentUser && state.adminUsers.includes(state.currentUser.email)) {
                adminLink.style.display = 'block';
            } else {
                adminLink.style.display = 'none';
            }

            updateUserUI();

            // Check active investment
            if (state.currentUser && state.currentUser.activeInvestment) {
                startInvestmentTimer();
            }
        }

        function showLoginPage() {
            appContainer.style.display = 'none';
            loginPage.style.display = 'flex';
            registerPage.style.display = 'none';
        }

        function showRegisterPage() {
            appContainer.style.display = 'none';
            loginPage.style.display = 'none';
            registerPage.style.display = 'flex';
        }

        function setupEventListeners() {
            // Login Form
            loginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                handleLogin();
            });

            // Register Form
            registerForm.addEventListener('submit', function(e) {
                e.preventDefault();
                handleRegister();
            });

            // Show Register Page
            showRegisterBtn.addEventListener('click', function(e) {
                e.preventDefault();
                showRegisterPage();
            });

            // Show Login Page
            showLoginBtn.addEventListener('click', function(e) {
                e.preventDefault();
                showLoginPage();
            });

            // Register Promo Button
            registerPromoBtn.addEventListener('click', function(e) {
                e.preventDefault();
                showRegisterPage();
            });

            // Logout Button
            logoutBtn.addEventListener('click', handleLogout);

            // Deposit Button
            confirmDeposit.addEventListener('click', handleDeposit);

            // Withdraw Button
            confirmWithdraw.addEventListener('click', handleWithdraw);

            // Change Bank Button
            changeBankBtn.addEventListener('click', function() {
                openBankModal();
            });

            // Save Bank Button
            saveBankBtn.addEventListener('click', handleSaveBank);

            // Investment Buttons
            investButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const packageId = parseInt(this.closest('.package').dataset.packageId);
                    openInvestmentModal(packageId);
                });
            });

            // Confirm Investment
            confirmInvestment.addEventListener('click', handleInvestment);

            // Navigation Links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    navigateTo(this.dataset.page);
                });
            });

            // Modal Close Buttons
            document.querySelectorAll('.modal-close').forEach(closeBtn => {
                closeBtn.addEventListener('click', function() {
                    this.closest('.modal').style.display = 'none';
                });
            });

            // Close modal when clicking outside
            window.addEventListener('click', function(e) {
                if (e.target.classList.contains('modal')) {
                    e.target.style.display = 'none';
                }
            });

            // Admin tabs
            adminTabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    // Remove active class from all tabs
                    adminTabs.forEach(t => t.classList.remove('active'));
                    // Add active class to clicked tab
                    this.classList.add('active');

                    // Hide all contents
                    adminContents.forEach(c => c.classList.remove('active'));
                    // Show selected content
                    document.getElementById(`${this.dataset.tab}Tab`).classList.add('active');

                    // Update the content
                    updateAdminPanel();
                });
            });
        }

        function handleLogin() {
            const email = loginEmail.value.trim();
            const password = loginPassword.value.trim();

            // Reset error messages
            resetErrorMessages();

            // Validate inputs
            let isValid = true;

            if (!email) {
                showError('loginEmailError', 'E-posta adresi gereklidir');
                isValid = false;
            } else if (!validateEmail(email)) {
                showError('loginEmailError', 'Geçerli bir e-posta adresi girin');
                isValid = false;
            }

            if (!password) {
                showError('loginPasswordError', 'Şifre gereklidir');
                isValid = false;
            } else if (password.length < 6) {
                showError('loginPasswordError', 'Şifre en az 6 karakter olmalıdır');
                isValid = false;
            }

            if (!isValid) return;

            // Show loading state
            loginBtnText.style.display = 'none';
            loginSpinner.style.display = 'inline-block';

            // Simulate API call
            setTimeout(() => {
                const user = state.users.find(u => u.email === email && u.password === password);

                if (user) {
                    state.currentUser = user;
                    localStorage.setItem('currentUser', JSON.stringify(user));
                    showApp();
                    showNotification('Başarıyla giriş yaptınız!');
                } else {
                    showError('loginPasswordError', 'Geçersiz e-posta veya şifre');
                }

                // Hide loading state
                loginBtnText.style.display = 'inline';
                loginSpinner.style.display = 'none';
            }, 1000);
        }

        function handleRegister() {
            const name = registerName.value.trim();
            const email = registerEmail.value.trim();
            const phone = registerPhone.value.trim();
            const password = registerPassword.value.trim();
            const confirmPassword = registerConfirmPassword.value.trim();

            // Reset error messages
            resetErrorMessages();

            // Validate inputs
            let isValid = true;

            if (!name) {
                showError('registerNameError', 'Ad soyad gereklidir');
                isValid = false;
            }

            if (!email) {
                showError('registerEmailError', 'E-posta adresi gereklidir');
                isValid = false;
            } else if (!validateEmail(email)) {
                showError('registerEmailError', 'Geçerli bir e-posta adresi girin');
                isValid = false;
            } else if (state.users.some(u => u.email === email)) {
                showError('registerEmailError', 'Bu e-posta ile zaten kayıtlı bir hesap var');
                isValid = false;
            }

            if (!phone) {
                showError('registerPhoneError', 'Telefon numarası gereklidir');
                isValid = false;
            } else if (!validatePhone(phone)) {
                showError('registerPhoneError', 'Geçerli bir telefon numarası girin');
                isValid = false;
            }

            if (!password) {
                showError('registerPasswordError', 'Şifre gereklidir');
                isValid = false;
            } else if (password.length < 6) {
                showError('registerPasswordError', 'Şifre en az 6 karakter olmalıdır');
                isValid = false;
            }

            if (!confirmPassword) {
                showError('registerConfirmPasswordError', 'Şifre tekrar gereklidir');
                isValid = false;
            } else if (password !== confirmPassword) {
                showError('registerConfirmPasswordError', 'Şifreler eşleşmiyor');
                isValid = false;
            }

            if (!isValid) return;

            // Show loading state
            registerBtnText.style.display = 'none';
            registerSpinner.style.display = 'inline-block';

            // Simulate API call
            setTimeout(() => {
                const newUser = {
                    id: 'MN' + Math.floor(10000 + Math.random() * 90000),
                    name,
                    email,
                    phone,
                    password,
                    balance: 500, // Bonus for new users
                    invested: 0,
                    profit: 0,
                    bankAccount: '',
                    iban: '',
                    bankAccountHolder: '',
                    transactions: [],
                    activeInvestment: null,
                    isActive: true
                };

                state.users.push(newUser);
                state.currentUser = newUser;

                localStorage.setItem('users', JSON.stringify(state.users));
                localStorage.setItem('currentUser', JSON.stringify(newUser));

                // Hide loading state
                registerBtnText.style.display = 'inline';
                registerSpinner.style.display = 'none';

                // Show success message and redirect
                showNotification(`Tebrikler ${name}! Hesabınız oluşturuldu ve 500 TL bonus bakiyeniz yatırıldı.`);
                showApp();
            }, 1500);
        }

        function handleLogout() {
            state.currentUser = null;
            localStorage.removeItem('currentUser');
            showLoginPage();
        }

        function handleDeposit() {
            const amount = parseFloat(depositAmount.value);

            // Reset error message
            errorMessages.depositError.style.display = 'none';

            // Validate input
            if (isNaN(amount) || amount <= 0) {
                showError('depositError', 'Lütfen geçerli bir tutar girin');
                return;
            }

            // Create deposit request
            const depositRequest = {
                id: 'DP' + Date.now(),
                userId: state.currentUser.id,
                userName: state.currentUser.name,
                amount: amount,
                date: new Date().toLocaleString(),
                status: 'Beklemede',
                adminAction: null
            };

            // Add to pending deposits
            state.pendingDeposits.push(depositRequest);
            localStorage.setItem('pendingDeposits', JSON.stringify(state.pendingDeposits));

            // Add transaction to user history
            const transaction = {
                id: depositRequest.id,
                date: depositRequest.date,
                type: 'Para Yatırma',
                amount: amount,
                status: 'Beklemede'
            };

            state.currentUser.transactions.push(transaction);
            saveUserData();
            updateUserUI();

            // Show success message
            showNotification(`${amount.toFixed(2)} TL yatırma talebiniz alındı! Admin onayı bekleniyor.`);

            // Reset input
            depositAmount.value = '';
        }

        function handleWithdraw() {
            const amount = parseFloat(withdrawAmount.value);

            // Reset error message
            errorMessages.withdrawError.style.display = 'none';

            // Validate input
            if (isNaN(amount) || amount <= 0) {
                showError('withdrawError', 'Lütfen geçerli bir tutar girin');
                return;
            }

            if (amount > state.currentUser.balance) {
                showError('withdrawError', 'Yetersiz bakiye');
                return;
            }

            if (!state.currentUser.bankAccount) {
                showError('withdrawError', 'Lütfen önce bir banka hesabı ekleyin');
                return;
            }

            // Create withdrawal request
            const withdrawalRequest = {
                id: 'WD' + Date.now(),
                userId: state.currentUser.id,
                userName: state.currentUser.name,
                amount: amount,
                date: new Date().toLocaleString(),
                status: 'Beklemede',
                adminAction: null,
                bankAccount: state.currentUser.bankAccount,
                iban: state.currentUser.iban
            };

            // Add to pending withdrawals
            state.pendingWithdrawals.push(withdrawalRequest);
            localStorage.setItem('pendingWithdrawals', JSON.stringify(state.pendingWithdrawals));

            // Add transaction to user history
            const transaction = {
                id: withdrawalRequest.id,
                date: withdrawalRequest.date,
                type: 'Para Çekme',
                amount: amount,
                status: 'Beklemede'
            };

            state.currentUser.transactions.push(transaction);
            saveUserData();
            updateUserUI();

            // Show success message
            showNotification(`${amount.toFixed(2)} TL çekme talebiniz alındı! Admin onayı bekleniyor.`);

            // Reset input
            withdrawAmount.value = '';
        }

        function handleSaveBank() {
            const bank = bankName.value.trim();
            const iban = ibanNumber.value.trim();
            const holder = accountHolder.value.trim();

            // Reset error messages
            resetErrorMessages();

            // Validate inputs
            let isValid = true;

            if (!bank) {
                showError('bankNameError', 'Banka adı gereklidir');
                isValid = false;
            }

            if (!iban) {
                showError('ibanError', 'IBAN numarası gereklidir');
                isValid = false;
            } else if (!validateIban(iban)) {
                showError('ibanError', 'Geçerli bir IBAN numarası girin');
                isValid = false;
            }

            if (!holder) {
                showError('accountHolderError', 'Hesap sahibi adı gereklidir');
                isValid = false;
            }

            if (!isValid) return;

            // Update user bank info
            state.currentUser.bankAccount = `${bank} •••• ${iban.slice(-4)}`;
            state.currentUser.iban = iban;
            state.currentUser.bankAccountHolder = holder;

            saveUserData();
            updateUserUI();

            // Close modal
            bankModal.style.display = 'none';

            // Show success message
            showNotification('Banka hesap bilgileriniz başarıyla kaydedildi!');
        }

        function handleInvestment() {
            const amount = parseFloat(investmentAmount.value);

            // Reset error message
            errorMessages.investmentAmountError.style.display = 'none';

            // Validate input
            if (isNaN(amount) || amount <= 0) {
                showError('investmentAmountError', 'Lütfen geçerli bir tutar girin');
                return;
            }

            if (amount < state.currentPackage.minAmount) {
                showError('investmentAmountError', `Minimum yatırım tutarı ${state.currentPackage.minAmount} TL'dir`);
                return;
            }

            if (amount > state.currentPackage.maxAmount) {
                showError('investmentAmountError', `Maksimum yatırım tutarı ${state.currentPackage.maxAmount} TL'dir`);
                return;
            }

            if (amount > state.currentUser.balance) {
                showError('investmentAmountError', 'Yetersiz bakiye');
                return;
            }

            if (state.currentUser.activeInvestment) {
                showError('investmentAmountError', 'Zaten aktif bir yatırımınız var');
                return;
            }

            // Create investment request
            const investmentRequest = {
                id: 'INV' + Date.now(),
                userId: state.currentUser.id,
                userName: state.currentUser.name,
                packageId: state.currentPackage.id,
                packageName: state.currentPackage.name,
                amount: amount,
                profitRate: state.currentPackage.profitRate,
                date: new Date().toLocaleString(),
                status: 'Beklemede',
                adminAction: null
            };

            // Add to pending investments
            state.pendingInvestments.push(investmentRequest);
            localStorage.setItem('pendingInvestments', JSON.stringify(state.pendingInvestments));

            // Add transaction to user history
            const transaction = {
                id: investmentRequest.id,
                date: investmentRequest.date,
                type: `Yatırım Talebi - ${state.currentPackage.name}`,
                amount: amount,
                status: 'Beklemede'
            };

            state.currentUser.transactions.push(transaction);
            saveUserData();
            updateUserUI();

            // Close modal
            investmentModal.style.display = 'none';

            // Show success message
            showNotification(`${amount.toFixed(2)} TL tutarındaki yatırım talebiniz alındı! Admin onayı bekleniyor.`);
        }

        function startInvestmentTimer() {
            if (!state.currentUser || !state.currentUser.activeInvestment) return;

            const investment = state.currentUser.activeInvestment;
            const timer = setInterval(() => {
                investment.timeLeft--;
                investment.progress = 100 - (investment.timeLeft / 300) * 100;

                // Update UI
                activeInvestmentCard.style.display = 'block';
                activePackageName.textContent = investment.packageName;
                investmentProgress.style.width = `${investment.progress}%`;
                remainingTime.textContent = `${Math.floor(investment.timeLeft / 60)}:${(investment.timeLeft % 60).toString().padStart(2, '0')}`;
                expectedProfit.textContent = `${investment.expectedProfit.toFixed(2)} TL`;

                if (investment.timeLeft <= 0) {
                    clearInterval(timer);

                    // Add profit
                    state.currentUser.profit += investment.expectedProfit;
                    state.currentUser.balance += investment.expectedProfit;

                    // Add profit transaction
                    const profitTransaction = {
                        id: 'TX' + Date.now(),
                        date: new Date().toLocaleString(),
                        type: `Kâr - ${investment.packageName}`,
                        amount: investment.expectedProfit,
                        status: 'Başarılı'
                    };

                    state.currentUser.transactions.push(profitTransaction);

                    // Clear active investment
                    state.currentUser.activeInvestment = null;

                    saveUserData();
                    updateUserUI();

                    // Hide active investment card
                    activeInvestmentCard.style.display = 'none';

                    // Show profit notification
                    showNotification(`Tebrikler! ${investment.packageName} yatırımınızdan ${investment.expectedProfit.toFixed(2)} TL kâr elde ettiniz.`);
                }
            }, 1000);
        }

        function openBankModal() {
            // Fill form with existing data if available
            if (state.currentUser.bankAccount) {
                bankName.value = state.currentUser.bankAccount.split(' •••• ')[0];
                ibanNumber.value = state.currentUser.iban;
                accountHolder.value = state.currentUser.bankAccountHolder;
            } else {
                bankName.value = '';
                ibanNumber.value = '';
                accountHolder.value = state.currentUser.name;
            }

            // Reset error messages
            resetErrorMessages();

            // Show modal
            bankModal.style.display = 'block';
        }

        function openInvestmentModal(packageId) {
            // Get package details
            state.currentPackage = state.packages.find(p => p.id === packageId);

            // Update modal content
            modalPackageName.textContent = state.currentPackage.name;
            modalProfitRate.textContent = `%${state.currentPackage.profitRate}`;
            modalMinAmount.textContent = `${state.currentPackage.minAmount.toFixed(2)} TL`;
            modalMaxAmount.textContent = `${state.currentPackage.maxAmount.toFixed(2)} TL`;

            // Reset input
            investmentAmount.value = state.currentPackage.minAmount;

            // Reset error message
            errorMessages.investmentAmountError.style.display = 'none';

            // Show modal
            investmentModal.style.display = 'block';
        }

        function navigateTo(page) {
            // Remove active class from all links
            navLinks.forEach(l => l.classList.remove('active'));

            // Add active class to clicked link
            document.querySelector(`nav a[data-page="${page}"]`).classList.add('active');

            // Hide all pages
            Object.values(pages).forEach(p => p.style.display = 'none');

            // Show the selected page
            pages[page].style.display = 'block';

            // If admin page, update the panel
            if (page === 'admin') {
                updateAdminPanel();
            }
        }

        function updateUserUI() {
            if (state.currentUser) {
                // Update user info
                userBalance.textContent = formatCurrency(state.currentUser.balance);
                customerId.textContent = state.currentUser.id;
                totalBalance.textContent = formatCurrency(state.currentUser.balance);
                investedAmount.textContent = formatCurrency(state.currentUser.invested);
                totalProfit.textContent = formatCurrency(state.currentUser.profit);
                bankAccount.textContent = state.currentUser.bankAccount || 'Henüz eklenmedi';

                // Update deposit page info
                depositBalance.textContent = formatCurrency(state.currentUser.balance);
                depositBankAccount.textContent = state.currentUser.bankAccount || 'Henüz eklenmedi';
                withdrawBalance.textContent = formatCurrency(state.currentUser.balance);
                withdrawBankAccount.textContent = state.currentUser.bankAccount || 'Henüz eklenmedi';

                // Update transaction history
                updateTransactionHistory();

                // Show/hide active investment card
                if (state.currentUser.activeInvestment) {
                    activeInvestmentCard.style.display = 'block';
                    const investment = state.currentUser.activeInvestment;
                    activePackageName.textContent = investment.packageName;
                    investmentProgress.style.width = `${investment.progress}%`;
                    remainingTime.textContent = `${Math.floor(investment.timeLeft / 60)}:${(investment.timeLeft % 60).toString().padStart(2, '0')}`;
                    expectedProfit.textContent = `${investment.expectedProfit.toFixed(2)} TL`;
                } else {
                    activeInvestmentCard.style.display = 'none';
                }
            } else {
                // Reset user info
                userBalance.textContent = formatCurrency(0);
                customerId.textContent = '-';
                totalBalance.textContent = formatCurrency(0);
                investedAmount.textContent = formatCurrency(0);
                totalProfit.textContent = formatCurrency(0);
                bankAccount.textContent = '-';

                // Reset deposit page
                depositBalance.textContent = formatCurrency(0);
                depositBankAccount.textContent = '-';
                withdrawBalance.textContent = formatCurrency(0);
                withdrawBankAccount.textContent = '-';

                // Clear transaction history
                transactionHistory.innerHTML = '';

                // Hide active investment card
                activeInvestmentCard.style.display = 'none';
            }
        }

        function updateTransactionHistory() {
            if (!state.currentUser || state.currentUser.transactions.length === 0) {
                transactionHistory.innerHTML = '<tr><td colspan="5" style="text-align: center;">Henüz işlem geçmişiniz bulunmamaktadır</td></tr>';
                return;
            }

            let html = '';

            // Sort transactions by date (newest first)
            const sortedTransactions = [...state.currentUser.transactions].sort((a, b) => {
                return new Date(b.date) - new Date(a.date);
            });

            sortedTransactions.forEach(transaction => {
                let statusClass = '';
                if (transaction.status === 'Başarılı') {
                    statusClass = 'success';
                } else if (transaction.status === 'Beklemede') {
                    statusClass = 'pending';
                } else if (transaction.status === 'Reddedildi') {
                    statusClass = 'rejected';
                }

                html += `
                <tr>
                    <td>${transaction.date}</td>
                    <td>${transaction.type}</td>
                    <td>${formatCurrency(transaction.amount)}</td>
                    <td><span class="status ${statusClass}">${transaction.status}</span></td>
                    <td><button class="btn btn-secondary" style="padding: 5px 10px;">Detay</button></td>
                </tr>
                `;
            });

            transactionHistory.innerHTML = html;
        }

        function updateAdminPanel() {
            // Update deposits tab
            updateDepositRequests();

            // Update withdrawals tab
            updateWithdrawalRequests();

            // Update investments tab
            updateInvestmentRequests();

            // Update users tab
            updateUsersList();
        }

        function updateDepositRequests() {
            let html = '';

            if (state.pendingDeposits.length === 0) {
                html = '<tr><td colspan="6" style="text-align: center;">Bekleyen para yatırma talebi bulunmamaktadır</td></tr>';
            } else {
                state.pendingDeposits.forEach(request => {
                    if (request.status === 'Beklemede') {
                        html += `
                        <tr>
                            <td>${request.id}</td>
                            <td>${request.userName}</td>
                            <td>${formatCurrency(request.amount)}</td>
                            <td>${request.date}</td>
                            <td><span class="status pending">${request.status}</span></td>
                            <td class="admin-actions">
                                <button class="admin-btn approve-btn" data-id="${request.id}" data-type="deposit">Onayla</button>
                                <button class="admin-btn reject-btn" data-id="${request.id}" data-type="deposit">Reddet</button>
                            </td>
                        </tr>
                        `;
                    }
                });
            }

            depositRequests.innerHTML = html;

            // Add event listeners to new buttons
            document.querySelectorAll('.approve-btn[data-type="deposit"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    approveRequest(this.dataset.id, 'deposit');
                });
            });

            document.querySelectorAll('.reject-btn[data-type="deposit"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    rejectRequest(this.dataset.id, 'deposit');
                });
            });
        }

        function updateWithdrawalRequests() {
            let html = '';

            if (state.pendingWithdrawals.length === 0) {
                html = '<tr><td colspan="6" style="text-align: center;">Bekleyen para çekme talebi bulunmamaktadır</td></tr>';
            } else {
                state.pendingWithdrawals.forEach(request => {
                    if (request.status === 'Beklemede') {
                        html += `
                        <tr>
                            <td>${request.id}</td>
                            <td>${request.userName}</td>
                            <td>${formatCurrency(request.amount)}</td>
                            <td>${request.date}</td>
                            <td><span class="status pending">${request.status}</span></td>
                            <td class="admin-actions">
                                <button class="admin-btn approve-btn" data-id="${request.id}" data-type="withdrawal">Onayla</button>
                                <button class="admin-btn reject-btn" data-id="${request.id}" data-type="withdrawal">Reddet</button>
                            </td>
                        </tr>
                        `;
                    }
                });
            }

            withdrawalRequests.innerHTML = html;

            // Add event listeners to new buttons
            document.querySelectorAll('.approve-btn[data-type="withdrawal"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    approveRequest(this.dataset.id, 'withdrawal');
                });
            });

            document.querySelectorAll('.reject-btn[data-type="withdrawal"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    rejectRequest(this.dataset.id, 'withdrawal');
                });
            });
        }

        function updateInvestmentRequests() {
            let html = '';

            if (state.pendingInvestments.length === 0) {
                html = '<tr><td colspan="7" style="text-align: center;">Bekleyen yatırım talebi bulunmamaktadır</td></tr>';
            } else {
                state.pendingInvestments.forEach(request => {
                    if (request.status === 'Beklemede') {
                        html += `
                        <tr>
                            <td>${request.id}</td>
                            <td>${request.userName}</td>
                            <td>${request.packageName}</td>
                            <td>${formatCurrency(request.amount)}</td>
                            <td>${request.date}</td>
                            <td><span class="status pending">${request.status}</span></td>
                            <td class="admin-actions">
                                <button class="admin-btn approve-btn" data-id="${request.id}" data-type="investment">Onayla</button>
                                <button class="admin-btn reject-btn" data-id="${request.id}" data-type="investment">Reddet</button>
                            </td>
                        </tr>
                        `;
                    }
                });
            }

            investmentRequests.innerHTML = html;

            // Add event listeners to new buttons
            document.querySelectorAll('.approve-btn[data-type="investment"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    approveRequest(this.dataset.id, 'investment');
                });
            });

            document.querySelectorAll('.reject-btn[data-type="investment"]').forEach(btn => {
                btn.addEventListener('click', function() {
                    rejectRequest(this.dataset.id, 'investment');
                });
            });
        }

        function updateUsersList() {
            let html = '';

            if (state.users.length === 0) {
                html = '<tr><td colspan="7" style="text-align: center;">Kayıtlı kullanıcı bulunmamaktadır</td></tr>';
            } else {
                state.users.forEach(user => {
                    const status = user.isActive ? 'Aktif' : 'Pasif';
                    const statusClass = user.isActive ? 'success' : 'danger';

                    html += `
                    <tr>
                        <td>${user.id}</td>
                        <td>${user.name}</td>
                        <td>${user.email}</td>
                        <td>${user.phone}</td>
                        <td>${formatCurrency(user.balance)}</td>
                        <td><span class="status ${statusClass}">${status}</span></td>
                        <td class="admin-actions">
                            <button class="admin-btn ${user.isActive ? 'reject-btn' : 'approve-btn'}" data-id="${user.id}">
                                ${user.isActive ? 'Pasif Yap' : 'Aktif Yap'}
                            </button>
                        </td>
                    </tr>
                    `;
                });
            }

            usersList.innerHTML = html;

            // Add event listeners to user status buttons
            document.querySelectorAll('.admin-actions button').forEach(btn => {
                btn.addEventListener('click', function() {
                    toggleUserStatus(this.dataset.id);
                });
            });
        }

        function approveRequest(requestId, type) {
            let request, user, transactionType, successMessage;

            if (type === 'deposit') {
                request = state.pendingDeposits.find(r => r.id === requestId);
                if (!request) return;

                user = state.users.find(u => u.id === request.userId);
                if (!user) return;

                // Update user balance
                user.balance += request.amount;

                // Update request status
                request.status = 'Başarılı';
                request.adminAction = state.currentUser.id;

                transactionType = 'Para Yatırma';
                successMessage = `${user.name} kullanıcısının ${formatCurrency(request.amount)} TL para yatırma talebi onaylandı.`;
            } else if (type === 'withdrawal') {
                request = state.pendingWithdrawals.find(r => r.id === requestId);
                if (!request) return;

                user = state.users.find(u => u.id === request.userId);
                if (!user) return;

                // Update request status (no need to deduct balance as it was already deducted when request was made)
                request.status = 'Başarılı';
                request.adminAction = state.currentUser.id;

                transactionType = 'Para Çekme';
                successMessage = `${user.name} kullanıcısının ${formatCurrency(request.amount)} TL para çekme talebi onaylandı.`;
            } else if (type === 'investment') {
                request = state.pendingInvestments.find(r => r.id === requestId);
                if (!request) return;

                user = state.users.find(u => u.id === request.userId);
                if (!user) return;

                // Check if user has enough balance
                if (user.balance < request.amount) {
                    showNotification('Kullanıcının yeterli bakiyesi yok!', 'error');
                    return;
                }

                // Deduct investment amount from balance
                user.balance -= request.amount;
                user.invested += request.amount;

                // Create active investment
                const packageInfo = state.packages.find(p => p.id === request.packageId);
                const dailyProfit = (request.amount * request.profitRate) / 100;
                const totalProfit = dailyProfit * 1; // Only 1 day for demo

                user.activeInvestment = {
                    id: request.id,
                    packageId: request.packageId,
                    packageName: request.packageName,
                    amount: request.amount,
                    startTime: new Date(),
                    duration: 1, // Only 1 day for demo
                    profitRate: request.profitRate,
                    expectedProfit: totalProfit,
                    status: 'active',
                    timeLeft: 300, // 5 minutes in seconds
                    progress: 0
                };

                // Update request status
                request.status = 'Başarılı';
                request.adminAction = state.currentUser.id;

                transactionType = `Yatırım - ${request.packageName}`;
                successMessage = `${user.name} kullanıcısının ${formatCurrency(request.amount)} TL ${request.packageName} yatırım talebi onaylandı.`;

                // Start investment timer
                if (user.id === state.currentUser.id) {
                    startInvestmentTimer();
                }
            }

            // Update transaction in user history
            const transaction = user.transactions.find(t => t.id === requestId);
            if (transaction) {
                transaction.status = 'Başarılı';
                transaction.type = transactionType;
            }

            // Save changes
            saveAllData();

            // Update UI
            updateAdminPanel();
            if (user.id === state.currentUser.id) {
                updateUserUI();
            }

            // Show notification
            showNotification(successMessage);
        }

        function rejectRequest(requestId, type) {
            let request, user, transactionType, rejectionMessage;

            if (type === 'deposit') {
                request = state.pendingDeposits.find(r => r.id === requestId);
                transactionType = 'Para Yatırma';
                rejectionMessage = 'Para yatırma talebiniz reddedildi';
            } else if (type === 'withdrawal') {
                request = state.pendingWithdrawals.find(r => r.id === requestId);
                transactionType = 'Para Çekme';
                rejectionMessage = 'Para çekme talebiniz reddedildi';

                // Return the amount to user's balance
                user = state.users.find(u => u.id === request.userId);
                if (user) {
                    user.balance += request.amount;
                }
            } else if (type === 'investment') {
                request = state.pendingInvestments.find(r => r.id === requestId);
                transactionType = `Yatırım Talebi - ${request.packageName}`;
                rejectionMessage = `Yatırım talebiniz (${request.packageName}) reddedildi`;
            }

            if (!request) return;

            user = state.users.find(u => u.id === request.userId);

            // Update request status
            request.status = 'Reddedildi';
            request.adminAction = state.currentUser.id;

            // Update transaction in user history
            const transaction = user.transactions.find(t => t.id === requestId);
            if (transaction) {
                transaction.status = 'Reddedildi';
                transaction.type = transactionType;
            }

            // Save changes
            saveAllData();

            // Update UI
            updateAdminPanel();
            if (user.id === state.currentUser.id) {
                updateUserUI();
                showNotification(rejectionMessage, 'error');
            } else {
                showNotification(`${user.name} kullanıcısının talebi reddedildi.`);
            }
        }

        function toggleUserStatus(userId) {
            const user = state.users.find(u => u.id === userId);
            if (!user) return;

            user.isActive = !user.isActive;
            saveAllData();

            // Update UI
            updateAdminPanel();
            showNotification(`${user.name} kullanıcısı ${user.isActive ? 'aktif' : 'pasif'} yapıldı.`);
        }

        function checkForUpdates() {
            // Check if there are any updates to the user's transactions
            if (!state.currentUser) return;

            // Get fresh data from localStorage
            const freshPendingDeposits = JSON.parse(localStorage.getItem('pendingDeposits')) || [];
            const freshPendingWithdrawals = JSON.parse(localStorage.getItem('pendingWithdrawals')) || [];
            const freshPendingInvestments = JSON.parse(localStorage.getItem('pendingInvestments')) || [];

            // Check for changes in deposit requests
            freshPendingDeposits.forEach(deposit => {
                if (deposit.userId === state.currentUser.id) {
                    const existingDeposit = state.pendingDeposits.find(d => d.id === deposit.id);
                    if (!existingDeposit || existingDeposit.status !== deposit.status) {
                        // Update found
                        state.realTimeUpdates = true;
                        realTimeIndicator.style.display = 'flex';

                        // Update the transaction in user's history
                        const transaction = state.currentUser.transactions.find(t => t.id === deposit.id);
                        if (transaction) {
                            transaction.status = deposit.status;
                        }

                        // Update the local state
                        if (existingDeposit) {
                            existingDeposit.status = deposit.status;
                        } else {
                            state.pendingDeposits.push(deposit);
                        }

                        // Show notification if this is the current user
                        if (deposit.status === 'Başarılı') {
                            showNotification(`${formatCurrency(deposit.amount)} TL para yatırma işleminiz onaylandı!`);
                        } else if (deposit.status === 'Reddedildi') {
                            showNotification(`${formatCurrency(deposit.amount)} TL para yatırma işleminiz reddedildi.`, 'error');
                        }
                    }
                }
            });

            // Check for changes in withdrawal requests
            freshPendingWithdrawals.forEach(withdrawal => {
                if (withdrawal.userId === state.currentUser.id) {
                    const existingWithdrawal = state.pendingWithdrawals.find(w => w.id === withdrawal.id);
                    if (!existingWithdrawal || existingWithdrawal.status !== withdrawal.status) {
                        // Update found
                        state.realTimeUpdates = true;
                        realTimeIndicator.style.display = 'flex';

                        // Update the transaction in user's history
                        const transaction = state.currentUser.transactions.find(t => t.id === withdrawal.id);
                        if (transaction) {
                            transaction.status = withdrawal.status;
                        }

                        // Update the local state
                        if (existingWithdrawal) {
                            existingWithdrawal.status = withdrawal.status;
                        } else {
                            state.pendingWithdrawals.push(withdrawal);
                        }

                        // Show notification if this is the current user
                        if (withdrawal.status === 'Başarılı') {
                            showNotification(`${formatCurrency(withdrawal.amount)} TL para çekme işleminiz onaylandı!`);
                        } else if (withdrawal.status === 'Reddedildi') {
                            showNotification(`${formatCurrency(withdrawal.amount)} TL para çekme işleminiz reddedildi.`, 'error');
                        }
                    }
                }
            });

            // Check for changes in investment requests
            freshPendingInvestments.forEach(investment => {
                if (investment.userId === state.currentUser.id) {
                    const existingInvestment = state.pendingInvestments.find(i => i.id === investment.id);
                    if (!existingInvestment || existingInvestment.status !== investment.status) {
                        // Update found
                        state.realTimeUpdates = true;
                        realTimeIndicator.style.display = 'flex';

                        // Update the transaction in user's history
                        const transaction = state.currentUser.transactions.find(t => t.id === investment.id);
                        if (transaction) {
                            transaction.status = investment.status;
                        }

                        // Update the local state
                        if (existingInvestment) {
                            existingInvestment.status = investment.status;
                        } else {
                            state.pendingInvestments.push(investment);
                        }

                        // Show notification if this is the current user
                        if (investment.status === 'Başarılı') {
                            showNotification(`${formatCurrency(investment.amount)} TL ${investment.packageName} yatırım talebiniz onaylandı!`);
                        } else if (investment.status === 'Reddedildi') {
                            showNotification(`${formatCurrency(investment.amount)} TL ${investment.packageName} yatırım talebiniz reddedildi.`, 'error');
                        }
                    }
                }
            });

            // Update the UI if there were changes
            if (state.realTimeUpdates) {
                updateUserUI();
                state.realTimeUpdates = false;

                // Hide the indicator after 3 seconds
                setTimeout(() => {
                    realTimeIndicator.style.display = 'none';
                }, 3000);
            }
        }

        function saveUserData() {
            // Find and update user in users array
            const userIndex = state.users.findIndex(u => u.id === state.currentUser.id);
            if (userIndex !== -1) {
                state.users[userIndex] = state.currentUser;
            }

            // Save to localStorage
            localStorage.setItem('users', JSON.stringify(state.users));
            localStorage.setItem('currentUser', JSON.stringify(state.currentUser));
        }

        function saveAllData() {
            // Save all state data to localStorage
            localStorage.setItem('users', JSON.stringify(state.users));
            localStorage.setItem('pendingDeposits', JSON.stringify(state.pendingDeposits));
            localStorage.setItem('pendingWithdrawals', JSON.stringify(state.pendingWithdrawals));
            localStorage.setItem('pendingInvestments', JSON.stringify(state.pendingInvestments));

            if (state.currentUser) {
                localStorage.setItem('currentUser', JSON.stringify(state.currentUser));
            }
        }

        function showError(elementId, message) {
            const element = errorMessages[elementId];
            element.textContent = message;
            element.style.display = 'block';
        }

        function resetErrorMessages() {
            Object.values(errorMessages).forEach(element => {
                element.style.display = 'none';
            });
        }

        function showNotification(message, type = 'success') {
            notificationMessage.textContent = message;
            notification.className = 'notification';
            notification.classList.add(type);
            notification.style.display = 'block';

            // Hide after 5 seconds
            setTimeout(() => {
                notification.style.display = 'none';
            }, 5000);
        }

        function formatCurrency(amount) {
            return new Intl.NumberFormat('tr-TR', {
                style: 'currency',
                currency: 'TRY'
            }).format(amount);
        }

        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }

        function validatePhone(phone) {
            const re = /^(\+90|0)?5[0-9]{9}$/;
            return re.test(phone);
        }

        function validateIban(iban) {
            // Basic IBAN validation (should be improved for production)
            return iban.length >= 16;
        }
    </script>
</body>

</html>
