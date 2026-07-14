
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Puducherry Cyber Camera Control Room</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #080c18;
            color: #e8edf5;
            height: 100vh;
            overflow: hidden;
        }

        .hud-bar {
            background: rgba(15, 26, 46, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            padding: 10px 28px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: 1px solid rgba(0, 212, 255, 0.15);
            z-index: 1000;
            position: relative;
            flex-wrap: wrap;
            gap: 10px;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
        }

        .hud-left {
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .hud-icon {
            width: 38px;
            height: 38px;
            background: linear-gradient(135deg, #00d4ff, #00ff88);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.15);
        }

        .hud-title {
            font-size: 18px;
            font-weight: 800;
            background: linear-gradient(135deg, #00d4ff, #00ff88);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 0.5px;
        }

        .hud-title-sub {
            font-size: 11px;
            font-weight: 400;
            color: #5a7a9a;
            -webkit-text-fill-color: #5a7a9a;
            letter-spacing: 1px;
            margin-top: 1px;
        }

        .hud-stats {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap;
        }

        .hud-stat {
            display: flex;
            align-items: center;
            gap: 6px;
            padding: 5px 14px;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.3s ease;
            cursor: default;
            position: relative;
            overflow: hidden;
        }

        .hud-stat::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.02), transparent);
            pointer-events: none;
        }

        .hud-stat .label {
            color: #7a9ab5;
            font-weight: 400;
            font-size: 11px;
            letter-spacing: 0.3px;
        }

        .hud-stat .value {
            font-weight: 700;
            font-size: 15px;
            font-variant-numeric: tabular-nums;
        }

        .hud-stat .value.total {
            color: #00d4ff;
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }
        .hud-stat .value.online {
            color: #00ff88;
            text-shadow: 0 0 20px rgba(0, 255, 136, 0.2);
        }
        .hud-stat .value.offline {
            color: #ff4466;
            text-shadow: 0 0 20px rgba(255, 68, 102, 0.2);
        }

        .status-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            display: inline-block;
            position: relative;
        }

        .status-dot.online {
            background: #00ff88;
            box-shadow: 0 0 12px rgba(0, 255, 136, 0.4);
        }
        .status-dot.offline {
            background: #ff4466;
            box-shadow: 0 0 12px rgba(255, 68, 102, 0.4);
        }

        .status-dot.online::after {
            content: '';
            position: absolute;
            top: -4px;
            left: -4px;
            right: -4px;
            bottom: -4px;
            border-radius: 50%;
            border: 2px solid rgba(0, 255, 136, 0.15);
            animation: pulse-ring 2s ease-in-out infinite;
        }

        .status-dot.offline::after {
            content: '';
            position: absolute;
            top: -4px;
            left: -4px;
            right: -4px;
            bottom: -4px;
            border-radius: 50%;
            border: 2px solid rgba(255, 68, 102, 0.15);
            animation: pulse-ring 2s ease-in-out infinite;
        }

        @keyframes pulse-ring {
            0%, 100% { transform: scale(1); opacity: 0.6; }
            50% { transform: scale(1.8); opacity: 0; }
        }

        .main-container {
            display: flex;
            height: calc(100vh - 70px);
        }

        .device-panel {
            width: 400px;
            min-width: 400px;
            background: rgba(12, 22, 40, 0.92);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-right: 1px solid rgba(255, 255, 255, 0.04);
            overflow-y: auto;
            padding: 14px 14px;
            flex-shrink: 0;
            display: flex;
            flex-direction: column;
        }

        .device-panel::-webkit-scrollbar {
            width: 4px;
        }
        .device-panel::-webkit-scrollbar-track {
            background: transparent;
        }
        .device-panel::-webkit-scrollbar-thumb {
            background: rgba(0, 212, 255, 0.3);
            border-radius: 4px;
        }

        .search-section {
            display: flex;
            gap: 10px;
            align-items: center;
            padding-bottom: 14px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 12px;
            flex-shrink: 0;
        }

        .search-wrapper {
            flex: 1;
            position: relative;
            display: flex;
            align-items: center;
        }

        .search-wrapper .search-icon {
            position: absolute;
            left: 14px;
            color: #4a6a8a;
            font-size: 14px;
            pointer-events: none;
        }

        .search-wrapper input {
            width: 100%;
            padding: 10px 16px 10px 42px;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            background: rgba(255, 255, 255, 0.04);
            color: #e8edf5;
            font-size: 13px;
            font-family: 'Inter', sans-serif;
            outline: none;
            transition: all 0.3s ease;
        }

        .search-wrapper input::placeholder {
            color: #4a6a8a;
            font-weight: 400;
        }

        .search-wrapper input:focus {
            border-color: rgba(0, 212, 255, 0.3);
            background: rgba(255, 255, 255, 0.06);
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.04);
        }

        .search-shortcut {
            font-size: 10px;
            color: #4a6a8a;
            background: rgba(255, 255, 255, 0.04);
            padding: 2px 10px;
            border-radius: 6px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            font-weight: 500;
            letter-spacing: 0.5px;
        }

        .panel-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 6px 4px 12px 4px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            margin-bottom: 10px;
            flex-shrink: 0;
        }

        .panel-header .title {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #4a6a8a;
            font-weight: 600;
        }

        .panel-header .count {
            font-size: 13px;
            font-weight: 700;
            color: #00d4ff;
            background: rgba(0, 212, 255, 0.08);
            padding: 2px 14px;
            border-radius: 20px;
            border: 1px solid rgba(0, 212, 255, 0.08);
        }

        .device-list-container {
            flex: 1;
            overflow-y: auto;
            padding-right: 4px;
        }

        .device-list-container::-webkit-scrollbar {
            width: 3px;
        }
        .device-list-container::-webkit-scrollbar-track {
            background: transparent;
        }
        .device-list-container::-webkit-scrollbar-thumb {
            background: rgba(0, 212, 255, 0.2);
            border-radius: 4px;
        }

        .device-item {
            padding: 10px 14px;
            margin-bottom: 6px;
            border-radius: 12px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .device-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 3px;
            height: 100%;
            background: transparent;
            transition: all 0.3s ease;
        }

        .device-item:hover {
            background: rgba(255, 255, 255, 0.04);
            border-color: rgba(255, 255, 255, 0.06);
            transform: translateX(4px);
        }

        .device-item:hover::before {
            background: linear-gradient(180deg, #00d4ff, #00ff88);
        }

        .device-item .info {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .device-item .top-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .device-item .jb-name {
            font-weight: 600;
            font-size: 13px;
            color: #e8edf5;
            letter-spacing: 0.2px;
        }

        .device-item .camera-count {
            font-size: 10px;
            color: #4a6a8a;
            background: rgba(255, 255, 255, 0.04);
            padding: 1px 10px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            font-weight: 500;
        }

        .device-item .location-name {
            font-size: 12px;
            color: #6a8aaa;
            max-width: 240px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .device-item .ip-status-row {
            display: flex;
            flex-wrap: wrap;
            gap: 4px;
            margin-top: 4px;
        }

        .ip-pill {
            font-size: 10px;
            font-family: 'Inter', 'Consolas', monospace;
            padding: 2px 10px;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.04);
            color: #5a7a9a;
            font-weight: 500;
            transition: all 0.2s ease;
        }

        .ip-pill.online {
            border-color: rgba(0, 255, 136, 0.15);
            color: #00ff88;
            background: rgba(0, 255, 136, 0.04);
        }

        .ip-pill.offline {
            border-color: rgba(255, 68, 102, 0.15);
            color: #ff4466;
            background: rgba(255, 68, 102, 0.04);
        }

        .ip-pill.pinging {
            border-color: rgba(255, 170, 0, 0.15);
            color: #ffaa00;
            background: rgba(255, 170, 0, 0.04);
            animation: pulse-ping 0.8s ease-in-out infinite;
        }

        @keyframes pulse-ping {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.4; }
        }

        .device-item .bottom-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 4px;
        }

        .device-item .status-badge {
            font-size: 9px;
            padding: 2px 12px;
            border-radius: 20px;
            font-weight: 600;
            white-space: nowrap;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .device-item .status-badge.online {
            background: rgba(0, 255, 136, 0.08);
            color: #00ff88;
            border: 1px solid rgba(0, 255, 136, 0.1);
        }

        .device-item .status-badge.offline {
            background: rgba(255, 68, 102, 0.08);
            color: #ff4466;
            border: 1px solid rgba(255, 68, 102, 0.1);
        }

        .device-item .status-badge.partial {
            background: rgba(255, 170, 0, 0.08);
            color: #ffaa00;
            border: 1px solid rgba(255, 170, 0, 0.1);
        }

        .device-item .status-badge.pinging {
            background: rgba(255, 170, 0, 0.08);
            color: #ffaa00;
            border: 1px solid rgba(255, 170, 0, 0.1);
            animation: pulse-ping 0.8s ease-in-out infinite;
        }

        .loading-text {
            color: #4a6a8a;
            text-align: center;
            padding: 60px 20px;
            font-size: 13px;
        }

        .loading-text .spinner {
            display: inline-block;
            width: 24px;
            height: 24px;
            border: 2px solid rgba(255, 255, 255, 0.04);
            border-top-color: #00d4ff;
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
            margin-right: 12px;
            vertical-align: middle;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .no-results {
            color: #4a6a8a;
            text-align: center;
            padding: 40px 20px;
            font-size: 13px;
        }

        #map {
            flex: 1;
            height: 100%;
            background: #e8edf2;
        }

        /* ============================================================
           MARKER WITH LABEL - JB Number on Map
           ============================================================ */
        .jb-marker {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
            transition: transform 0.2s ease;
        }

        .jb-marker:hover {
            transform: scale(1.1);
        }

        .jb-marker .marker-dot {
            width: 16px;
            height: 16px;
            border-radius: 50% 50% 50% 0;
            transform: rotate(-45deg);
            border: 2px solid #fff;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
            margin-bottom: 2px;
        }

        .jb-marker .marker-dot.online {
            background: #00cc77;
        }

        .jb-marker .marker-dot.offline {
            background: #dd3355;
        }

        .jb-marker .marker-dot.partial {
            background: #ffaa00;
        }

        .jb-marker .marker-dot.pinging {
            background: #ffaa00;
            animation: pulse-dot 0.8s ease-in-out infinite;
        }

        @keyframes pulse-dot {
            0%, 100% { transform: rotate(-45deg) scale(1); }
            50% { transform: rotate(-45deg) scale(1.2); }
        }

        .jb-marker .marker-label {
            font-size: 9px;
            font-weight: 600;
            color: #e8edf5;
            text-shadow: 0 1px 4px rgba(0, 0, 0, 0.9), 0 0 8px rgba(0, 0, 0, 0.6);
            background: rgba(0, 0, 0, 0.5);
            padding: 1px 6px;
            border-radius: 4px;
            white-space: nowrap;
            font-family: 'Inter', sans-serif;
            letter-spacing: 0.3px;
            border: 1px solid rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(4px);
            margin-top: 2px;
        }

        .jb-marker .marker-label.online {
            border-color: rgba(0, 204, 119, 0.2);
        }

        .jb-marker .marker-label.offline {
            border-color: rgba(221, 51, 85, 0.2);
        }

        .jb-marker .marker-label.partial {
            border-color: rgba(255, 170, 0, 0.2);
        }

        .jb-marker .marker-label.pinging {
            border-color: rgba(255, 170, 0, 0.2);
            animation: pulse-label 0.8s ease-in-out infinite;
        }

        @keyframes pulse-label {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .google-popup .leaflet-popup-content-wrapper {
            background: #191d3e;
            border-radius: 12px;
            color: #e8edf5;
            box-shadow: 0 4px 24px rgba(0, 0, 0, 0.4);
            padding: 0;
            border: 1px solid rgba(255, 255, 255, 0.06);
        }

        .google-popup .leaflet-popup-tip {
            background: #191d3e;
            border: 1px solid rgba(255, 255, 255, 0.06);
        }

        .popup-content {
            padding: 14px 16px;
            min-width: 200px;
        }

        .popup-content .popup-jb {
            font-weight: 700;
            font-size: 16px;
            color: #00d4ff;
        }

        .popup-content .popup-location {
            font-size: 12px;
            color: #8899bb;
            margin: 4px 0 8px 0;
        }

        .popup-content .popup-ip-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 4px 8px;
            margin: 2px 0;
            border-radius: 6px;
            font-size: 12px;
            font-family: 'Inter', 'Consolas', monospace;
            background: rgba(255, 255, 255, 0.04);
        }

        .popup-content .popup-ip-item .ip-addr {
            color: #8899bb;
            font-weight: 500;
        }

        .popup-content .popup-ip-item .ip-status {
            font-size: 10px;
            font-weight: 600;
            padding: 1px 10px;
            border-radius: 20px;
        }

        .popup-content .popup-ip-item .ip-status.online {
            color: #00ff88;
            background: rgba(0, 255, 136, 0.1);
        }

        .popup-content .popup-ip-item .ip-status.offline {
            color: #ff4466;
            background: rgba(255, 68, 102, 0.1);
        }

        .popup-content .popup-ip-item .ip-status.pinging {
            color: #ffaa00;
            background: rgba(255, 170, 0, 0.1);
            animation: pulse-ping 0.8s ease-in-out infinite;
        }

        .popup-content .popup-divider {
            border-top: 1px solid rgba(255, 255, 255, 0.06);
            margin: 6px 0;
        }

        .popup-content .popup-status-text {
            font-size: 12px;
            font-weight: 600;
            margin-top: 6px;
        }

        .popup-content .popup-status-text.online {
            color: #00ff88;
        }
        .popup-content .popup-status-text.offline {
            color: #ff4466;
        }
        .popup-content .popup-status-text.partial {
            color: #ffaa00;
        }
        .popup-content .popup-status-text.pinging {
            color: #ffaa00;
            animation: pulse-ping 0.8s ease-in-out infinite;
        }

        .leaflet-marker-icon {
            cursor: pointer !important;
            background: transparent !important;
            border: none !important;
        }

        @media (max-width: 1024px) {
            .device-panel {
                width: 340px;
                min-width: 340px;
            }
        }

        @media (max-width: 768px) {
            .device-panel {
                width: 280px;
                min-width: 280px;
            }
            .hud-stats {
                gap: 6px;
            }
            .hud-stat {
                padding: 4px 10px;
                font-size: 10px;
            }
            .hud-stat .value {
                font-size: 13px;
            }
            .hud-title {
                font-size: 15px;
            }
            .device-item .location-name {
                max-width: 140px;
            }
            .jb-marker .marker-label {
                font-size: 7px;
                padding: 1px 4px;
            }
            .jb-marker .marker-dot {
                width: 12px;
                height: 12px;
            }
        }

        @media (max-width: 600px) {
            .device-panel {
                width: 100%;
                min-width: unset;
                height: 45vh;
                border-right: none;
                border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            }
            .main-container {
                flex-direction: column;
                height: calc(100vh - 70px);
            }
            #map {
                height: 55vh;
            }
            .hud-bar {
                padding: 8px 16px;
            }
            .hud-stats {
                gap: 4px;
                justify-content: center;
                width: 100%;
            }
            .hud-left {
                width: 100%;
                justify-content: center;
            }
            .hud-title {
                font-size: 14px;
            }
            .search-wrapper input {
                font-size: 12px;
                padding: 8px 14px 8px 38px;
            }
            .search-shortcut {
                display: none;
            }
            .jb-marker .marker-label {
                font-size: 6px;
                padding: 0px 3px;
            }
            .jb-marker .marker-dot {
                width: 10px;
                height: 10px;
            }
        }
    </style>
