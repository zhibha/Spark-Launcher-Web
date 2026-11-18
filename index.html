<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">

    <title>Spark Launcher · Android 上的 Minecraft Java 版启动器</title>
    <meta name="description" content="Spark Launcher 是一款开源、非商业的 Android 端 Minecraft Java 版第三方启动器。使用微软官方 OAuth 2.0 设备代码流认证，支持正版登录与在线模式服务器。">
    <meta name="keywords" content="Spark Launcher, Minecraft, Java 版, Android 启动器, 我的世界, 开源">
    <meta name="theme-color" content="#03050a">
    <link rel="canonical" href="https://github.com/zhibha/Spark-Launcher">

    <meta property="og:type" content="website">
    <meta property="og:title" content="Spark Launcher · Android 上的 Minecraft Java 版">
    <meta property="og:description" content="开源、非商业的 Android 端 Minecraft Java 启动器，微软官方登录，支持在线模式服务器。">
    <meta property="og:url" content="https://github.com/zhibha/Spark-Launcher">
    <meta name="twitter:card" content="summary_large_image">

    <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%2303050a'/%3E%3Cpath d='M13 7 5 18h6l-1 7 9-12h-6z' fill='%23ff3b5c'/%3E%3C/svg%3E">

    <style>
        /* ================= 基础与液态玻璃变量 ================= */
        :root {
            --bg-base: #03050a;
            --glass-bg: rgba(255, 255, 255, 0.02);
            --glass-border: rgba(255, 255, 255, 0.06);
            --glass-highlight: rgba(255, 255, 255, 0.15);
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --primary: #ff3b5c;
            --primary-hover: #ff6379;
            --primary-glow: rgba(255, 59, 92, 0.42);
            --nav-h: 68px;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }
        @media (prefers-reduced-motion: reduce) {
            * { animation: none !important; transition: none !important; scroll-behavior: auto !important; }
            .fade-up { opacity: 1 !important; transform: none !important; }
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-base);
            color: var(--text-main);
            line-height: 1.7;
            overflow-x: hidden;
            position: relative;
            -webkit-font-smoothing: antialiased;
        }

        /* 无障碍：键盘焦点可见 */
        :focus-visible { outline: 2px solid var(--primary); outline-offset: 3px; border-radius: 6px; }
        .skip-link {
            position: absolute; left: -9999px; top: 0; z-index: 2000;
            background: var(--primary); color: #fff; padding: .7rem 1.2rem;
            border-radius: 0 0 12px 0; font-weight: 700;
        }
        .skip-link:focus { left: 0; }

        /* ================= 动态流光背景 ================= */
        .liquid-bg {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            z-index: -1; overflow: hidden; background: var(--bg-base);
        }
        .blob {
            position: absolute; filter: blur(120px); border-radius: 50%; opacity: 0.45;
            animation: float 25s infinite alternate ease-in-out;
        }
        .blob-1 { width: 600px; height: 600px; background: #8f1329; top: -10%; left: -10%; }
        .blob-2 { width: 500px; height: 500px; background: #4a0b18; bottom: -10%; right: -10%; animation-delay: -8s; }
        .blob-3 { width: 400px; height: 400px; background: #6d0f22; top: 40%; left: 40%; animation-delay: -15s; }
        @keyframes float {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(120px, 150px) scale(1.15); }
        }

        a { text-decoration: none; color: var(--primary); transition: all 0.3s; }

        /* ================= 导航栏 ================= */
        nav#nav {
            position: fixed; top: 1.5rem; left: 50%; transform: translateX(-50%);
            width: 92%; max-width: 1100px;
            background: linear-gradient(135deg, rgba(255,255,255,0.08), rgba(255,255,255,0.01));
            backdrop-filter: blur(24px) saturate(200%);
            -webkit-backdrop-filter: blur(24px) saturate(200%);
            border: 1px solid var(--glass-border);
            border-top-color: rgba(255, 255, 255, 0.25);
            border-left-color: rgba(255, 255, 255, 0.1);
            border-radius: 100px; z-index: 1000;
            box-shadow: 0 10px 40px -10px rgba(0,0,0,0.8), inset 0 1px 0 rgba(255, 255, 255, 0.1);
            transition: box-shadow .3s, background .3s;
        }
        nav#nav.scrolled { box-shadow: 0 14px 50px -10px rgba(0,0,0,0.95), inset 0 1px 0 rgba(255,255,255,0.12); }
        .nav-content {
            padding: 0.65rem 1.1rem 0.65rem 1.5rem; display: flex; justify-content: space-between; align-items: center; gap: 1rem;
        }
        .logo { font-size: 1.25rem; font-weight: 800; color: var(--text-main); letter-spacing: 0.5px; white-space: nowrap; }
        .logo span { color: var(--primary); }

        .nav-right { display: flex; align-items: center; gap: 1.2rem; }
        .nav-links { display: flex; gap: 1.4rem; }
        .nav-links a {
            color: var(--text-muted); font-size: 0.95rem; font-weight: 500; position: relative;
        }
        .nav-links a::after {
            content: ''; position: absolute; bottom: -4px; left: 0; width: 0; height: 2px;
            background: var(--primary); transition: width 0.3s ease; border-radius: 2px;
        }
        .nav-links a:hover { color: var(--text-main); }
        .nav-links a:hover::after { width: 100%; }

        /* iOS 风格液态玻璃圆钮 */
        .lang-switch, .menu-btn {
            position: relative; flex-shrink: 0;
            width: 38px; height: 38px; padding: 0; border-radius: 50%;
            display: inline-flex; align-items: center; justify-content: center;
            color: var(--text-main); cursor: pointer;
            border: 1px solid rgba(255,255,255,0.12);
            background:
                radial-gradient(120% 120% at 30% 0%, rgba(255,255,255,0.22) 0%, rgba(255,255,255,0.06) 38%, rgba(255,255,255,0.015) 70%),
                rgba(255,255,255,0.02);
            backdrop-filter: blur(22px) saturate(200%);
            -webkit-backdrop-filter: blur(22px) saturate(200%);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.45),
                inset 0 -1px 1px rgba(0,0,0,0.35),
                0 4px 14px -4px rgba(0,0,0,0.7);
            transition: transform .28s cubic-bezier(.34,1.56,.64,1), box-shadow .3s, border-color .3s, background .3s;
            -webkit-tap-highlight-color: transparent;
        }
        /* 高光扫过（液态感） */
        .lang-switch::after, .menu-btn::after {
            content: ''; position: absolute; inset: 0; border-radius: 50%;
            background: linear-gradient(140deg, rgba(255,255,255,0.28) 0%, rgba(255,255,255,0) 45%);
            opacity: .75; pointer-events: none; transition: opacity .3s;
        }
        .lang-switch:hover, .menu-btn:hover {
            transform: translateY(-1px) scale(1.06);
            border-color: rgba(52, 211, 153, 0.45);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.55),
                inset 0 -1px 1px rgba(0,0,0,0.35),
                0 6px 22px -6px var(--primary-glow),
                0 0 22px -2px rgba(255,59,92,0.35);
        }
        .lang-switch:hover::after, .menu-btn:hover::after { opacity: 1; }
        .lang-switch:active, .menu-btn:active { transform: scale(0.94); }
        .lang-switch svg, .menu-btn svg { width: 17px; height: 17px; stroke: currentColor; fill: none; stroke-width: 1.9; position: relative; z-index: 1; }
        .menu-btn { display: none; }

        /* 语言文字仅给读屏用 */
        .sr-only {
            position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px;
            overflow: hidden; clip: rect(0 0 0 0); white-space: nowrap; border: 0;
        }
        /* 悬停提示（iOS 风格小气泡） */
        .lang-switch::before {
            content: attr(data-tip); position: absolute; top: calc(100% + 10px); left: 50%;
            transform: translateX(-50%) translateY(-4px); white-space: nowrap;
            background: rgba(12,16,24,0.92); border: 1px solid var(--glass-border);
            color: var(--text-main); font-size: .72rem; font-weight: 600; letter-spacing: .02em;
            padding: .3rem .6rem; border-radius: 8px; backdrop-filter: blur(12px);
            opacity: 0; pointer-events: none; transition: all .25s;
            box-shadow: 0 8px 20px -8px rgba(0,0,0,.9);
        }
        .lang-switch:hover::before { opacity: 1; transform: translateX(-50%) translateY(0); }

        /* 移动端下拉菜单 */
        .mobile-menu {
            display: none; position: fixed; top: calc(1.5rem + var(--nav-h)); left: 50%;
            transform: translateX(-50%) translateY(-8px); width: 92%; max-width: 1100px;
            background: rgba(8,11,18,0.92); backdrop-filter: blur(24px);
            border: 1px solid var(--glass-border); border-radius: 20px; z-index: 999;
            padding: .8rem; opacity: 0; pointer-events: none; transition: all .25s;
            box-shadow: 0 20px 50px -10px rgba(0,0,0,.9);
        }
        .mobile-menu.open { opacity: 1; pointer-events: auto; transform: translateX(-50%) translateY(0); }
        .mobile-menu a { display: block; padding: .8rem 1rem; border-radius: 12px; color: var(--text-main); font-weight: 600; }
        .mobile-menu a:hover { background: rgba(255,255,255,.06); }

        /* ================= 全局液态卡片 ================= */
        .glass-card {
            background: linear-gradient(135deg, rgba(255,255,255,0.05) 0%, rgba(255,255,255,0.01) 100%);
            backdrop-filter: blur(24px) saturate(150%);
            -webkit-backdrop-filter: blur(24px) saturate(150%);
            border: 1px solid var(--glass-border);
            border-top-color: rgba(255,255,255,0.15);
            border-radius: 24px;
            box-shadow: 0 12px 40px -10px rgba(0,0,0,0.6), inset 0 1px 0 rgba(255,255,255,0.05);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative; overflow: hidden;
        }
        .glass-card::before {
            content: ''; position: absolute; top: 0; left: 0; right: 0; height: 100%;
            background: radial-gradient(800px circle at var(--mouse-x, 50%) var(--mouse-y, 50%), rgba(255,255,255,0.06), transparent 40%);
            opacity: 0; transition: opacity 0.3s; pointer-events: none;
        }
        .glass-card:hover::before { opacity: 1; }
        .glass-card:hover {
            transform: translateY(-8px); border-color: rgba(255, 59, 92, 0.3);
            box-shadow: 0 20px 40px -10px rgba(255, 59, 92, 0.15), inset 0 1px 0 rgba(255,255,255,0.1);
        }

        /* ================= 通用区块与动画 ================= */
        section { padding: 7rem 2rem 3rem 2rem; max-width: 1100px; margin: 0 auto; }
        .section-title { text-align: center; font-size: 2.5rem; font-weight: 800; letter-spacing: -0.5px; margin-bottom: 1rem; }
        .section-subtitle { text-align: center; color: var(--text-muted); margin-bottom: 3.5rem; font-size: 1.05rem; max-width: 760px; margin-left: auto; margin-right: auto; }

        .fade-up { opacity: 0; transform: translateY(40px); transition: opacity 0.8s ease, transform 0.8s ease; }
        .fade-up.visible { opacity: 1; transform: translateY(0); }

        /* ================= 首页 ================= */
        #hero {
            min-height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            text-align: center; padding-top: 8rem;
        }
        .badge {
            display: inline-flex; align-items: center; gap: .5rem;
            background: rgba(255,255,255,0.03); border: 1px solid var(--glass-border);
            padding: 0.5rem 1.2rem; border-radius: 100px; font-size: 0.85rem; font-weight: 600; color: var(--primary);
            margin-bottom: 2rem; backdrop-filter: blur(10px); box-shadow: inset 0 1px 0 rgba(255,255,255,0.1);
        }
        .dot { width: 7px; height: 7px; border-radius: 50%; background: var(--primary); box-shadow: 0 0 8px var(--primary); }
        #hero h1 { font-size: 4.2rem; font-weight: 900; letter-spacing: -1.5px; line-height: 1.1; margin-bottom: 1.5rem; }
        #hero h1 span {
            background: linear-gradient(135deg, #ff7a8a, #d61f3f);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            background-clip: text;
            filter: drop-shadow(0 0 15px rgba(255,59,92,0.3));
        }
        #hero p { font-size: 1.15rem; color: var(--text-muted); max-width: 680px; margin-bottom: 2.5rem; }

        .btn-group { display: flex; gap: 1rem; z-index: 10; }
        .btn {
            display: inline-flex; align-items: center; justify-content: center; gap: .5rem;
            padding: 0.9rem 2.3rem; border-radius: 100px;
            font-weight: 600; font-size: 1rem; cursor: pointer;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); position: relative; overflow: hidden;
            border: 1px solid transparent;
        }
        .btn-primary { background: var(--primary); color: #fff; box-shadow: 0 0 20px var(--primary-glow); }
        .btn-primary:hover { background: var(--primary-hover); transform: translateY(-3px) scale(1.02); box-shadow: 0 10px 30px var(--primary-glow); }
        .btn-glass { background: var(--glass-bg); color: var(--text-main); border-color: var(--glass-border); backdrop-filter: blur(10px); }
        .btn-glass:hover { background: rgba(255,255,255,0.08); border-color: var(--glass-highlight); transform: translateY(-3px) scale(1.02); }

        .hero-meta {
            display: flex; flex-wrap: wrap; gap: .5rem 1.4rem; justify-content: center;
            margin-top: 2.5rem; color: var(--text-muted); font-size: .9rem;
        }
        .hero-meta span { display: inline-flex; align-items: center; gap: .4rem; }
        .hero-meta svg { width: 15px; height: 15px; stroke: var(--primary); fill: none; stroke-width: 2.4; }

        /* ================= 特性区 ================= */
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; }
        .feature-card { padding: 2.4rem 2rem; display: flex; flex-direction: column; }
        .feature-icon {
            width: 52px; height: 52px; border-radius: 14px;
            background: rgba(255, 59, 92, 0.08); border: 1px solid rgba(255, 59, 92, 0.2);
            border-top-color: rgba(255, 59, 92, 0.4);
            display: flex; justify-content: center; align-items: center; margin-bottom: 1.4rem; color: var(--primary);
            box-shadow: inset 0 1px 0 rgba(255,255,255,0.1), 0 4px 10px rgba(0,0,0,0.2);
            flex-shrink: 0;
        }
        .feature-icon svg { width: 24px; height: 24px; stroke: currentColor; fill: none; stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }
        .feature-card h3 { font-size: 1.22rem; margin-bottom: 0.7rem; font-weight: 700; }
        .feature-card p { font-size: 0.94rem; color: var(--text-muted); flex-grow: 1; }

        /* ================= 运行要求 ================= */
        .req-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; }
        .req-item { padding: 1.6rem 1.4rem; display: flex; flex-direction: column; gap: .35rem; }
        .req-item .k { font-size: .8rem; letter-spacing: .08em; text-transform: uppercase; color: var(--primary); font-weight: 700; }
        .req-item .v { font-size: 1.35rem; font-weight: 800; }
        .req-item .n { font-size: .85rem; color: var(--text-muted); }

        /* ================= FAQ ================= */
        .faq-list { display: flex; flex-direction: column; gap: .8rem; }
        details.faq {
            background: linear-gradient(135deg, rgba(255,255,255,0.04), rgba(255,255,255,0.01));
            border: 1px solid var(--glass-border); border-radius: 16px;
            padding: 0 1.4rem; transition: border-color .3s, background .3s;
        }
        details.faq[open] { border-color: rgba(255,59,92,.35); background: rgba(255,59,92,.04); }
        details.faq summary {
            cursor: pointer; padding: 1.1rem 0; font-weight: 600; font-size: 1rem;
            list-style: none; display: flex; justify-content: space-between; align-items: center; gap: 1rem;
        }
        details.faq summary::-webkit-details-marker { display: none; }
        details.faq summary::after {
            content: '+'; color: var(--primary); font-size: 1.4rem; line-height: 1; flex-shrink: 0;
            transition: transform .25s;
        }
        details.faq[open] summary::after { transform: rotate(45deg); }
        details.faq p { padding: 0 0 1.2rem; color: var(--text-muted); font-size: .95rem; }

        /* ================= 社区致谢 ================= */
        .credits-container { display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center; }
        .credit-pill {
            display: flex; align-items: center; gap: 0.5rem;
            background: rgba(255,255,255,0.03); border: 1px solid var(--glass-border);
            padding: 0.8rem 1.5rem; border-radius: 50px; font-weight: 600; color: var(--text-muted);
            transition: all 0.3s; box-shadow: inset 0 1px 0 rgba(255,255,255,0.05);
        }
        .credit-pill:hover {
            color: var(--text-main); background: rgba(255,255,255,0.08); border-color: var(--glass-highlight);
            transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0,0,0,0.3), inset 0 1px 0 rgba(255,255,255,0.1);
        }

        /* ================= 下载区 ================= */
        #download { text-align: center; padding: 5rem 2rem; max-width: 900px; }
        #download .glass-card {
            padding: 3.5rem 2rem; max-width: 800px; margin: 0 auto;
            background: linear-gradient(180deg, rgba(255,59,92,0.06) 0%, rgba(255,255,255,0.01) 100%);
            border-color: rgba(255, 59, 92, 0.2); border-top-color: rgba(255, 59, 92, 0.4);
        }
        .dl-note { margin-top: 1.5rem; font-size: .9rem; color: var(--text-muted); }
        .dl-sub { margin-top: .9rem; font-size: .88rem; }
        .dl-sub a { color: var(--text-muted); text-decoration: underline; text-underline-offset: 3px; }
        .dl-sub a:hover { color: var(--primary); }

        /* ================= 页脚 ================= */
        footer {
            padding: 3rem 2rem 2.5rem; color: var(--text-muted); font-size: 0.9rem;
            border-top: 1px solid var(--glass-border); background: rgba(0,0,0,0.3);
            text-align: center;
        }
        .disclaimer {
            max-width: 800px; margin: 0 auto 2rem auto; padding: 1.2rem 1.3rem;
            background: rgba(239, 68, 68, 0.03); border: 1px solid rgba(239, 68, 68, 0.1);
            border-left: 4px solid #ef4444; border-radius: 8px; text-align: left;
            font-size: .88rem; line-height: 1.65;
        }
        .footer-links { display: flex; flex-wrap: wrap; gap: .5rem 1.5rem; justify-content: center; margin-bottom: 1.2rem; }
        .footer-links a { color: var(--text-muted); font-size: .9rem; }
        .footer-links a:hover { color: var(--primary); }

        /* 返回顶部 */
        .to-top {
            position: fixed; right: 1.4rem; bottom: 1.4rem; width: 46px; height: 46px;
            border-radius: 50%; display: flex; align-items: center; justify-content: center;
            background: rgba(255,59,92,.12); border: 1px solid rgba(255,59,92,.3);
            color: var(--primary); cursor: pointer; z-index: 900;
            opacity: 0; pointer-events: none; transition: all .3s; backdrop-filter: blur(10px);
        }
        .to-top.show { opacity: 1; pointer-events: auto; }
        .to-top:hover { background: rgba(255,59,92,.22); transform: translateY(-3px); }
        .to-top svg { width: 20px; height: 20px; stroke: currentColor; fill: none; stroke-width: 2.4; }

        /* ================= 响应式 ================= */
        /* ================= 移动端（M3 / iOS / ColorOS / HyperOS / HarmonyOS 取向） ================= */
        :root {
            --safe-top: env(safe-area-inset-top, 0px);
            --safe-bottom: env(safe-area-inset-bottom, 0px);
            --tabbar-h: 62px;
        }

        /* 底部标签栏：移动端主导航，替代下拉菜单 */
        .tabbar {
            display: none;
            position: fixed; left: 0; right: 0; bottom: 0; z-index: 998;
            padding: 6px 8px calc(6px + var(--safe-bottom));
            background: rgba(6, 9, 14, 0.72);
            backdrop-filter: blur(26px) saturate(180%);
            -webkit-backdrop-filter: blur(26px) saturate(180%);
            border-top: 1px solid rgba(255,255,255,0.07);
            box-shadow: 0 -10px 30px -12px rgba(0,0,0,.9);
        }
        .tabbar-inner { display: flex; align-items: stretch; justify-content: space-around; max-width: 560px; margin: 0 auto; }
        .tab {
            flex: 1; min-height: 48px; display: flex; flex-direction: column;
            align-items: center; justify-content: center; gap: 3px;
            color: var(--text-muted); font-size: 10.5px; font-weight: 600; letter-spacing: .02em;
            border-radius: 14px; text-decoration: none; transition: color .25s, background .25s, transform .2s;
            -webkit-tap-highlight-color: transparent;
        }
        .tab svg { width: 21px; height: 21px; stroke: currentColor; fill: none; stroke-width: 1.9; stroke-linecap: round; stroke-linejoin: round; }
        .tab:active { transform: scale(.94); }
        .tab.active { color: var(--primary); }
        .tab.active::after {
            content: ''; position: absolute; bottom: 4px; width: 16px; height: 2px; border-radius: 2px;
            background: var(--primary); box-shadow: 0 0 8px var(--primary-glow);
        }
        .tab { position: relative; }

        /* iOS 风格：更圆的卡片 + 更柔阴影 */
        html.platform-ios .glass-card { border-radius: 28px; }
        html.platform-ios .btn { border-radius: 999px; }

        /* Android 14+（M3 / ColorOS / HyperOS / HarmonyOS）：
           状态层 + 大圆角 + 更明显的触摸反馈 */
        html.platform-android .glass-card { border-radius: 22px; }
        html.platform-android .btn { border-radius: 20px; }
        html.platform-android .tab { border-radius: 16px; }
        html.platform-android .tab.active { background: rgba(255,59,92,.12); }

        @media (max-width: 860px) {
            /* 顶部：只留 logo + 语言圆钮，导航交给底栏 */
            nav#nav {
                top: calc(10px + var(--safe-top));
                width: calc(100% - 24px); border-radius: 22px;
            }
            .nav-content { padding: .5rem .6rem .5rem 1rem; }
            .nav-links { display: none; }
            .menu-btn { display: none; }
            .lang-switch { width: 44px; height: 44px; }  /* iOS HIG 最小触摸区 */
            .logo { font-size: 1.1rem; }

            /* 底部留出标签栏空间 */
            body { padding-bottom: calc(var(--tabbar-h) + var(--safe-bottom)); }
            .tabbar { display: block; }
            .to-top { bottom: calc(var(--tabbar-h) + var(--safe-bottom) + 14px); right: 14px; }

            /* 排版节奏 */
            #hero { padding-top: calc(var(--safe-top) + 84px); min-height: 88vh; }
            #hero h1 { font-size: clamp(2.1rem, 9.2vw, 2.9rem); letter-spacing: -1px; line-height: 1.14; }
            #hero p { font-size: 1rem; line-height: 1.72; margin-bottom: 2rem; }
            section { padding: 4.2rem 1.15rem 1.6rem 1.15rem; }
            .section-title { font-size: clamp(1.5rem, 6.4vw, 1.95rem); }
            .section-subtitle { font-size: .97rem; margin-bottom: 2.2rem; }

            /* 触摸目标统一 ≥44px */
            .btn { width: 100%; min-height: 50px; font-size: 1rem; }
            .btn-group { flex-direction: column; width: 100%; max-width: 360px; margin: 0 auto; gap: .7rem; }
            details.faq summary { min-height: 52px; }
            .credit-pill { min-height: 44px; display: inline-flex; align-items: center; }

            .features-grid { grid-template-columns: 1fr; gap: 1rem; }
            .feature-card { padding: 1.8rem 1.4rem; }
            .req-grid { grid-template-columns: repeat(2, 1fr); gap: .7rem; }
            .req-item { padding: 1.2rem 1rem; }
            .req-item .v { font-size: 1.15rem; }
            .credits-container { gap: .6rem; }
            .credit-pill { padding: .55rem 1.05rem; font-size: .84rem; }
            #download .glass-card { padding: 2.2rem 1.2rem; }
            .disclaimer { font-size: .82rem; padding: 1rem; }
            .footer-links { gap: .8rem 1.1rem; }

            /* 没有 hover 的触屏：用 active 代替 hover 抬升 */
            .glass-card:hover { transform: none; }
        }

        @media (hover: none) {
            .glass-card:hover { transform: none; box-shadow: 0 12px 40px -10px rgba(0,0,0,.6), inset 0 1px 0 rgba(255,255,255,.05); }
            .glass-card:active { transform: scale(.985); border-color: rgba(255,59,92,.25); }
            .btn:hover { transform: none; }
            .btn:active { transform: scale(.97); }
        }

        /* 小屏（360 及以下） */
        @media (max-width: 380px) {
            #hero h1 { font-size: 1.95rem; }
            .req-grid { grid-template-columns: 1fr; }
            .tab { font-size: 9.5px; }
            .tab svg { width: 19px; height: 19px; }
        }

        /* 横屏手机：收窄首屏高度 */
        @media (max-height: 520px) and (orientation: landscape) {
            #hero { min-height: auto; padding-top: calc(var(--safe-top) + 90px); padding-bottom: 3rem; }
            .tabbar { display: none; }
            body { padding-bottom: 0; }
            .nav-links { display: flex; }
        }

        /* 平板 / 大屏，保持桌面排版但放宽 */
        @media (min-width: 861px) and (max-width: 1100px) {
            section { padding-left: 2rem; padding-right: 2rem; }
        }

        /* ================= 红色立体质感增强 ================= */
        :root {
            --depth-hi: rgba(255,255,255,0.55);
            --depth-lo: rgba(0,0,0,0.55);
            --red-deep: #b8132f;
            --red-mid: #ff3b5c;
            --red-light: #ff8296;
        }

        /* 主按钮：纵向渐变 + 顶部高光 + 落地阴影，做出一块凸起的糖果冻 */
        .btn-primary {
            background: linear-gradient(180deg, var(--red-light) 0%, var(--red-mid) 42%, var(--red-deep) 100%);
            color: #fff;
            border: 1px solid rgba(255,255,255,0.22);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.6),
                inset 0 -2px 6px rgba(0,0,0,0.35),
                0 10px 24px -8px rgba(255,59,92,0.55),
                0 2px 0 var(--red-deep);
            text-shadow: 0 1px 1px rgba(0,0,0,0.25);
        }
        .btn-primary:hover {
            background: linear-gradient(180deg, #ff96a8 0%, #ff5570 42%, #c81836 100%);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.7),
                inset 0 -2px 6px rgba(0,0,0,0.32),
                0 14px 34px -10px rgba(255,59,92,0.7),
                0 3px 0 var(--red-deep);
        }
        .btn-primary:active {
            transform: translateY(2px) scale(.99);
            box-shadow:
                inset 0 2px 8px rgba(0,0,0,0.45),
                0 3px 10px -6px rgba(255,59,92,0.6);
        }

        /* 玻璃卡片：顶部内高光 + 底部内暗影，边缘带一圈极细的亮边 */
        .glass-card {
            background:
                linear-gradient(180deg, rgba(255,255,255,0.075) 0%, rgba(255,255,255,0.02) 42%, rgba(255,255,255,0.008) 100%);
            border-color: rgba(255,255,255,0.09);
            border-top-color: rgba(255,255,255,0.22);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.18),
                inset 0 -18px 30px -24px rgba(0,0,0,0.9),
                0 18px 44px -18px rgba(0,0,0,0.9);
        }
        .glass-card:hover {
            border-color: rgba(255,59,92,0.42);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.24),
                inset 0 -18px 30px -24px rgba(0,0,0,0.85),
                0 26px 60px -22px rgba(255,59,92,0.45),
                0 0 0 1px rgba(255,59,92,0.12);
        }

        /* 图标底座：红色凹陷感 */
        .feature-icon {
            background: radial-gradient(120% 120% at 30% 0%, rgba(255,255,255,0.18) 0%, rgba(255,59,92,0.16) 45%, rgba(255,59,92,0.06) 100%);
            border-color: rgba(255,59,92,0.32);
            border-top-color: rgba(255,255,255,0.45);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.35),
                inset 0 -3px 8px rgba(0,0,0,0.4),
                0 6px 16px -8px rgba(255,59,92,0.6);
            color: #ff8a9c;
        }

        /* 导航：更明显的玻璃厚度 */
        nav#nav {
            background:
                linear-gradient(180deg, rgba(255,255,255,0.12) 0%, rgba(255,255,255,0.03) 38%, rgba(255,255,255,0.012) 100%);
            border-top-color: rgba(255,255,255,0.32);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.28),
                inset 0 -10px 24px -18px rgba(0,0,0,0.8),
                0 14px 40px -14px rgba(0,0,0,0.9),
                0 0 0 1px rgba(255,59,92,0.06);
        }

        /* 圆形按钮：红调玻璃球 */
        .lang-switch, .menu-btn {
            background:
                radial-gradient(120% 120% at 32% 0%, rgba(255,255,255,0.3) 0%, rgba(255,255,255,0.08) 40%, rgba(255,59,92,0.1) 72%, rgba(255,59,92,0.03) 100%),
                rgba(255,255,255,0.02);
            border-color: rgba(255,255,255,0.18);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.6),
                inset 0 -3px 8px rgba(0,0,0,0.5),
                0 4px 14px -4px rgba(0,0,0,0.75);
        }
        .lang-switch:hover, .menu-btn:hover {
            border-color: rgba(255,59,92,0.5);
            box-shadow:
                inset 0 1px 0 rgba(255,255,255,0.7),
                inset 0 -3px 8px rgba(0,0,0,0.45),
                0 8px 26px -8px rgba(255,59,92,0.75);
        }

        /* 数字/标题的红色渐变，带一点上亮下暗 */
        #hero h1 span {
            background: linear-gradient(180deg, #ffa1af 0%, #ff3b5c 55%, #c81836 100%);
            -webkit-background-clip: text; background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 2px 10px rgba(255,59,92,0.45));
        }

        /* 徽章与圆点 */
        .badge { color: #ff8a9c; border-color: rgba(255,59,92,0.28); }
        .dot { box-shadow: 0 0 10px #ff3b5c, 0 0 22px rgba(255,59,92,0.6); }

        /* 底部标签栏选中：红色上浮 */
        .tab.active { color: #ff6379; text-shadow: 0 0 14px rgba(255,59,92,0.6); }
        .tab.active::after { background: #ff3b5c; box-shadow: 0 0 12px rgba(255,59,92,0.9); }
        html.platform-android .tab.active { background: rgba(255,59,92,0.14); }

        /* 分隔与细节 */
        details.faq[open] { border-color: rgba(255,59,92,0.38); background: rgba(255,59,92,0.06); }
        details.faq summary::after { color: #ff6379; }
        .req-item .k { color: #ff8a9c; }
        .disclaimer { background: rgba(255,59,92,0.05); border-color: rgba(255,59,92,0.16); border-left-color: #ff3b5c; }
        .to-top { background: rgba(255,59,92,0.14); border-color: rgba(255,59,92,0.34); color: #ff8296; }
        .to-top:hover { background: rgba(255,59,92,0.24); }
    </style>
</head>
<body>

    <a class="skip-link" href="#hero" data-en="Skip to content" data-zh="跳到正文">跳到正文</a>

    <!-- 动态流光背景 -->
    <div class="liquid-bg" aria-hidden="true">
        <div class="blob blob-1"></div>
        <div class="blob blob-2"></div>
        <div class="blob blob-3"></div>
    </div>

    <!-- 导航栏 -->
    <nav id="nav">
        <div class="nav-content">
            <a href="#hero" class="logo">Spark<span>Launcher</span></a>
            <div class="nav-right">
                <div class="nav-links">
                    <a href="#features" data-en="Features" data-zh="特性">特性</a>
                    <a href="#requirements" data-en="Requirements" data-zh="配置要求">配置要求</a>
                    <a href="#faq" data-en="FAQ" data-zh="常见问题">常见问题</a>
                    <a href="#credits" data-en="Credits" data-zh="致谢">致谢</a>
                    <a href="#download" data-en="Download" data-zh="下载">下载</a>
                    <a href="https://github.com/zhibha/Spark-Launcher" target="_blank" rel="noopener">GitHub</a>
                </div>
                <button class="lang-switch" id="langBtn" type="button" data-tip="English" aria-label="切换语言 / Switch language">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><circle cx="12" cy="12" r="9.2"></circle><line x1="2.8" y1="12" x2="21.2" y2="12"></line><path d="M12 2.8a15 15 0 0 1 0 18.4 15 15 0 0 1 0-18.4z"></path></svg>
                    <span id="lang-text" class="sr-only">EN</span>
                </button>
                <button class="menu-btn" id="menuBtn" type="button" aria-label="打开菜单" aria-expanded="false" aria-controls="mobileMenu">
                    <svg viewBox="0 0 24 24" width="18" height="18" style="stroke:currentColor;fill:none;stroke-width:2.4"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg>
                </button>
            </div>
        </div>
    </nav>

    <!-- 移动端菜单 -->
    <div class="mobile-menu" id="mobileMenu">
        <a href="#features" data-en="Features" data-zh="特性">特性</a>
        <a href="#requirements" data-en="Requirements" data-zh="配置要求">配置要求</a>
        <a href="#faq" data-en="FAQ" data-zh="常见问题">常见问题</a>
        <a href="#credits" data-en="Credits" data-zh="致谢">致谢</a>
        <a href="#download" data-en="Download" data-zh="下载">下载</a>
        <a href="https://github.com/zhibha/Spark-Launcher" target="_blank" rel="noopener">GitHub</a>
    </div>

    <!-- 首屏 -->
    <main>
    <section id="hero">
        <div class="badge fade-up"><span class="dot"></span><span data-en="Open-source · Non-commercial · GPL-3.0" data-zh="开源 · 非商业 · GPL-3.0">开源 · 非商业 · GPL-3.0</span></div>
        <h1 class="fade-up" data-en='Minecraft: Java Edition<br>on <span>Android</span>' data-zh='Minecraft: Java 版<br>登陆 <span>Android</span>'>
            Minecraft: Java 版<br>登陆 <span>Android</span>
        </h1>
        <p class="fade-up" data-en="Spark Launcher is an open-source, non-commercial third-party launcher built for Android devices. It uses the official Microsoft OAuth 2.0 Device Code Flow for secure authentication, letting players verify game ownership and join online-mode multiplayer servers." data-zh="Spark Launcher 是一款专为 Android 设备打造的开源、非商业第三方启动器。它采用微软官方 OAuth 2.0 设备代码流进行安全认证，让你验证游戏所有权并加入正版（在线模式）多人服务器。">
            Spark Launcher 是一款专为 Android 设备打造的开源、非商业第三方启动器。它采用微软官方 OAuth 2.0 设备代码流进行安全认证，让你验证游戏所有权并加入正版（在线模式）多人服务器。
        </p>
        <div class="btn-group fade-up">
            <a href="#download" class="btn btn-primary" data-en="Download Now" data-zh="立即下载">立即下载</a>
            <a href="https://github.com/zhibha/Spark-Launcher" target="_blank" rel="noopener" class="btn btn-glass" data-en="View on GitHub" data-zh="在 GitHub 查看">在 GitHub 查看</a>
        </div>

        <div class="hero-meta fade-up">
            <span><svg viewBox="0 0 24 24" aria-hidden="true"><polyline points="20 6 9 17 4 12"/></svg><span data-en="No ads, no fees" data-zh="无广告、无内购">无广告、无内购</span></span>
            <span><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg><span data-en="Official Microsoft login" data-zh="微软官方登录">微软官方登录</span></span>
            <span><svg viewBox="0 0 24 24" aria-hidden="true"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg><span data-en="Requires a legit copy" data-zh="需拥有正版游戏">需拥有正版游戏</span></span>
        </div>
    </section>

    <!-- 特性 -->
    <section id="features">
        <h2 class="section-title fade-up" data-en="Why Spark Launcher?" data-zh="为什么选择 Spark Launcher？">为什么选择 Spark Launcher？</h2>
        <p class="section-subtitle fade-up" data-en="Built with a modern stack for performance, stability, and full compliance." data-zh="采用现代技术构建，为性能、稳定性和合规性而生。">采用现代技术构建，为性能、稳定性和合规性而生。</p>

        <div class="features-grid">
            <div class="feature-card glass-card fade-up">
                <div class="feature-icon">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect><path d="M7 11V7a5 5 0 0 1 10 0v4"></path></svg>
                </div>
                <h3 data-en="Official Microsoft Login" data-zh="微软官方正版登录">微软官方正版登录</h3>
                <p data-en="Secure OAuth 2.0 flow with your official Microsoft account. It verifies game ownership, supports online-mode servers, and retrieves your profile and skin safely." data-zh="使用官方微软账号走 OAuth 2.0 安全认证。会验证游戏所有权，支持在线模式服务器，并安全获取你的档案和皮肤。">
                    使用官方微软账号走 OAuth 2.0 安全认证。会验证游戏所有权，支持在线模式服务器，并安全获取你的档案和皮肤。
                </p>
            </div>

            <div class="feature-card glass-card fade-up" style="transition-delay:.08s">
                <div class="feature-icon">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
                </div>
                <h3 data-en="Modern Technical Stack" data-zh="现代技术栈">现代技术栈</h3>
                <p data-en="Kotlin + Android SDK, powered by OpenJDK 17 and MobileGlues for high-performance graphics translation — smooth gameplay across a wide range of Android devices." data-zh="Kotlin + Android SDK 构建，由 OpenJDK 17 与 MobileGlues 高性能图形翻译层驱动，在大量 Android 设备上保持流畅。">
                    Kotlin + Android SDK 构建，由 OpenJDK 17 与 MobileGlues 高性能图形翻译层驱动，在大量 Android 设备上保持流畅。
                </p>
            </div>

            <div class="feature-card glass-card fade-up" style="transition-delay:.16s">
                <div class="feature-icon">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><circle cx="12" cy="12" r="3"></circle><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"></path></svg>
                </div>
                <h3 data-en="100% Free &amp; Open Source" data-zh="100% 免费开源">100% 免费开源</h3>
                <p data-en="Completely free, open-source, and strictly non-commercial. No ads, no paid tiers, no hidden fees. Community-driven, distributed under GPL-3.0." data-zh="完全免费、开源、严格非商业。没有广告，没有付费档位，也没有隐藏费用。由社区驱动，基于 GPL-3.0 分发。">
                    完全免费、开源、严格非商业。没有广告，没有付费档位，也没有隐藏费用。由社区驱动，基于 GPL-3.0 分发。
                </p>
            </div>

            <div class="feature-card glass-card fade-up" style="transition-delay:.24s">
                <div class="feature-icon">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path></svg>
                </div>
                <h3 data-en="EULA Compliant" data-zh="符合 EULA">符合 EULA</h3>
                <p data-en="No game files are distributed, no authentication is bypassed, piracy is not promoted. You must own a legitimate copy. Not an official Minecraft product; not affiliated with Mojang or Microsoft." data-zh="不分发游戏文件、不绕过认证、不鼓励盗版。你必须拥有正版游戏。本产品非官方 Minecraft 产品，与 Mojang 或 Microsoft 无隶属关系。">
                    不分发游戏文件、不绕过认证、不鼓励盗版。你必须拥有正版游戏。本产品非官方 Minecraft 产品，与 Mojang 或 Microsoft 无隶属关系。
                </p>
            </div>
        </div>
    </section>

    <!-- 配置要求 -->
    <section id="requirements">
        <h2 class="section-title fade-up" data-en="Requirements" data-zh="配置要求">配置要求</h2>
        <p class="section-subtitle fade-up" data-en="These are the baseline targets. Lower-end devices may need reduced render distance." data-zh="以下为基线目标。性能较弱的设备建议调低视距与画质。">以下为基线目标。性能较弱的设备建议调低视距与画质。</p>
        <div class="req-grid fade-up">
            <div class="req-item glass-card">
                <span class="k">Android</span>
                <span class="v">8.0+</span>
                <span class="n" data-en="API 26 or newer" data-zh="API 26 及以上">API 26 及以上</span>
            </div>
            <div class="req-item glass-card">
                <span class="k">ABI</span>
                <span class="v">arm64</span>
                <span class="n" data-en="64-bit device recommended" data-zh="推荐 64 位设备">推荐 64 位设备</span>
            </div>
            <div class="req-item glass-card">
                <span class="k">RAM</span>
                <span class="v">3 GB+</span>
                <span class="n" data-en="The more the better" data-zh="越大越稳">越大越稳</span>
            </div>
            <div class="req-item glass-card">
                <span class="k">Runtime</span>
                <span class="v">JDK 17</span>
                <span class="n" data-en="Bundled with the launcher" data-zh="启动器内置">启动器内置</span>
            </div>
        </div>
    </section>

    <!-- 常见问题 -->
    <section id="faq">
        <h2 class="section-title fade-up" data-en="FAQ" data-zh="常见问题">常见问题</h2>
        <p class="section-subtitle fade-up" data-en="The things people ask most." data-zh="问得最多的几件事。">问得最多的几件事。</p>

        <div class="faq-list fade-up">
            <details class="faq">
                <summary data-en="Do I need to own Minecraft?" data-zh="我需要买正版吗？">我需要买正版吗？</summary>
                <p data-en="Yes. Spark Launcher does not bypass authentication or distribute game files. You need a legitimate Minecraft: Java Edition account to log in and join online-mode servers." data-zh="需要。Spark Launcher 不绕过认证，也不分发游戏文件。你必须拥有正版的 Minecraft: Java 版账号，才能登录并进入在线模式服务器。">需要。Spark Launcher 不绕过认证，也不分发游戏文件。你必须拥有正版的 Minecraft: Java 版账号，才能登录并进入在线模式服务器。</p>
            </details>

            <details class="faq">
                <summary data-en="Is it really free?" data-zh="真的完全免费吗？">真的完全免费吗？</summary>
                <p data-en="Yes. No ads, no subscriptions, no in-app purchases. The source is open under GPL-3.0 — you can read it, build it, and modify it." data-zh="是。没有广告、没有订阅、没有内购。源码以 GPL-3.0 开源，你可以自行阅读、编译和修改。">是。没有广告、没有订阅、没有内购。源码以 GPL-3.0 开源，你可以自行阅读、编译和修改。</p>
            </details>

            <details class="faq">
                <summary data-en="Will it run on my phone?" data-zh="我的手机能跑吗？">我的手机能跑吗？</summary>
                <p data-en="Android 8.0+ and a 64-bit (arm64) device is the baseline. 3 GB of RAM or more is recommended. On weaker devices, lower the render distance first." data-zh="基线是 Android 8.0+、64 位（arm64）设备，建议 3 GB 内存以上。设备较弱时，先调低视距。">基线是 Android 8.0+、64 位（arm64）设备，建议 3 GB 内存以上。设备较弱时，先调低视距。</p>
            </details>

            <details class="faq">
                <summary data-en="Where do I report bugs?" data-zh="遇到 bug 去哪反馈？">遇到 bug 去哪反馈？</summary>
                <p data-en="Open an issue on GitHub. Please include your device model, Android version, and the log from the launcher — it saves a round trip." data-zh="去 GitHub 提 issue。记得带上设备型号、Android 版本和启动器里的日志，能省一轮来回。">去 GitHub 提 issue。记得带上设备型号、Android 版本和启动器里的日志，能省一轮来回。</p>
            </details>

            <details class="faq">
                <summary data-en="Can I redistribute or fork it?" data-zh="我能二次分发或 fork 吗？">我能二次分发或 fork 吗？</summary>
                <p data-en="Forking is welcome under GPL-3.0, as long as you keep the license and don't present it as an official Minecraft product. Commercial redistribution is not permitted by the project's non-commercial stance." data-zh="在 GPL-3.0 下欢迎 fork，前提是保留许可证，并且不要把它包装成官方 Minecraft 产品。按照本项目的非商业立场，不允许商业再分发。">在 GPL-3.0 下欢迎 fork，前提是保留许可证，并且不要把它包装成官方 Minecraft 产品。按照本项目的非商业立场，不允许商业再分发。</p>
            </details>
        </div>
    </section>

    <!-- 社区致谢 -->
    <section id="credits">
        <h2 class="section-title fade-up" data-en="Community &amp; Inspirations" data-zh="社区与灵感来源">社区与灵感来源</h2>
        <p class="section-subtitle fade-up" data-en="Spark Launcher stands on the shoulders of giants. Thanks to these open-source projects that paved the way for Minecraft on mobile." data-zh="Spark Launcher 站在巨人的肩膀上。感谢这些为移动端 Minecraft 铺平道路的开源项目。">Spark Launcher 站在巨人的肩膀上。感谢这些为移动端 Minecraft 铺平道路的开源项目。</p>
        <div class="credits-container fade-up">
            <a class="credit-pill" href="https://github.com/Hex-Dragon/PCL2" target="_blank" rel="noopener" title="Plain Craft Launcher 2">PCL2</a>
            <a class="credit-pill" href="https://github.com/ZalithLauncher/ZalithLauncher2" target="_blank" rel="noopener" title="Zalith Launcher 2">ZL2</a>
            <a class="credit-pill" href="https://github.com/FCL-Team/FoldCraftLauncher" target="_blank" rel="noopener" title="Fold Craft Launcher">FCL</a>
            <a class="credit-pill" href="https://github.com/PojavLauncherTeam/PojavLauncher" target="_blank" rel="noopener" title="PojavLauncher">PojavLauncher</a>
            <a class="credit-pill" href="https://github.com/AngelAuraMC/Amethyst-Android" target="_blank" rel="noopener" title="Amethyst">Amethyst</a>
        </div>
    </section>

    <!-- 下载 -->
    <section id="download" class="fade-up">
        <div class="glass-card">
            <h2 class="section-title" data-en="Ready to Play?" data-zh="准备好开始了吗？">准备好开始了吗？</h2>
            <p class="section-subtitle" style="margin-bottom:2.2rem" data-en="Download the latest APK from GitHub Releases." data-zh="从 GitHub Releases 下载最新的 APK。" >从 GitHub Releases 下载最新的 APK。</p>
            <a href="https://github.com/zhibha/Spark-Launcher/releases/latest" class="btn btn-primary" style="font-size:1.05rem;padding:1rem 3rem" data-en="Download APK" data-zh="下载 APK">下载 APK</a>
            <p class="dl-note" data-en="Android 8.0+ · arm64 recommended · JDK 17 bundled" data-zh="Android 8.0+ · 推荐 arm64 · 内置 JDK 17">Android 8.0+ · 推荐 arm64 · 内置 JDK 17</p>
            <p class="dl-sub">
                <a href="https://github.com/zhibha/Spark-Launcher/releases" target="_blank" rel="noopener" data-en="All releases" data-zh="查看全部版本">查看全部版本</a>
                <span> · </span>
                <a href="https://github.com/zhibha/Spark-Launcher/blob/main/LICENSE" target="_blank" rel="noopener" data-en="License" data-zh="开源许可">开源许可</a>
            </p>
        </div>
    </section>
    </main>

    <!-- 移动端底部标签栏 -->
    <nav class="tabbar" id="tabbar" aria-label="页面导航">
        <div class="tabbar-inner">
            <a class="tab" href="#features" data-target="features">
                <svg viewBox="0 0 24 24" aria-hidden="true"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                <span data-en="Features" data-zh="特性">特性</span>
            </a>
            <a class="tab" href="#requirements" data-target="requirements">
                <svg viewBox="0 0 24 24" aria-hidden="true"><rect x="4" y="3" width="16" height="18" rx="2"/><line x1="8" y1="8" x2="16" y2="8"/><line x1="8" y1="12" x2="16" y2="12"/><line x1="8" y1="16" x2="12" y2="16"/></svg>
                <span data-en="Specs" data-zh="要求">要求</span>
            </a>
            <a class="tab" href="#faq" data-target="faq">
                <svg viewBox="0 0 24 24" aria-hidden="true"><circle cx="12" cy="12" r="9"/><path d="M9.5 9a2.6 2.6 0 0 1 5 .9c0 1.7-2.5 2-2.5 3.6"/><line x1="12" y1="17" x2="12" y2="17.01"/></svg>
                <span data-en="FAQ" data-zh="问题">问题</span>
            </a>
            <a class="tab" href="#download" data-target="download">
                <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12 3v12"/><polyline points="7 11 12 16 17 11"/><path d="M4 20h16"/></svg>
                <span data-en="Download" data-zh="下载">下载</span>
            </a>
        </div>
    </nav>

    <!-- 页脚 -->
    <footer>
        <div class="disclaimer">
            <strong data-en="Disclaimer: " data-zh="免责声明：">免责声明：</strong><span data-en="Spark Launcher is NOT an official Minecraft product. We are not approved by or associated with Mojang or Microsoft. You must own a legitimate copy of Minecraft: Java Edition to play." data-zh="Spark Launcher 不是官方 Minecraft 产品。我们未获得 Mojang 或 Microsoft 的批准，也不与其关联。你必须拥有 Minecraft: Java 版的合法副本才能游戏。">Spark Launcher 不是官方 Minecraft 产品。我们未获得 Mojang 或 Microsoft 的批准，也不与其关联。你必须拥有 Minecraft: Java 版的合法副本才能游戏。</span>
        </div>

        <div class="footer-links">
            <a href="https://github.com/zhibha/Spark-Launcher" target="_blank" rel="noopener">GitHub</a>
            <a href="https://github.com/zhibha/Spark-Launcher/releases" target="_blank" rel="noopener" data-en="Releases" data-zh="版本发布">版本发布</a>
            <a href="https://github.com/zhibha/Spark-Launcher/issues" target="_blank" rel="noopener" data-en="Issues" data-zh="问题反馈">问题反馈</a>
            <a href="https://github.com/zhibha/Spark-Launcher/blob/main/LICENSE" target="_blank" rel="noopener" data-en="License (GPL-3.0)" data-zh="许可证（GPL-3.0）">许可证（GPL-3.0）</a>
        </div>

        <p>© <span id="year">2026</span> Spark Launcher · <span data-en="Licensed under GPL-3.0" data-zh="基于 GPL-3.0 许可">基于 GPL-3.0 许可</span></p>
    </footer>

    <button class="to-top" id="toTop" type="button" aria-label="返回顶部">
        <svg viewBox="0 0 24 24" aria-hidden="true"><polyline points="18 15 12 9 6 15"/></svg>
    </button>

    <script>
        // ============ 语言切换（记忆 + 同步 html lang / title） ============
        const TITLES = {
            zh: 'Spark Launcher · Android 上的 Minecraft Java 版启动器',
            en: 'Spark Launcher · Minecraft Java Edition for Android'
        };
        const LABEL = { zh: 'EN', en: '中文' };
        let currentLang = localStorage.getItem('spark-lang')
            || (navigator.language && navigator.language.toLowerCase().startsWith('zh') ? 'zh' : 'en');

        function applyLang(lang) {
            currentLang = lang;
            document.documentElement.lang = lang === 'zh' ? 'zh-CN' : 'en';
            document.title = TITLES[lang];
            document.querySelectorAll('[data-en][data-zh]').forEach(el => {
                el.innerHTML = el.getAttribute(lang === 'zh' ? 'data-zh' : 'data-en');
            });
            const t = document.getElementById('lang-text');
            if (t) t.textContent = LABEL[lang];
            const btn = document.getElementById('langBtn');
            if (btn) {
                btn.dataset.tip = lang === 'zh' ? 'English' : '中文';
                btn.setAttribute('aria-label', lang === 'zh' ? 'Switch to English' : '切换到中文');
            }
            localStorage.setItem('spark-lang', lang);
        }

        document.getElementById('langBtn').addEventListener('click', () => {
            applyLang(currentLang === 'zh' ? 'en' : 'zh');
        });
        applyLang(currentLang);

        // ============ 滚动渐入 ============
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });
        document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

        // 不支持 IO 的旧环境直接显示
        if (!('IntersectionObserver' in window)) {
            document.querySelectorAll('.fade-up').forEach(el => el.classList.add('visible'));
        }

        // ============ 卡片液态光晕 ============
        document.querySelectorAll('.glass-card').forEach(card => {
            card.addEventListener('mousemove', e => {
                const rect = card.getBoundingClientRect();
                card.style.setProperty('--mouse-x', (e.clientX - rect.left) + 'px');
                card.style.setProperty('--mouse-y', (e.clientY - rect.top) + 'px');
            });
        });

        // ============ 导航 / 返回顶部 ============
        const nav = document.getElementById('nav');
        const toTop = document.getElementById('toTop');
        const onScroll = () => {
            const y = window.scrollY;
            nav.classList.toggle('scrolled', y > 20);
            toTop.classList.toggle('show', y > 600);
        };
        window.addEventListener('scroll', onScroll, { passive: true });
        onScroll();
        toTop.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));

        // ============ 移动端菜单 ============
        const menuBtn = document.getElementById('menuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        menuBtn.addEventListener('click', () => {
            const open = mobileMenu.classList.toggle('open');
            menuBtn.setAttribute('aria-expanded', String(open));
        });
        mobileMenu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => {
            mobileMenu.classList.remove('open');
            menuBtn.setAttribute('aria-expanded', 'false');
        }));

        // ============ 年份 ============
        document.getElementById('year').textContent = new Date().getFullYear();

        // ============ 平台识别：iOS / Android 材质微调 ============
        (function detectPlatform() {
            const ua = navigator.userAgent || '';
            const isIOS = /iPad|iPhone|iPod/.test(ua) ||
                (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1);
            const isAndroid = /Android/i.test(ua);
            document.documentElement.classList.add(isIOS ? 'platform-ios' : isAndroid ? 'platform-android' : 'platform-web');
        })();

        // ============ 底部标签栏高亮（根据当前视口内区块） ============
        (function tabSpy() {
            const tabs = Array.from(document.querySelectorAll('.tab'));
            if (!tabs.length) return;
            const sections = tabs
                .map(t => document.getElementById(t.dataset.target))
                .filter(Boolean);
            const setActive = (id) => tabs.forEach(t => t.classList.toggle('active', t.dataset.target === id));
            if ('IntersectionObserver' in window) {
                const io = new IntersectionObserver((entries) => {
                    const visible = entries
                        .filter(e => e.isIntersecting)
                        .sort((a, b) => b.intersectionRatio - a.intersectionRatio)[0];
                    if (visible) setActive(visible.target.id);
                }, { rootMargin: '-45% 0px -45% 0px', threshold: [0, .2, .5] });
                sections.forEach(s => io.observe(s));
            }
            tabs.forEach(t => t.addEventListener('click', () => setActive(t.dataset.target)));
        })();
    </script>
</body>
</html>
