<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>⚡ Minecraft Profile · Dev Icons</title>

    <!-- ===== MINECRAFT FONT ===== -->
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet" />

    <!-- ===== DEVICON (language & tool icons) ===== -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/devicon@2.16.0/devicon.min.css" />

    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #2d2d2d;
            font-family: 'Press Start 2P', 'Courier New', monospace;
            padding: 20px;
            background-image:
                repeating-linear-gradient(45deg,
                    #6b4c3b 0px, #6b4c3b 8px,
                    #5a3d2e 8px, #5a3d2e 16px),
                repeating-linear-gradient(-45deg,
                    #7a5c4a 0px, #7a5c4a 6px,
                    #5a3d2e 6px, #5a3d2e 12px);
            background-blend-mode: overlay;
            position: relative;
        }

        /* ===== GRASS TOP BAR ===== */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            height: 28px;
            background: repeating-linear-gradient(90deg,
                    #7cb342 0px, #7cb342 12px,
                    #689f38 12px, #689f38 24px);
            border-bottom: 4px solid #5d4037;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
        }

        /* ===== MAIN CARD ===== */
        .minecraft-card {
            max-width: 840px;
            width: 100%;
            background: #c6c6c6;
            border: 6px solid #4a4a4a;
            border-radius: 8px;
            padding: 24px 28px 20px;
            box-shadow:
                0 0 0 4px #2d2d2d,
                0 0 0 8px #6b4c3b,
                0 12px 60px rgba(0, 0, 0, 0.8);
            position: relative;
            transition: transform 0.2s;
            image-rendering: pixelated;
            animation: float 4s ease-in-out infinite;
        }

        .minecraft-card:hover {
            transform: translateY(-4px);
        }

        /* ===== CARD HEADER ===== */
        .card-header {
            background: #8d6e63;
            background-image: repeating-linear-gradient(90deg,
                    #8d6e63 0px, #8d6e63 6px,
                    #6d4c41 6px, #6d4c41 12px);
            border: 4px solid #4e342e;
            border-radius: 4px;
            padding: 12px 18px;
            margin-bottom: 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 12px;
            box-shadow: inset 0 -4px 0 #3e2723;
        }

        .card-header h1 {
            font-size: 18px;
            color: #fff;
            text-shadow: 2px 2px 0 #3e2723, 4px 4px 0 #1b1b1b;
            letter-spacing: 1px;
        }

        .card-header .badge {
            background: #2d2d2d;
            border: 3px solid #5d4037;
            border-radius: 4px;
            padding: 6px 14px;
            color: #aed581;
            font-size: 11px;
            letter-spacing: 0.5px;
            text-shadow: 1px 1px 0 #1b1b1b;
            box-shadow: inset 0 -3px 0 #1b1b1b;
        }

        /* ===== PROFILE ROW ===== */
        .profile-row {
            display: flex;
            flex-wrap: wrap;
            gap: 24px;
            align-items: center;
            margin-bottom: 28px;
            background: #bdbdbd;
            border: 4px solid #7a7a7a;
            border-radius: 6px;
            padding: 18px 22px;
            box-shadow: inset 0 -6px 0 #5a5a5a;
        }

        .avatar-frame {
            flex-shrink: 0;
            width: 110px;
            height: 110px;
            background: #4a4a4a;
            border: 6px solid #3e2723;
            border-radius: 6px;
            padding: 4px;
            box-shadow: inset 0 -4px 0 #2d2d2d, 0 4px 0 #1b1b1b;
            display: flex;
            align-items: center;
            justify-content: center;
            image-rendering: pixelated;
        }

        .avatar-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 2px;
            background: #6b4c3b;
            image-rendering: pixelated;
        }

        .avatar-steve {
            width: 100%;
            height: 100%;
            background:
                linear-gradient(135deg, #d4a373 40%, #b8835a 70%),
                radial-gradient(circle at 30% 40%, #2d2d2d 6px, transparent 6px),
                radial-gradient(circle at 70% 40%, #2d2d2d 6px, transparent 6px),
                radial-gradient(circle at 50% 70%, #2d2d2d 4px, transparent 4px);
            background-blend-mode: normal;
            border-radius: 4px;
        }

        .profile-info {
            flex: 1;
            min-width: 180px;
        }

        .profile-info .display-name {
            font-size: 24px;
            color: #1b1b1b;
            text-shadow: 2px 2px 0 #8d8d8d;
            margin-bottom: 4px;
            letter-spacing: 0.5px;
        }

        .profile-info .username {
            font-size: 13px;
            color: #3e2723;
            background: #e0d5c1;
            display: inline-block;
            padding: 4px 12px;
            border: 3px solid #7a5c4a;
            border-radius: 4px;
            margin-bottom: 10px;
            box-shadow: inset 0 -3px 0 #5a3d2e;
        }

        .profile-info .bio {
            font-size: 11px;
            line-height: 1.8;
            color: #2d2d2d;
            background: #e8e0d5;
            padding: 8px 14px;
            border: 3px solid #8d6e63;
            border-radius: 4px;
            box-shadow: inset 0 -3px 0 #6d4c41;
        }

        .profile-info .bio span {
            color: #4caf50;
            text-shadow: 1px 1px 0 #1b5e20;
        }

        /* ===== STATS ===== */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 12px;
            margin-bottom: 28px;
        }

        .stat-item {
            background: #b0a090;
            border: 4px solid #5d4037;
            border-radius: 4px;
            padding: 12px 8px;
            text-align: center;
            box-shadow: inset 0 -6px 0 #3e2723, 0 4px 0 #1b1b1b;
            transition: all 0.15s;
            cursor: default;
        }

        .stat-item:hover {
            transform: scale(1.04);
            background: #c4b4a0;
            border-color: #7a5c4a;
        }

        .stat-item .icon {
            font-size: 28px;
            display: block;
            margin-bottom: 4px;
            filter: drop-shadow(2px 2px 0 #2d2d2d);
        }

        .stat-item .value {
            font-size: 20px;
            color: #1b1b1b;
            text-shadow: 1px 1px 0 #8d8d8d;
            display: block;
            line-height: 1.2;
        }

        .stat-item .label {
            font-size: 8px;
            color: #3e2723;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            background: #d7c9b5;
            padding: 2px 8px;
            border-radius: 2px;
            display: inline-block;
            margin-top: 2px;
            border: 2px solid #7a5c4a;
        }

        /* ===== SECTION TITLE ===== */
        .section-title {
            font-size: 12px;
            color: #1b1b1b;
            text-shadow: 1px 1px 0 #8d8d8d;
            background: #d7c9b5;
            display: inline-block;
            padding: 4px 16px;
            border: 4px solid #5d4037;
            border-radius: 4px;
            margin-bottom: 14px;
            box-shadow: inset 0 -4px 0 #3e2723;
            letter-spacing: 0.5px;
        }

        /* ===== INVENTORY GRID (skills with devicons) ===== */
        .inventory-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 10px;
            margin-bottom: 24px;
            background: #b0a090;
            border: 4px solid #5d4037;
            border-radius: 4px;
            padding: 14px;
            box-shadow: inset 0 -6px 0 #3e2723;
        }

        .item-slot {
            background: #8d7a6a;
            border: 4px solid #4a3a2e;
            border-radius: 4px;
            padding: 10px 6px 8px;
            text-align: center;
            box-shadow: inset 0 -4px 0 #2d1f16, 0 2px 0 #1b1b1b;
            transition: all 0.15s;
            cursor: default;
        }

        .item-slot:hover {
            transform: scale(1.06);
            background: #a08878;
            border-color: #6d4c41;
        }

        .item-slot .item-icon {
            font-size: 36px;
            display: block;
            line-height: 1.2;
            filter: drop-shadow(2px 2px 0 #1b1b1b);
            color: #fff;
            /* devicon will apply its own color, but we keep white fallback */
        }

        /* Devicon overrides: ensure icons are visible and colored */
        .item-slot .item-icon i {
            font-size: inherit;
            /* inherit the 36px */
        }

        .item-slot .item-name {
            font-size: 7px;
            color: #f5f0e8;
            text-shadow: 1px 1px 0 #1b1b1b;
            display: block;
            margin-top: 2px;
            background: #2d2d2d;
            padding: 2px 4px;
            border-radius: 2px;
            border: 2px solid #1b1b1b;
            word-break: break-word;
            letter-spacing: 0.3px;
        }

        /* ===== HOTBAR (social links) ===== */
        .hotbar {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            background: #8d7a6a;
            border: 4px solid #4a3a2e;
            border-radius: 4px;
            padding: 12px 16px;
            box-shadow: inset 0 -6px 0 #2d1f16, 0 4px 0 #1b1b1b;
            margin-top: 4px;
        }

        .hotbar .slot {
            background: #6b5a4a;
            border: 4px solid #3a2a1e;
            border-radius: 4px;
            padding: 8px 16px;
            box-shadow: inset 0 -4px 0 #1b1b1b;
            transition: all 0.15s;
            text-decoration: none;
            color: #f5f0e8;
            font-size: 9px;
            display: flex;
            align-items: center;
            gap: 6px;
            letter-spacing: 0.3px;
        }

        .hotbar .slot:hover {
            transform: scale(1.08);
            background: #8d7a6a;
            border-color: #6d4c41;
        }

        .hotbar .slot .h-icon {
            font-size: 18px;
        }

        /* ===== FOOTER ===== */
        .card-footer {
            margin-top: 18px;
            text-align: center;
            font-size: 7px;
            color: #5a5a5a;
            letter-spacing: 0.5px;
            border-top: 4px solid #7a7a7a;
            padding-top: 12px;
            text-shadow: 1px 1px 0 #b0b0b0;
        }

        .card-footer a {
            color: #3e2723;
            text-decoration: none;
            font-weight: bold;
        }

        .card-footer a:hover {
            text-decoration: underline;
        }

        /* ===== ANIMATIONS ===== */
        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-6px);
            }
            100% {
                transform: translateY(0px);
            }
        }

        @keyframes float-particle {
            0% {
                transform: translate(0, 0) rotate(0deg);
                opacity: 0.2;
            }
            50% {
                transform: translate(20px, -30px) rotate(180deg);
                opacity: 0.5;
            }
            100% {
                transform: translate(0, 0) rotate(360deg);
                opacity: 0.2;
            }
        }

        /* ===== DIRT PARTICLES ===== */
        .dirt-particle {
            position: fixed;
            width: 6px;
            height: 6px;
            background: #6b4c3b;
            border-radius: 2px;
            opacity: 0.25;
            pointer-events: none;
            z-index: 0;
        }

        .dirt-particle:nth-child(1) {
            top: 12%;
            left: 5%;
            animation: float-particle 12s infinite;
        }
        .dirt-particle:nth-child(2) {
            bottom: 18%;
            right: 4%;
            animation: float-particle 16s infinite reverse;
        }
        .dirt-particle:nth-child(3) {
            top: 45%;
            left: 3%;
            animation: float-particle 14s infinite 2s;
        }
        .dirt-particle:nth-child(4) {
            bottom: 30%;
            right: 3%;
            animation: float-particle 18s infinite 1s;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 600px) {
            .minecraft-card {
                padding: 16px 14px 14px;
            }
            .card-header h1 {
                font-size: 13px;
            }
            .profile-row {
                flex-direction: column;
                align-items: center;
                text-align: center;
                padding: 14px;
            }
            .avatar-frame {
                width: 80px;
                height: 80px;
            }
            .profile-info .display-name {
                font-size: 18px;
            }
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .inventory-grid {
                grid-template-columns: repeat(3, 1fr);
                padding: 10px;
            }
            .hotbar .slot {
                font-size: 7px;
                padding: 6px 10px;
            }
            .hotbar .slot .h-icon {
                font-size: 14px;
            }
        }

        @media (max-width: 400px) {
            .inventory-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .stats-grid {
                grid-template-columns: 1fr 1fr;
            }
            .card-header {
                flex-direction: column;
                align-items: stretch;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- ===== DECORATIVE PARTICLES ===== -->
    <div class="dirt-particle"></div>
    <div class="dirt-particle"></div>
    <div class="dirt-particle"></div>
    <div class="dirt-particle"></div>

    <!-- ==========================================
    MAIN CARD
    ========================================== -->
    <div class="minecraft-card">

        <!-- ===== HEADER ===== -->
        <div class="card-header">
            <h1>⛏️  CRAFTING PROFILE</h1>
            <span class="badge">✦ SURVIVAL MODE ✦</span>
        </div>

        <!-- ===== PROFILE ROW ===== -->
        <div class="profile-row">
            <div class="avatar-frame">
                <img
                src="https://crafatar.com/avatars/YourGitHubUsername?size=128&overlay"
                alt="Avatar"
                onerror="this.style.display='none'; this.parentElement.innerHTML='<div class=\'avatar-steve\'></div>';"
                />
            </div>
            <div class="profile-info">
                <div class="display-name">⛏️ YourName</div>
                <div class="username">@yourusername</div>
                <div class="bio">
                    <span>▶</span> Full-stack dev &amp; Minecraft enthusiast.<br />
                    <span>⛏️</span> Building stuff, one commit at a time.
                </div>
            </div>
        </div>

        <!-- ===== STATS ===== -->
        <div class="stats-grid">
            <div class="stat-item">
                <span class="icon">⭐</span>
                <span class="value">42</span>
                <span class="label">Stars</span>
            </div>
            <div class="stat-item">
                <span class="icon">🍴</span>
                <span class="value">18</span>
                <span class="label">Forks</span>
            </div>
            <div class="stat-item">
                <span class="icon">👥</span>
                <span class="value">27</span>
                <span class="label">Followers</span>
            </div>
            <div class="stat-item">
                <span class="icon">📦</span>
                <span class="value">9</span>
                <span class="label">Repos</span>
            </div>
        </div>

        <!-- ===== INVENTORY (skills with Devicon) ===== -->
        <div class="section-title">🎒 INVENTORY</div>
        <div class="inventory-grid" id="inventoryGrid">
            <!-- Will be populated by JavaScript with devicon icons -->
        </div>

        <!-- ===== HOTBAR (social links) ===== -->
        <div class="section-title" style="margin-bottom:10px;">🔗 HOTBAR</div>
        <div class="hotbar" id="hotbar">
            <!-- Will be populated by JavaScript -->
        </div>

        <!-- ===== FOOTER ===== -->
        <div class="card-footer">
            🧱 crafted with ❤️ &nbsp;·&nbsp; <a href="https://github.com/yourusername" target="_blank">github.com/yourusername</a>
        </div>

    </div>

    <!-- ==========================================
    SCRIPT – dynamic data with devicons
    ========================================== -->
    <script>
        (function() {
            // ---- CONFIG ----
            const USERNAME = 'yourusername';
            const DISPLAY_NAME = '⛏️ YourName';
            const BIO = 'Full-stack dev & Minecraft enthusiast. ⛏️ Building stuff, one commit at a time.';
            const AVATAR_URL = `https://crafatar.com/avatars/${USERNAME}?size=128&overlay`;

            // Stats (static for demo)
            const STATS = {
                stars: 42,
                forks: 18,
                followers: 27,
                repos: 9
            };

            // Social links
            const LINKS = {
                github: `https://github.com/${USERNAME}`,
                twitter: 'https://twitter.com/yourhandle',
                linkedin: 'https://linkedin.com/in/yourhandle',
                youtube: 'https://youtube.com/@yourhandle',
                email: 'mailto:you@example.com'
            };

            // ---- SKILLS with Devicon classes ----
            const SKILLS = [
                { icon: 'devicon-react-original', name: 'React' },
                { icon: 'devicon-nodejs-plain-wordmark', name: 'Node.js' },
                { icon: 'devicon-python-plain', name: 'Python' },
                { icon: 'devicon-java-plain', name: 'Java' },
                { icon: 'devicon-docker-plain', name: 'Docker' },
                { icon: 'devicon-mysql-plain', name: 'MySQL' },
                { icon: 'devicon-figma-plain', name: 'Figma' },
                { icon: 'devicon-tensorflow-original', name: 'TensorFlow' }
            ];

            // ---- DOM UPDATE ----
            try {
                // Profile name & username
                const nameEl = document.querySelector('.profile-info .display-name');
                if (nameEl) nameEl.textContent = DISPLAY_NAME;

                const userEl = document.querySelector('.profile-info .username');
                if (userEl) userEl.textContent = `@${USERNAME}`;

                const bioEl = document.querySelector('.profile-info .bio');
                if (bioEl) bioEl.innerHTML = BIO.replace(/\n/g, '<br />');

                // Avatar
                const img = document.querySelector('.avatar-frame img');
                if (img) {
                    img.src = AVATAR_URL;
                    img.alt = `${USERNAME}'s avatar`;
                    img.onerror = function() {
                        this.style.display = 'none';
                        const frame = this.parentElement;
                        if (frame && !frame.querySelector('.avatar-steve')) {
                            const steve = document.createElement('div');
                            steve.className = 'avatar-steve';
                            frame.appendChild(steve);
                        }
                    };
                }

                // Stats
                const statValues = document.querySelectorAll('.stat-item .value');
                const statKeys = ['stars', 'forks', 'followers', 'repos'];
                statValues.forEach((el, i) => {
                    if (i < statKeys.length) {
                        const key = statKeys[i];
                        if (STATS[key] !== undefined) {
                            el.textContent = STATS[key];
                        }
                    }
                });

                // Inventory / Skills (with devicons)
                const invGrid = document.getElementById('inventoryGrid');
                if (invGrid) {
                    invGrid.innerHTML = '';
                    SKILLS.forEach(skill => {
                        const slot = document.createElement('div');
                        slot.className = 'item-slot';
                        slot.innerHTML = `
                                    <span class="item-icon"><i class="${skill.icon}"></i></span>
                                    <span class="item-name">${skill.name}</span>
                                `;
                        invGrid.appendChild(slot);
                    });
                }

                // Hotbar links
                const hotbar = document.getElementById('hotbar');
                if (hotbar) {
                    const linkConfig = [
                        { icon: '🐙', label: 'GitHub', url: LINKS.github },
                        { icon: '🐦', label: 'Twitter', url: LINKS.twitter },
                        { icon: '💼', label: 'LinkedIn', url: LINKS.linkedin },
                        { icon: '📺', label: 'YouTube', url: LINKS.youtube },
                        { icon: '✉️', label: 'Email', url: LINKS.email }
                    ];
                    hotbar.innerHTML = '';
                    linkConfig.forEach(link => {
                        const a = document.createElement('a');
                        a.className = 'slot';
                        a.href = link.url;
                        a.target = '_blank';
                        a.innerHTML = `
                                    <span class="h-icon">${link.icon}</span> ${link.label}
                                `;
                        hotbar.appendChild(a);
                    });
                }

                // Footer link
                const footerLink = document.querySelector('.card-footer a');
                if (footerLink) {
                    footerLink.href = LINKS.github;
                    footerLink.textContent = `github.com/${USERNAME}`;
                }

                console.log('✅ Minecraft profile with devicons loaded!');
            } catch (e) {
                console.warn('⚠️ Could not update some elements:', e);
            }

            // ---- OPTIONAL: fetch live stats from GitHub API (commented) ----
            /*
            async function fetchGitHubStats(username) {
                try {
                    const res = await fetch(`https://api.github.com/users/${username}`);
                    if (!res.ok) throw new Error('API error');
                    const data = await res.json();
                    const stats = {
                        stars: 0,
                        forks: 0,
                        followers: data.followers || 0,
                        repos: data.public_repos || 0
                    };
                    const reposRes = await fetch(`https://api.github.com/users/${username}/repos?per_page=100`);
                    const repos = await reposRes.json();
                    if (Array.isArray(repos)) {
                        stats.stars = repos.reduce((acc, r) => acc + (r.stargazers_count || 0), 0);
                        stats.forks = repos.reduce((acc, r) => acc + (r.forks_count || 0), 0);
                    }
                    const vals = document.querySelectorAll('.stat-item .value');
                    const keys = ['stars', 'forks', 'followers', 'repos'];
                    vals.forEach((el, i) => {
                        if (i < keys.length && stats[keys[i]] !== undefined) {
                            el.textContent = stats[keys[i]];
                        }
                    });
                } catch (err) {
                    console.warn('Could not fetch live stats:', err);
                }
            }
            // fetchGitHubStats(USERNAME);
            */
        })();
    </script>

</body>
</html>
## Hi there 👋

<!--
**kimhongpech-dev/kimhongpech-dev** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