</head>
<body>

    <div class="hud-bar">
        <div class="hud-left">
            <div class="hud-icon">🛡️</div>
            <div>
                <div class="hud-title">CCTV CAMERA STATUS</div>
                <div class="hud-title-sub">REAL-TIME MONITORING SYSTEM</div>
            </div>
        </div>
        <div class="hud-stats">
            <div class="hud-stat">
                <span class="label">Total JB</span>
                <span class="value total" id="totalJB">0</span>
            </div>
            <div class="hud-stat">
                <span class="label">Total Cam</span>
                <span class="value total" id="totalCam">0</span>
            </div>
            <div class="hud-stat">
                <span class="status-dot online"></span>
                <span class="label">Online</span>
                <span class="value online" id="onlineCount">0</span>
            </div>
            <div class="hud-stat">
                <span class="status-dot offline"></span>
                <span class="label">Offline</span>
                <span class="value offline" id="offlineCount">0</span>
            </div>
        </div>
    </div>

    <div class="main-container">

        <div class="device-panel" id="devicePanel">
            <div class="search-section">
                <div class="search-wrapper">
                    <span class="search-icon"></span>
                    <input type="text" id="searchInput" placeholder="Search JB, IP, or Location..." />
                </div>
                <span class="search-shortcut"></span>
            </div>

            <div class="panel-header">
                <span class="title"> JB-Count</span>
                <span class="count" id="deviceCount">0</span>
            </div>

            <div class="device-list-container">
                <div id="deviceList">
                    <div class="loading-text">
                        <span class="spinner"></span> Loading cameras...
                    </div>
                </div>
            </div>
        </div>

        <div id="map"></div>
    </div>

    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js">
    </script>

    <script>
        // ============================================================
        // COMPLETE DATA: 180 JB Locations with IPs
        // ============================================================

        const cameraData = [{
            "jb": "JB-1",
            "location": "Mission Street – Near Archies",
            "lat": 11.933654,
            "lng": 79.830788,
            "ips": ["10.110.10.87", "10.110.10.88", "10.110.10.89", "10.110.10.90"]
        }, {
            "jb": "JB-2",
            "location": "Mission Street – Near De La Cathedral Church",
            "lat": 11.932950,
            "lng": 79.830705,
            "ips": ["10.110.10.101", "10.110.10.102", "10.110.10.103"]
        }, {
            "jb": "JB-3",
            "location": "Mission Street – Near Immaculate Heart of Mary Girls Sr. Secondary School",
            "lat": 11.932154,
            "lng": 79.830529,
            "ips": ["10.110.10.91", "10.110.10.92", "10.110.10.93", "10.110.10.94"]
        }, {
            "jb": "JB-4",
            "location": "Mission Street – Opp. Nandu Brandy Shop, Bussy Street Mission Street Junction",
            "lat": 11.929153,
            "lng": 79.830023,
            "ips": ["10.110.10.11", "10.110.10.12", "10.110.10.13"]
        }, {
            "jb": "JB-5",
            "location": "Mission Street – Near Nilgiris & Dominos",
            "lat": 11.934816,
            "lng": 79.831005,
            "ips": ["10.110.10.104", "10.110.10.105", "10.110.10.106"]
        }, {
            "jb": "JB-6",
            "location": "Mission Street – Near Bata Showroom",
            "lat": 11.935785,
            "lng": 79.831167,
            "ips": ["10.110.10.83", "10.110.10.84", "10.110.10.85", "10.110.10.86"]
        }, {
            "jb": "JB-7",
            "location": "Mission Street – Near Kids World",
            "lat": 11.938125,
            "lng": 79.831604,
            "ips": ["10.110.10.76", "10.110.10.77", "10.110.10.78"]
        }, {
            "jb": "JB-8",
            "location": "MG Road – Near Vardharaja Perumal Temple",
            "lat": 11.941129,
            "lng": 79.830216,
            "ips": ["10.110.3.10", "10.110.3.11", "10.110.3.12"]
        }, {
            "jb": "JB-9",
            "location": "MG Road – Near Kamatchi Ammal Kovil",
            "lat": 11.938936,
            "lng": 79.829820,
            "ips": ["10.110.3.13", "10.110.3.14", "10.110.3.15"]
        }, {
            "jb": "JB-10",
            "location": "MG Road – Near KBS Kofi",
            "lat": 11.937361,
            "lng": 79.829501,
            "ips": ["10.110.3.16", "10.110.3.17", "10.110.3.18", "10.110.3.19"]
        }, {
            "jb": "JB-11",
            "location": "MG Road – Near Royal Collection",
            "lat": 11.936114,
            "lng": 79.829295,
            "ips": ["10.110.3.20", "10.110.3.21", "10.110.3.22", "10.110.3.23"]
        }, {
            "jb": "JB-12",
            "location": "MG Road – Near KFC",
            "lat": 11.935143,
            "lng": 79.829135,
            "ips": ["10.110.3.24", "10.110.3.25", "10.110.3.26", "10.110.3.27"]
        }, {
            "jb": "JB-13",
            "location": "MG Road – Near Burma Hotel",
            "lat": 11.930757,
            "lng": 79.828283,
            "ips": ["10.110.3.140", "10.110.3.141", "10.110.3.142", "10.110.3.143"]
        }, {
            "jb": "JB-14",
            "location": "MG Road – Near Clock Tower Hotel",
            "lat": 11.929545,
            "lng": 79.827906,
            "ips": ["10.110.3.144", "10.110.3.145", "10.110.3.146", "10.110.3.147"]
        }, {
            "jb": "JB-15",
            "location": "MG Road – Near Sacred Heart Church",
            "lat": 11.925504,
            "lng": 79.827228,
            "ips": ["10.110.11.204", "10.110.11.205", "10.110.11.206"]
        }, {
            "jb": "JB-16",
            "location": "MG Road – Near Government Women's College",
            "lat": 11.944475,
            "lng": 79.830807,
            "ips": ["10.110.1.142", "10.110.1.143"]
        }, {
            "jb": "JB-17",
            "location": "MG Road – Near Muthialpet Police Station",
            "lat": 11.947663,
            "lng": 79.831373,
            "ips": ["10.110.1.140", "10.110.1.141"]
        }, {
            "jb": "JB-18",
            "location": "MG Road – Near Rajendra Pillai Complex",
            "lat": 11.956724,
            "lng": 79.833196,
            "ips": ["10.110.0.211", "10.110.0.212"]
        }, {
            "jb": "JB-19",
            "location": "Bussy Street – Near Bank of India",
            "lat": 11.928996,
            "lng": 79.830766,
            "ips": ["10.110.10.14", "10.110.10.15", "10.110.10.16", "10.110.10.17"]
        }, {
            "jb": "JB-20",
            "location": "Bussy Street – Near Spice Route Pub",
            "lat": 11.928383,
            "lng": 79.833593,
            "ips": ["10.110.11.11", "10.110.11.12", "10.110.11.13", "10.110.11.14"]
        }, {
            "jb": "JB-21",
            "location": "Bussy Street – Near PWD Office & Karthika Cafe",
            "lat": 11.928644,
            "lng": 79.832349,
            "ips": ["10.110.9.11", "10.110.9.12", "10.110.9.13"]
        }, {
            "jb": "JB-22",
            "location": "Bussy Street – Near Canal & White Town Liquor Shop",
            "lat": 11.928838,
            "lng": 79.831475,
            "ips": ["10.110.10.18", "10.110.10.19", "10.110.10.20", "10.110.10.21"]
        }, {
            "jb": "JB-23",
            "location": "Bussy Street – White Town Near Beach Entrance 3",
            "lat": 11.928251,
            "lng": 79.834333,
            "ips": ["10.110.11.15", "10.110.11.16"]
        }, {
            "jb": "JB-24",
            "location": "Bussy Street – Near Jayaram High School",
            "lat": 11.929928,
            "lng": 79.826190,
            "ips": ["10.110.2.140", "10.110.2.141"]
        }, {
            "jb": "JB-25",
            "location": "Near Mudaliarpet, Opp. RTO Office",
            "lat": 11.919606,
            "lng": 79.809042,
            "ips": ["10.110.7.11", "10.110.7.12", "10.110.7.13", "10.110.7.14"]
        }, {
            "jb": "JB-26",
            "location": "Natesan Nagar Street, Near 100 Feet Road",
            "lat": 11.928283,
            "lng": 79.807317,
            "ips": ["10.110.7.15", "10.110.7.16"]
        }, {
            "jb": "JB-27",
            "location": "Nellithope Junction",
            "lat": 11.932869,
            "lng": 79.812081,
            "ips": ["10.110.5.14", "10.110.5.15"]
        }, {
            "jb": "JB-28",
            "location": "Sathani Street",
            "lat": 11.936489,
            "lng": 79.816815,
            "ips": ["10.110.5.80", "10.110.5.81"]
        }, {
            "jb": "JB-29",
            "location": "Kamaraja Junction Near GRT Jewelleries",
            "lat": 11.937355,
            "lng": 79.821628,
            "ips": ["10.110.4.140", "10.110.4.141"]
        }, {
            "jb": "JB-30",
            "location": "Raja Theatre Junction",
            "lat": 11.936883,
            "lng": 79.825130,
            "ips": ["10.110.3.79", "10.110.3.80", "10.110.3.81", "10.110.3.82"]
        }, {
            "jb": "JB-31",
            "location": "Botanical Garden",
            "lat": 11.928118,
            "lng": 79.824396,
            "ips": ["10.110.11.207", "10.110.11.208"]
        }, {
            "jb": "JB-32",
            "location": "Anna Salai Junction _1",
            "lat": 11.930456,
            "lng": 79.823803,
            "ips": ["10.110.2.210", "10.110.2.211", "10.110.2.212"]
        }, {
            "jb": "JB-33",
            "location": "Providance mall",
            "lat": 11.929187,
            "lng": 79.819833,
            "ips": ["10.110.8.76", "10.110.8.77"]
        }, {
            "jb": "JB-34",
            "location": "Intregrated court complex",
            "lat": 11.927963,
            "lng": 79.819211,
            "ips": ["10.110.8.140", "10.110.8.141", "10.110.8.142"]
        }, {
            "jb": "JB-35",
            "location": "Mudaliarpet junction",
            "lat": 11.922407,
            "lng": 79.816558,
            "ips": ["10.110.8.143", "10.110.8.144"]
        }, {
            "jb": "JB-36",
            "location": "Mudaliarpet Police station",
            "lat": 11.921120,
            "lng": 79.815214,
            "ips": ["10.110.8.145", "10.110.8.146", "10.110.8.147"]
        }, {
            "jb": "JB-37",
            "location": "Kamaraja salai junction, near Lenin street",
            "lat": 11.940195,
            "lng": 79.814326,
            "ips": ["10.110.4.204", "10.110.4.205", "10.110.4.206"]
        }, {
            "jb": "JB-38",
            "location": "Lenin street entrance near Indian Bank",
            "lat": 11.933509,
            "lng": 79.812711,
            "ips": ["10.110.5.76", "10.110.5.77"]
        }, {
            "jb": "JB-39",
            "location": "Thiravallur salai, Kosapalam road near Kumar Engineering College",
            "lat": 11.935668,
            "lng": 79.815030,
            "ips": ["10.110.5.78", "10.110.5.79"]
        }, {
            "jb": "JB-40",
            "location": "Kamaraja salai street opp SBI Bank",
            "lat": 11.938382,
            "lng": 79.817641,
            "ips": ["10.110.4.142", "10.110.4.143"]
        }, {
            "jb": "JB-41",
            "location": "Kamaraja salai New Saram, near Banana Leaf",
            "lat": 11.939582,
            "lng": 79.815700,
            "ips": ["10.110.4.207", "10.110.4.208", "10.110.4.209"]
        }, {
            "jb": "JB-42",
            "location": "Othaivadai street, New Saram, near Surya Designs",
            "lat": 11.941007,
            "lng": 79.816158,
            "ips": ["10.110.4.210", "10.110.4.211"]
        }, {
            "jb": "JB-43",
            "location": "Chinayanpet main road, Thendral Nagar, New Saram",
            "lat": 11.942576,
            "lng": 79.816795,
            "ips": ["10.110.4.212", "10.110.4.213"]
        }, {
            "jb": "JB-44",
            "location": "Vallar Salai Extension 45 Feet Road, Venkata Nagar, Auto Stand",
            "lat": 11.941704,
            "lng": 79.821841,
            "ips": ["10.110.4.144", "10.110.4.145"]
        }, {
            "jb": "JB-45",
            "location": "Rainbow Park, Venkata Nagar",
            "lat": 11.941447,
            "lng": 79.822821,
            "ips": ["10.110.4.75", "10.110.4.76"]
        }, {
            "jb": "JB-46",
            "location": "45 Feet Road, Rajeshwari Nagar, near Vairam Fitness Center",
            "lat": 11.940673,
            "lng": 79.826306,
            "ips": ["10.110.2.15", "10.110.2.16"]
        }, {
            "jb": "JB-47",
            "location": "Anna Salai Road opp Jain Temple",
            "lat": 11.940103,
            "lng": 79.826842,
            "ips": ["10.110.2.13", "10.110.2.14"]
        }, {
            "jb": "JB-48",
            "location": "Sardar Vallabhai Patel Road, near Ananda Inn Hotel",
            "lat": 11.941757,
            "lng": 79.828419,
            "ips": ["10.110.2.11", "10.110.2.12"]
        }, {
            "jb": "JB-49",
            "location": "Karuvadikuppam Main Road near Kamarajar Mandapam",
            "lat": 11.957657,
            "lng": 79.828122,
            "ips": ["10.110.0.206", "10.110.0.207", "10.110.0.208"]
        }, {
            "jb": "JB-50",
            "location": "ECR Road opp Vivekananda School",
            "lat": 11.953720,
            "lng": 79.820320,
            "ips": ["10.110.0.144", "10.110.0.145"]
        }, {
            "jb": "JB-51",
            "location": "ECR Road, Lawspet near Sankara Vidhyala Higher Secondary School",
            "lat": 11.951294,
            "lng": 79.816520,
            "ips": ["10.110.0.104", "10.110.0.105"]
        }, {
            "jb": "JB-52",
            "location": "Kamaraja Salai Road, Saram near Directorate of Economics and Statistics Office",
            "lat": 11.940920,
            "lng": 79.812206,
            "ips": ["10.110.4.80", "10.110.4.81"]
        }, {
            "jb": "JB-53",
            "location": "Manakula Vinayagar Temple",
            "lat": 11.936033,
            "lng": 79.833800,
            "ips": ["10.110.9.14", "10.110.9.15"]
        }, {
            "jb": "JB-54",
            "location": "Francois Martin Street",
            "lat": 11.935919,
            "lng": 79.834408,
            "ips": ["10.110.9.16", "10.110.9.17"]
        }, {
            "jb": "JB-55",
            "location": "Beach Entrance Road, near KBS Kofi Bar",
            "lat": 11.935638,
            "lng": 79.835924,
            "ips": ["10.110.10.140", "10.110.10.141"]
        }, {
            "jb": "JB-56",
            "location": "Campagne Street, White Town, near Park",
            "lat": 11.933591,
            "lng": 79.835139,
            "ips": ["10.110.10.142", "10.110.10.143"]
        }, {
            "jb": "JB-57",
            "location": "Campagne Street, White Town, near Library",
            "lat": 11.934003,
            "lng": 79.835188,
            "ips": ["10.110.10.144", "10.110.10.145"]
        }, {
            "jb": "JB-58",
            "location": "Netaji Subhash Chandra Bose Salai near Railway Station Cross Road",
            "lat": 11.925580,
            "lng": 79.830931,
            "ips": ["10.110.10.22", "10.110.10.23"]
        }, {
            "jb": "JB-59",
            "location": "Rue damas street, white town near beach entrance 1",
            "lat": 11.927373,
            "lng": 79.834170,
            "ips": ["10.110.11.17", "10.110.11.18"]
        }, {
            "jb": "JB-60",
            "location": "Police head quarters, white town",
            "lat": 11.931014,
            "lng": 79.834915,
            "ips": ["10.110.10.168", "10.110.10.169"]
        }, {
            "jb": "JB-61",
            "location": "Rue due bazar saint laurant, white town near EVA guest house",
            "lat": 11.927531,
            "lng": 79.833367,
            "ips": ["10.110.11.21", "10.110.11.22"]
        }, {
            "jb": "JB-62",
            "location": "100 feet road, near Rajeev Gandhi Women and Children Government Hospital",
            "lat": 11.936639,
            "lng": 79.807859,
            "ips": ["10.110.3.204", "10.110.3.205", "10.110.3.206"]
        }, {
            "jb": "JB-63",
            "location": "Industrial estate Thattanchavady near Directorate of Industries and Commerce",
            "lat": 11.943196,
            "lng": 79.804599,
            "ips": ["10.110.5.140", "10.110.5.141"]
        }, {
            "jb": "JB-64",
            "location": "Vazhudavoor road collectrate",
            "lat": 11.941606,
            "lng": 79.805873,
            "ips": ["10.110.5.204", "10.110.5.205"]
        }, {
            "jb": "JB-65",
            "location": "Airport road near NCC unit canteen",
            "lat": 11.965594,
            "lng": 79.811707,
            "ips": ["10.110.1.11", "10.110.1.12"]
        }, {
            "jb": "JB-66",
            "location": "Airport road near Tagore Arts College",
            "lat": 11.962501,
            "lng": 79.810461,
            "ips": ["10.110.1.13", "10.110.1.14"]
        }, {
            "jb": "JB-67",
            "location": "Airport road Women Polytechnic College",
            "lat": 11.960102,
            "lng": 79.810220,
            "ips": ["10.110.1.15", "10.110.1.16"]
        }, {
            "jb": "JB-68",
            "location": "Airport road Kurunji Nagar extension at Nissan service center",
            "lat": 11.958906,
            "lng": 79.810118,
            "ips": ["10.110.1.17", "10.110.1.18"]
        }, {
            "jb": "JB-69",
            "location": "Airport road, Netaji Subhash Chandra Bose statue",
            "lat": 11.957181,
            "lng": 79.816813,
            "ips": ["10.110.1.19", "10.110.1.20"]
        }, {
            "jb": "JB-70",
            "location": "Anna Salai road near Samsung showroom",
            "lat": 11.931986,
            "lng": 79.833842,
            "ips": ["10.110.11.19", "10.110.11.20"]
        }, {
            "jb": "JB-71",
            "location": "Campagne street, White Town near Ponlait dairy",
            "lat": 11.932825,
            "lng": 79.834950,
            "ips": ["10.110.10.146", "10.110.10.147"]
        }, {
            "jb": "JB-72",
            "location": "Shivaji Junction",
            "lat": 11.956265,
            "lng": 79.826540,
            "ips": ["10.110.0.203", "10.110.0.204", "10.110.0.205"]
        }, {
            "jb": "JB-73",
            "location": "Maduvapet junction -1",
            "lat": 11.952363,
            "lng": 79.818462,
            "ips": ["10.110.0.140", "10.110.0.141"]
        }, {
            "jb": "JB-74",
            "location": "Maduvapet junction -2",
            "lat": 11.952484,
            "lng": 79.818410,
            "ips": ["10.110.0.142", "10.110.0.143"]
        }, {
            "jb": "JB-75",
            "location": "Latha Steel Junction",
            "lat": 11.948362,
            "lng": 79.813054,
            "ips": ["10.110.0.106", "10.110.0.110"]
        }, {
            "jb": "JB-76",
            "location": "Kokku Park",
            "lat": 11.943647,
            "lng": 79.808599,
            "ips": ["10.110.0.11", "10.110.0.12"]
        }, {
            "jb": "JB-77",
            "location": "Kokku Park",
            "lat": 11.943751,
            "lng": 79.808727,
            "ips": ["10.110.0.13", "10.110.0.14"]
        }, {
            "jb": "JB-78",
            "location": "Rajiv Gandhi Junction",
            "lat": 11.941527,
            "lng": 79.808250,
            "ips": ["10.110.6.76", "10.110.6.77", "10.110.6.78"]
        }, {
            "jb": "JB-79",
            "location": "Rajiv Gandhi Junction",
            "lat": 11.941626,
            "lng": 79.808275,
            "ips": ["10.110.6.79", "10.110.6.80"]
        }, {
            "jb": "JB-80",
            "location": "Rajiv Gandhi Junction",
            "lat": 11.941667,
            "lng": 79.807641,
            "ips": ["10.110.6.140", "10.110.6.141"]
        }, {
            "jb": "JB-81",
            "location": "Indira Gandhi Junction",
            "lat": 11.931630,
            "lng": 79.807490,
            "ips": ["10.110.6.204", "10.110.6.205"]
        }, {
            "jb": "JB-82",
            "location": "Indira Gandhi Junction",
            "lat": 11.931685,
            "lng": 79.807533,
            "ips": ["10.110.6.206"]
        }, {
            "jb": "JB-83",
            "location": "Maraimalai Adigal Salai Cross Road Junction",
            "lat": 11.931108,
            "lng": 79.820511,
            "ips": ["10.110.8.78", "10.110.8.79", "10.110.8.80", "10.110.8.81"]
        }, {
            "jb": "JB-84",
            "location": "Anna Salai Junction _2",
            "lat": 11.930277,
            "lng": 79.823818,
            "ips": ["10.110.2.213", "10.110.2.214"]
        }, {
            "jb": "JB-85",
            "location": "Ajantha Signal Junction _1",
            "lat": 11.942085,
            "lng": 79.830310,
            "ips": ["10.110.1.76", "10.110.1.77"]
        }, {
            "jb": "JB-86",
            "location": "Ajantha Signal Junction _2",
            "lat": 11.941926,
            "lng": 79.830420,
            "ips": ["10.110.1.78", "10.110.1.79"]
        }, {
            "jb": "JB-87",
            "location": "100 feet Mudaliarpet near EPFO office",
            "lat": 11.922737,
            "lng": 79.808569,
            "ips": ["10.110.7.17", "10.110.7.18"]
        }, {
            "jb": "JB-88",
            "location": "100 feet road near Surguru restaurant",
            "lat": 11.934053,
            "lng": 79.807465,
            "ips": ["10.110.3.207", "10.110.3.208"]
        }, {
            "jb": "JB-89",
            "location": "RTC bus stand near Sabthagiri hotel",
            "lat": 11.932229,
            "lng": 79.815119,
            "ips": ["10.110.7.140", "10.110.7.141", "10.110.7.142"]
        }, {
            "jb": "JB-90",
            "location": "Jhansi Nagar, Karamanikuppam road",
            "lat": 11.926191,
            "lng": 79.805593,
            "ips": ["10.110.7.204", "10.110.7.205"]
        }, {
            "jb": "JB-91",
            "location": "Jamia Masjid, Mullaha street",
            "lat": 11.925806,
            "lng": 79.828623,
            "ips": ["10.110.11.209", "10.110.11.210"]
        }, {
            "jb": "JB-92",
            "location": "Shri Vadapuriswarar Temple, Ishwaran Kovil Street",
            "lat": 11.939434,
            "lng": 79.829987,
            "ips": ["10.110.3.28", "10.110.3.29"]
        }, {
            "jb": "JB-93",
            "location": "Sri Aurobindo Ashram",
            "lat": 11.936564,
            "lng": 79.833887,
            "ips": ["10.110.9.18", "10.110.9.19", "10.110.9.20", "10.110.9.21"]
        }, {
            "jb": "JB-94",
            "location": "ICCC",
            "lat": 11.948519,
            "lng": 79.814089,
            "ips": ["10.110.0.108", "10.110.0.109"]
        }, {
            "jb": "JB-95",
            "location": "SVP Salai - Old Distillery Junction",
            "lat": 11.939070,
            "lng": 79.836086,
            "ips": ["10.110.10.201", "10.110.10.202"]
        }, {
            "jb": "JB-96",
            "location": "SVP Salai - Gingee Salai Junction",
            "lat": 11.939469,
            "lng": 79.833576,
            "ips": ["10.110.10.203", "10.110.10.204"]
        }, {
            "jb": "JB-97",
            "location": "SVP Salai - Aambur Salai Junction",
            "lat": 11.940464,
            "lng": 79.833513,
            "ips": ["10.110.10.205", "10.110.10.206"]
        }, {
            "jb": "JB-98",
            "location": "SVP Salai - Mission Street Junction",
            "lat": 11.941255,
            "lng": 79.832181,
            "ips": ["10.110.10.207", "10.110.10.208", "10.110.10.209"]
        }, {
            "jb": "JB-99",
            "location": "Thengaithittu Marappalam junction",
            "lat": 11.914704,
            "lng": 79.810925,
            "ips": ["10.110.7.206", "10.110.7.207"]
        }, {
            "jb": "JB-100",
            "location": "Thengaithittu Marappalam junction",
            "lat": 11.914279,
            "lng": 79.810746,
            "ips": ["10.110.7.76", "10.110.7.77"]
        }, {
            "jb": "JB-101",
            "location": "AFT Mill Road- Cuddalore Road Junction",
            "lat": 11.923852,
            "lng": 79.817245,
            "ips": ["10.110.8.148", "10.110.8.149", "10.110.8.150"]
        }, {
            "jb": "JB-102",
            "location": "AFT Mill Road- Point Care Street Junction",
            "lat": 11.923701,
            "lng": 79.810952,
            "ips": ["10.110.7.19", "10.110.7.20", "10.110.7.21"]
        }, {
            "jb": "JB-103",
            "location": "Nainarmandapam junction",
            "lat": 11.910741,
            "lng": 79.809534,
            "ips": ["10.110.7.88", "10.110.7.89"]
        }, {
            "jb": "JB-104",
            "location": "Murungapakkam Junction",
            "lat": 11.906708,
            "lng": 79.807967,
            "ips": ["10.110.7.80", "10.110.7.81", "10.110.7.82"]
        }, {
            "jb": "JB-105",
            "location": "Muthiyalpet Manikoondu",
            "lat": 11.949043,
            "lng": 79.831660,
            "ips": ["10.110.0.213", "10.110.0.214", "10.110.0.215"]
        }, {
            "jb": "JB-106",
            "location": "Periyar Statue, Kamarajar salai",
            "lat": 11.937550,
            "lng": 79.819213,
            "ips": ["10.110.5.82", "10.110.5.83"]
        }, {
            "jb": "JB-107",
            "location": "Botanical garden entrance - Anna Jn - Rosema Thirumana",
            "lat": 11.930594,
            "lng": 79.822284,
            "ips": ["10.110.2.142", "10.110.2.143"]
        }, {
            "jb": "JB-108",
            "location": "New Bus stand - Nellithope Jn",
            "lat": 11.931984,
            "lng": 79.815652,
            "ips": ["10.110.7.143", "10.110.7.144"]
        }, {
            "jb": "JB-109",
            "location": "Schakralaya Tata Motors - Ariyankuppam bridge",
            "lat": 11.903312,
            "lng": 79.806304,
            "ips": ["10.110.7.83", "10.110.7.84", "10.110.7.85"]
        }, {
            "jb": "JB-110",
            "location": "7th gate Jipmer - 7th day church",
            "lat": 11.945325,
            "lng": 79.799946,
            "ips": ["10.110.5.142", "10.110.5.143"]
        }, {
            "jb": "JB-111",
            "location": "Kalki Medicals - Fathima blinds (Murga theare)",
            "lat": 11.943159,
            "lng": 79.804642,
            "ips": ["10.110.5.144", "10.110.5.145"]
        }, {
            "jb": "JB-112",
            "location": "Prasanna vaenkatesa perumal koil - Mercury Driving school",
            "lat": 11.942008,
            "lng": 79.798479,
            "ips": ["10.110.5.208", "10.110.5.209"]
        }, {
            "jb": "JB-113",
            "location": "GHS, Mettupalayam - Hotel Pushpa",
            "lat": 11.939503,
            "lng": 79.786935,
            "ips": ["10.110.6.142", "10.110.6.143"]
        }, {
            "jb": "JB-114",
            "location": "Indian overseas bank, Rediyarpalayam",
            "lat": 11.930883,
            "lng": 79.797020,
            "ips": ["10.110.6.11", "10.110.6.12"]
        }, {
            "jb": "JB-115",
            "location": "Jaya Nagar junction, Rediyarpalayam",
            "lat": 11.930742,
            "lng": 79.791513,
            "ips": ["10.110.6.13", "10.110.6.14"]
        }, {
            "jb": "JB-116",
            "location": "Kokku park - Blue fox bad & Restaurant",
            "lat": 11.943251,
            "lng": 79.809060,
            "ips": ["10.110.0.15"]
        }, {
            "jb": "JB-117",
            "location": "Shri Amman temple - Laxmi Granites (latha steels)",
            "lat": 11.948407,
            "lng": 79.813004,
            "ips": ["10.110.0.107", "10.110.0.111"]
        }, {
            "jb": "JB-118",
            "location": "Anna salai - Sri Aurobindo street",
            "lat": 11.939087,
            "lng": 79.826135,
            "ips": ["10.110.2.20", "10.110.2.21"]
        }, {
            "jb": "JB-119",
            "location": "Anna salai - Anandha Ranga pillai street",
            "lat": 11.935889,
            "lng": 79.824810,
            "ips": ["10.110.2.73", "10.110.2.74", "10.110.2.75"]
        }, {
            "jb": "JB-120",
            "location": "Anna Salai - Vellala Street",
            "lat": 11.935315,
            "lng": 79.824809,
            "ips": ["10.110.2.215", "10.110.2.216", "10.110.2.217"]
        }, {
            "jb": "JB-121",
            "location": "Anna Salai - Needarajapayar street",
            "lat": 11.934762,
            "lng": 79.824797,
            "ips": ["10.110.2.81", "10.110.2.82"]
        }, {
            "jb": "JB-122",
            "location": "Anna salai - Thambu naicker street",
            "lat": 11.933926,
            "lng": 79.824518,
            "ips": ["10.110.2.86", "10.110.2.87", "10.110.2.88"]
        }, {
            "jb": "JB-123",
            "location": "Anna salai - Petit cannal street",
            "lat": 11.932897,
            "lng": 79.824352,
            "ips": ["10.110.2.76", "10.110.2.77", "10.110.2.78"]
        }, {
            "jb": "JB-124",
            "location": "Anna salai - Savariravalu street",
            "lat": 11.932487,
            "lng": 79.824231,
            "ips": ["10.110.2.218", "10.110.2.219", "10.110.2.220"]
        }, {
            "jb": "JB-125",
            "location": "Anna salai - Laporte street",
            "lat": 11.932000,
            "lng": 79.824088,
            "ips": ["10.110.2.95", "10.110.2.96", "10.110.2.97"]
        }, {
            "jb": "JB-126",
            "location": "South Boolevard- Thillai Mestry Street",
            "lat": 11.928713,
            "lng": 79.824468,
            "ips": ["10.110.11.211", "10.110.11.212"]
        }, {
            "jb": "JB-127",
            "location": "South Boolevard- Badeer Sahib Street",
            "lat": 11.927470,
            "lng": 79.824614,
            "ips": ["10.110.11.213", "10.110.11.214", "10.110.11.215"]
        }, {
            "jb": "JB-128",
            "location": "South Boolevard- Bharathi Street",
            "lat": 11.926384,
            "lng": 79.825491,
            "ips": ["10.110.11.216", "10.110.11.217", "10.110.11.218"]
        }, {
            "jb": "JB-129",
            "location": "South Boolevard- Rue latouchne street",
            "lat": 11.925890,
            "lng": 79.826314,
            "ips": ["10.110.11.219", "10.110.11.220", "10.110.11.221"]
        }, {
            "jb": "JB-130",
            "location": "Subbaiahya Salai- Elaiyamman kovil Street",
            "lat": 11.925210,
            "lng": 79.828486,
            "ips": ["10.110.11.222", "10.110.11.223", "10.110.11.224"]
        }, {
            "jb": "JB-131",
            "location": "Subbaiahya Salai- Chandasahib Street",
            "lat": 11.925016,
            "lng": 79.829643,
            "ips": ["10.110.11.225", "10.110.11.226", "10.110.11.227"]
        }, {
            "jb": "JB-132",
            "location": "Subbaiahya Salai- Nethaji Suboschandrabose Salai",
            "lat": 11.924858,
            "lng": 79.830772,
            "ips": ["10.110.10.31", "10.110.10.32", "10.110.10.33", "10.110.10.34"]
        }, {
            "jb": "JB-133",
            "location": "South Boolevard- Labour Donnais street",
            "lat": 11.924716,
            "lng": 79.831662,
            "ips": ["10.110.11.25", "10.110.11.26", "10.110.11.27"]
        }, {
            "jb": "JB-134",
            "location": "South Boolevard- Rue Suffren Street",
            "lat": 11.924786,
            "lng": 79.832053,
            "ips": ["10.110.11.28", "10.110.11.29", "10.110.11.30"]
        }, {
            "jb": "JB-135",
            "location": "South Boolevard- Romain Rolland street",
            "lat": 11.925132,
            "lng": 79.832766,
            "ips": ["10.110.11.31", "10.110.11.32", "10.110.11.33"]
        }, {
            "jb": "JB-136",
            "location": "South Boolevard- Dumas Street",
            "lat": 11.925474,
            "lng": 79.833745,
            "ips": ["10.110.11.34", "10.110.11.35"]
        }, {
            "jb": "JB-137",
            "location": "Goubert Avenue (Beach Road)-St.Martin Street",
            "lat": 11.935687,
            "lng": 79.835560,
            "ips": ["10.110.10.148", "10.110.10.149", "10.110.10.150"]
        }, {
            "jb": "JB-138",
            "location": "Goubert Avenue (Beach Road)-Marine Street",
            "lat": 11.936284,
            "lng": 79.835340,
            "ips": ["10.110.10.151", "10.110.10.152", "10.110.10.153"]
        }, {
            "jb": "JB-139",
            "location": "Goubert Avenue (Beach Road)-St.Gilles Street",
            "lat": 11.936807,
            "lng": 79.835447,
            "ips": ["10.110.10.154", "10.110.10.155", "10.110.10.156"]
        }, {
            "jb": "JB-140",
            "location": "Goubert Avenue (Beach Road)-Dupui Street",
            "lat": 11.937374,
            "lng": 79.835610,
            "ips": ["10.110.10.157", "10.110.10.158", "10.110.10.159"]
        }, {
            "jb": "JB-141",
            "location": "Goubert Avenue (Beach Road)-Des Bassaymsde Richrmont Street",
            "lat": 11.937934,
            "lng": 79.835731,
            "ips": ["10.110.10.160", "10.110.10.161", "10.110.10.162"]
        }, {
            "jb": "JB-142",
            "location": "Goubert Avenue (Beach Road)-St.Louis Street",
            "lat": 11.938433,
            "lng": 79.835939,
            "ips": ["10.110.10.163", "10.110.10.164"]
        }, {
            "jb": "JB-143",
            "location": "Sarder Vallabhai Patel Salai (North Boolevard)- Francis Martin Street",
            "lat": 11.939567,
            "lng": 79.835335,
            "ips": ["10.110.10.210", "10.110.10.211", "10.110.10.212"]
        }, {
            "jb": "JB-144",
            "location": "Sardar Vallabhai Patel Salai (North Boolevard)- Manakula Vinayakar kovil street",
            "lat": 11.939789,
            "lng": 79.834460,
            "ips": ["10.110.10.213", "10.110.10.214", "10.110.10.215"]
        }, {
            "jb": "JB-145",
            "location": "Sarder Vallabhai Patel Salai (North Boolevard)- H.M Kassim Street",
            "lat": 11.940310,
            "lng": 79.833835,
            "ips": ["10.110.10.216", "10.110.10.217"]
        }, {
            "jb": "JB-146",
            "location": "Needarajapayar Street- Mission Street",
            "lat": 11.934572,
            "lng": 79.832444,
            "ips": ["10.110.10.107", "10.110.10.108", "10.110.10.109"]
        }, {
            "jb": "JB-147",
            "location": "Bharathi street-Needarajapayar Street",
            "lat": 11.934357,
            "lng": 79.827033,
            "ips": ["10.110.2.144", "10.110.2.145", "10.110.2.146"]
        }, {
            "jb": "JB-148",
            "location": "Jeeva Colony Airport Road",
            "lat": 11.948814,
            "lng": 79.811724,
            "ips": ["10.110.1.21", "10.110.1.22"]
        }, {
            "jb": "JB-149",
            "location": "Mission Street- Near Aura Hotel",
            "lat": 11.932499,
            "lng": 79.830727,
            "ips": ["10.110.10.24", "10.110.10.25", "10.110.10.26"]
        }, {
            "jb": "JB-150",
            "location": "Mission Street- Near Pasta Vento Restaurant",
            "lat": 11.929797,
            "lng": 79.830143,
            "ips": ["10.110.10.27", "10.110.10.28", "10.110.10.29", "10.110.10.30"]
        }, {
            "jb": "JB-151",
            "location": "Jawaharlal Nehru St near Universal Trading and Training Academy",
            "lat": 11.935327,
            "lng": 79.833650,
            "ips": ["10.110.9.22", "10.110.9.23", "10.110.9.24"]
        }, {
            "jb": "JB-152",
            "location": "Mission Street - Near Diva Showroom",
            "lat": 11.937038,
            "lng": 79.831394,
            "ips": ["10.110.10.79", "10.110.10.80", "10.110.10.81", "10.110.10.82"]
        }, {
            "jb": "JB-153",
            "location": "Mission Street - Near Taka Pizza",
            "lat": 11.939743,
            "lng": 79.831953,
            "ips": ["10.110.10.97", "10.110.10.98", "10.110.10.99", "10.110.10.100"]
        }, {
            "jb": "JB-154",
            "location": "Lawspet Main Road near Jeeva Book Store",
            "lat": 11.954932,
            "lng": 79.818915,
            "ips": ["10.110.1.23", "10.110.1.24", "10.110.1.25"]
        }, {
            "jb": "JB-155",
            "location": "MG Road - Near HDFC ATM",
            "lat": 11.938441,
            "lng": 79.829740,
            "ips": ["10.110.3.30", "10.110.3.31", "10.110.3.32"]
        }, {
            "jb": "JB-156",
            "location": "MG Road - Near Maurya Textiles",
            "lat": 11.934066,
            "lng": 79.828797,
            "ips": ["10.110.3.148", "10.110.3.149", "10.110.3.150", "10.110.3.151"]
        }, {
            "jb": "JB-157",
            "location": "MG Road - Near Beauty 360",
            "lat": 11.931798,
            "lng": 79.828527,
            "ips": ["10.110.3.152", "10.110.3.153", "10.110.3.154"]
        }, {
            "jb": "JB-158",
            "location": "MG Road - Near Honda Showroom",
            "lat": 11.953755,
            "lng": 79.832474,
            "ips": ["10.110.0.216", "10.110.0.217"]
        }, {
            "jb": "JB-159",
            "location": "Nellithope Area",
            "lat": 11.931528,
            "lng": 79.809912,
            "ips": ["10.110.5.11", "10.110.5.12", "10.110.5.13"]
        }, {
            "jb": "JB-160",
            "location": "Kamaraja Salai, Balaji Street",
            "lat": 11.937477,
            "lng": 79.820188,
            "ips": ["10.110.4.77", "10.110.4.78", "10.110.4.79"]
        }, {
            "jb": "JB-161",
            "location": "Cuddalore Road, Near KG Meals",
            "lat": 11.916170,
            "lng": 79.811892,
            "ips": ["10.110.8.151", "10.110.8.152", "10.110.8.153"]
        }, {
            "jb": "JB-162",
            "location": "10th Cross Road, Brindavanam, Near TMB Bank",
            "lat": 11.942270,
            "lng": 79.818978,
            "ips": ["10.110.4.147", "10.110.4.148"]
        }, {
            "jb": "JB-163",
            "location": "Vazhudavoor Road, Navashakthi Nagar, Near Deepak Scans",
            "lat": 11.941848,
            "lng": 79.804639,
            "ips": ["10.110.5.206", "10.110.5.207"]
        }, {
            "jb": "JB-164",
            "location": "Maraimalai Adigal Salai Cross Road Junction",
            "lat": 11.932653,
            "lng": 79.812034,
            "ips": ["10.110.5.16", "10.110.5.17"]
        }, {
            "jb": "JB-165",
            "location": "Mudaliarpet Road, Near ICICI Bank",
            "lat": 11.923979,
            "lng": 79.808282,
            "ips": ["10.110.7.22", "10.110.7.23"]
        }, {
            "jb": "JB-166",
            "location": "100 Feet Road, Sundaraja Nagar, Near Stay In Hotel",
            "lat": 11.925531,
            "lng": 79.807771,
            "ips": ["10.110.7.208", "10.110.7.209"]
        }, {
            "jb": "JB-167",
            "location": "Jayaram Garden Entrance, Near Sabthagiri Market",
            "lat": 11.955327,
            "lng": 79.823319,
            "ips": ["10.110.0.146", "10.110.0.147", "10.110.0.148"]
        }, {
            "jb": "JB-168",
            "location": "Near Mudaliarpet Police Station, Puducherry",
            "lat": 11.921618,
            "lng": 79.815696,
            "ips": ["10.110.8.154", "10.110.8.155"]
        }, {
            "jb": "JB-169",
            "location": "F & F Supermarket – Marappalam Jn – Thengaithittu Rd Jn",
            "lat": 11.914837,
            "lng": 79.811179,
            "ips": ["10.110.7.210", "10.110.7.211"]
        }, {
            "jb": "JB-170",
            "location": "Indira Gandhi Junction",
            "lat": 11.931535,
            "lng": 79.807584,
            "ips": ["10.110.6.207", "10.110.6.208"]
        }, {
            "jb": "JB-171",
            "location": "Raymond Shop – Puducherry Hotel (Kamatchi)",
            "lat": 11.931220,
            "lng": 79.800062,
            "ips": ["10.110.6.15", "10.110.6.16"]
        }, {
            "jb": "JB-172",
            "location": "Anna Salai – Kamatchiaman Koil Street",
            "lat": 11.939587,
            "lng": 79.826447,
            "ips": ["10.110.2.17", "10.110.2.18", "10.110.2.19"]
        }, {
            "jb": "JB-173",
            "location": "Anna Salai – S.S. Pillai Street",
            "lat": 11.938551,
            "lng": 79.825930,
            "ips": ["10.110.2.22", "10.110.2.23", "10.110.2.24"]
        }, {
            "jb": "JB-174",
            "location": "Anna Salai – Diagou Moudaliar Street",
            "lat": 11.936391,
            "lng": 79.825061,
            "ips": ["10.110.2.79", "10.110.2.80"]
        }, {
            "jb": "JB-175",
            "location": "Anna Salai – Louis Praassin Street",
            "lat": 11.934259,
            "lng": 79.824611,
            "ips": ["10.110.2.83", "10.110.2.84", "10.110.2.85"]
        }, {
            "jb": "JB-176",
            "location": "Anna Salai – St. Therese Street",
            "lat": 11.933298,
            "lng": 79.824381,
            "ips": ["10.110.2.221", "10.110.2.222", "10.110.2.223"]
        }, {
            "jb": "JB-177",
            "location": "Goubert Avenue (Beach Road) – De Labourdonais Street",
            "lat": 11.931719,
            "lng": 79.835058,
            "ips": ["10.110.10.165", "10.110.10.166", "10.110.10.167"]
        }, {
            "jb": "JB-178",
            "location": "Goubert Avenue (Beach Road) – St. Louis Street",
            "lat": 11.938924,
            "lng": 79.836140,
            "ips": ["10.110.10.218", "10.110.10.219"]
        }, {
            "jb": "JB-179",
            "location": "Laporte Street – GH",
            "lat": 11.932065,
            "lng": 79.833124,
            "ips": ["10.110.9.25", "10.110.9.26", "10.110.9.27"]
        }, {
            "jb": "JB-180",
            "location": "Bharathi Street – Laporte Street",
            "lat": 11.931607,
            "lng": 79.826516,
            "ips": ["10.110.2.147", "10.110.2.148", "10.110.2.149"]
        }];

        // ============================================================
        // APP LOGIC
        // ============================================================

        const devices = cameraData.map(cam => {
            const ipStatuses = cam.ips.map(ip => ({
                ip: ip,
                status: 'pinging'
            }));
            return {
                ...cam,
                ipStatuses: ipStatuses,
                onlineCount: 0,
                totalCount: ipStatuses.length,
                overallStatus: 'pinging'
            };
        });

        const totalDevices = devices.length;
        const totalCameras = devices.reduce((sum, d) => sum + d.totalCount, 0);

        document.getElementById('totalJB').textContent = totalDevices;
        document.getElementById('totalCam').textContent = totalCameras;
        document.getElementById('onlineCount').textContent = 0;
        document.getElementById('offlineCount').textContent = 0;
        document.getElementById('deviceCount').textContent = totalDevices;

        // ============================================================
        // LEAFLET MAP
        // ============================================================

        const map = L.map('map', {
            center: [11.93, 79.83],
            zoom: 14,
            zoomControl: true,
            fadeAnimation: true,
            attributionControl: false
        });

        L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
            attribution: '',
            subdomains: 'abcd',
            maxZoom: 19,
            minZoom: 10
        }).addTo(map);

        map.zoomControl.setPosition('bottomright');

        L.control.scale({
            position: 'bottomleft',
            metric: true,
            imperial: false
        }).addTo(map);

        let markers = [];

        // ============================================================
        // CREATE MARKER WITH JB LABEL
        // ============================================================

        function createLabeledMarker(status, jb) {
            let color;
            let statusClass;
            if (status === 'online') {
                color = '#00cc77';
                statusClass = 'online';
            } else if (status === 'offline') {
                color = '#dd3355';
                statusClass = 'offline';
            } else if (status === 'partial') {
                color = '#ffaa00';
                statusClass = 'partial';
            } else {
                color = '#ffaa00';
                statusClass = 'pinging';
            }

            // Create a custom div with marker dot and label
            const div = document.createElement('div');
            div.className = `jb-marker`;
            div.innerHTML = `
                <div class="marker-dot ${statusClass}" style="background:${color};"></div>
                <div class="marker-label ${statusClass}">${jb}</div>
            `;
            return div;
        }

        // ============================================================
        // PING FUNCTION
        // ============================================================

        function pingSingleIp(ip) {
            return new Promise((resolve) => {
                const controller = new AbortController();
                const timeoutId = setTimeout(() => controller.abort(), 3000);

                fetch(`http://${ip}`, {
                        method: 'HEAD',
                        mode: 'no-cors',
                        signal: controller.signal
                    })
                    .then(() => {
                        clearTimeout(timeoutId);
                        resolve(true);
                    })
                    .catch(() => {
                        clearTimeout(timeoutId);
                        resolve(false);
                    });
            });
        }

        // ============================================================
        // UPDATE ALL DEVICES - PARALLEL PINGING
        // ============================================================

        let isUpdating = false;

        async function updateAllDeviceStatuses() {
            if (isUpdating) return;
            isUpdating = true;

            const pingTasks = [];
            const ipMap = [];

            for (const device of devices) {
                for (const ipInfo of device.ipStatuses) {
                    ipInfo.status = 'pinging';
                    ipMap.push({
                        device: device,
                        ipInfo: ipInfo
                    });
                    pingTasks.push(pingSingleIp(ipInfo.ip));
                }
            }

            const results = await Promise.all(pingTasks);

            let onlineTotal = 0;
            let offlineTotal = 0;

            for (let i = 0; i < results.length; i++) {
                const { device, ipInfo } = ipMap[i];
                const isOnline = results[i];
                ipInfo.status = isOnline ? 'online' : 'offline';
                if (isOnline) onlineTotal++;
                else offlineTotal++;
            }

            for (const device of devices) {
                const onlineCount = device.ipStatuses.filter(i => i.status === 'online').length;
                device.onlineCount = onlineCount;
                device.overallStatus = onlineCount === device.totalCount ? 'online' :
                    onlineCount > 0 ? 'partial' : 'offline';

                // Update marker
                const marker = markers.find(m => m.deviceData.jb === device.jb);
                if (marker) {
                    // Update marker icon with new status
                    const newIcon = createLabeledMarker(device.overallStatus, device.jb);
                    marker.setIcon(L.divIcon({
                        html: newIcon.outerHTML,
                        className: '',
                        iconSize: [60, 40],
                        iconAnchor: [30, 40],
                        popupAnchor: [0, -35]
                    }));

                    let ipsHtml = device.ipStatuses.map(ipInfo =>
                        `<div class="popup-ip-item">
                            <span class="ip-addr">${ipInfo.ip}</span>
                            <span class="ip-status ${ipInfo.status}">● ${ipInfo.status.toUpperCase()}</span>
                        </div>`
                    ).join('');

                    marker.setPopupContent(`
                        <div class="popup-content">
                            <div class="popup-jb">${device.jb}</div>
                            <div class="popup-location">${device.location}</div>
                            <div class="popup-divider"></div>
                            <div style="font-size:11px;color:#8899bb;margin-bottom:4px;">
                                ${device.onlineCount}/${device.totalCount} cameras online
                            </div>
                            ${ipsHtml}
                            <div class="popup-divider"></div>
                            <div class="popup-status-text ${device.overallStatus}">● ${device.overallStatus.toUpperCase()}</div>
                        </div>
                    `);
                }
            }

            document.getElementById('onlineCount').textContent = onlineTotal;
            document.getElementById('offlineCount').textContent = offlineTotal;

            renderDeviceList();

            isUpdating = false;
        }

        // ============================================================
        // RENDER DEVICE LIST
        // ============================================================

        let currentSearch = '';

        function getFilteredDevices() {
            let filtered = devices;
            if (currentSearch.trim() !== '') {
                const query = currentSearch.toLowerCase().trim();
                filtered = filtered.filter(d =>
                    d.jb.toLowerCase().includes(query) ||
                    d.location.toLowerCase().includes(query) ||
                    d.ips.some(ip => ip.includes(query))
                );
            }
            return filtered;
        }

        function renderDeviceList() {
            const filtered = getFilteredDevices();
            const container = document.getElementById('deviceList');

            document.getElementById('deviceCount').textContent = filtered.length;

            if (filtered.length === 0) {
                container.innerHTML = `<div class="no-results">No devices found matching your search.</div>`;
                return;
            }

            let html = '';
            filtered.forEach(device => {
                const statusClass = device.overallStatus;
                const statusLabel = device.overallStatus.toUpperCase();

                const ipPills = device.ipStatuses.map(ipInfo =>
                    `<span class="ip-pill ${ipInfo.status}">${ipInfo.ip}</span>`
                ).join('');

                html += `
                    <div class="device-item" data-jb="${device.jb}" onclick="zoomToDevice('${device.jb}')">
                        <div class="info">
                            <div class="top-row">
                                <span class="jb-name">${device.jb}</span>
                                <span class="camera-count">${device.onlineCount}/${device.totalCount}</span>
                            </div>
                            <span class="location-name">${device.location}</span>
                            <div class="ip-status-row">${ipPills}</div>
                            <div class="bottom-row">
                                <span class="status-badge ${statusClass}">${statusLabel}</span>
                            </div>
                        </div>
                    </div>
                `;
            });

            container.innerHTML = html;

            const visibleJbs = new Set(filtered.map(d => d.jb));
            markers.forEach(m => {
                if (visibleJbs.has(m.deviceData.jb)) {
                    if (!m._map) m.addTo(map);
                    m.setOpacity(1);
                } else {
                    if (m._map) m.setOpacity(0.15);
                }
            });
        }

        // ============================================================
        // ZOOM TO DEVICE
        // ============================================================

        window.zoomToDevice = function(jb) {
            const device = devices.find(d => d.jb === jb);
            if (device) {
                map.setView([device.lat, device.lng], 17, {
                    animate: true,
                    duration: 0.6
                });
                const marker = markers.find(m => m.deviceData.jb === jb);
                if (marker) {
                    marker.openPopup();
                }
            }
        };

        // ============================================================
        // INITIALIZE MAP MARKERS WITH JB LABELS
        // ============================================================

        devices.forEach(device => {
            // Create custom marker with JB label
            const markerElement = createLabeledMarker('pinging', device.jb);

            const icon = L.divIcon({
                html: markerElement.outerHTML,
                className: '',
                iconSize: [60, 40],
                iconAnchor: [30, 40],
                popupAnchor: [0, -35]
            });

            const marker = L.marker([device.lat, device.lng], {
                icon: icon,
                title: device.jb,
                riseOnHover: true
            }).addTo(map);

            // Build initial popup content
            let ipsHtml = device.ipStatuses.map(ipInfo =>
                `<div class="popup-ip-item">
                    <span class="ip-addr">${ipInfo.ip}</span>
                    <span class="ip-status pinging">● PINGING</span>
                </div>`
            ).join('');

            const popupContent = `
                <div class="popup-content">
                    <div class="popup-jb">${device.jb}</div>
                    <div class="popup-location">${device.location}</div>
                    <div class="popup-divider"></div>
                    <div style="font-size:11px;color:#8899bb;margin-bottom:4px;">
                        Checking ${device.totalCount} cameras...
                    </div>
                    ${ipsHtml}
                    <div class="popup-divider"></div>
                    <div class="popup-status-text pinging">● PINGING</div>
                </div>
            `;

            marker.bindPopup(popupContent, {
                className: 'google-popup',
                maxWidth: 280
            });

            marker.on('click', function() {
                this.openPopup();
            });

            marker.deviceData = device;
            markers.push(marker);
        });

        // ============================================================
        // SEARCH INPUT
        // ============================================================

        document.getElementById('searchInput').addEventListener('input', function() {
            currentSearch = this.value;
            renderDeviceList();
        });

        document.addEventListener('keydown', function(e) {
            if ((e.metaKey || e.ctrlKey) && e.key === 'k') {
                e.preventDefault();
                document.getElementById('searchInput').focus();
            }
        });

        // ============================================================
        // INITIAL RENDER & START PINGING
        // ============================================================

        renderDeviceList();
        updateAllDeviceStatuses();
        setInterval(updateAllDeviceStatuses, 5000);

        // ============================================================
        // RESIZE
        // ============================================================

        window.addEventListener('resize', () => {
            map.invalidateSize();
        });

        console.log(`✅ Puducherry Cyber Camera Control Room loaded`);
        console.log(`📍 ${totalDevices} JB locations`);
        console.log(`📹 ${totalCameras} total cameras`);
        console.log(`🔄 Pinging ALL ${totalCameras} IPs simultaneously every 5 seconds...`);
        console.log(`📍 Each map marker shows JB number label`);
    </script>

</body>
</html>
