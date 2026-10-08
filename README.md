<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>百工专列英语 · 景德镇站 | 高铁乘务英语实训系统</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        :root {
            --porcelain-white: #f8fbff;
            --cobalt-blue: #0f3557;
            --mid-blue: #2a6ea8;
            --light-blue: #7dd3fc;
            --gold-accent: #c99f4a;
            --ink-blue: #1a2a3a;
            --text-muted: #5a6e82;
        }
        * { margin:0; padding:0; box-sizing:border-box; }
        body { 
            font-family:'Segoe UI','PingFang SC',Roboto,sans-serif; 
            background-color: var(--porcelain-white);
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 60 60"><path d="M30 0 C40 15 50 15 60 30 C50 45 40 45 30 60 C20 45 10 45 0 30 C10 15 20 15 30 0 Z" fill="none" stroke="%23e2eff9" stroke-width="1"/></svg>');
            color: var(--ink-blue); 
            padding-top:68px; 
            line-height:1.6; 
        }
        .navbar { 
            position:fixed; top:0; left:0; right:0; z-index:1000; 
            background:linear-gradient(145deg, #0a2540, #184e77); 
            padding:0 14px; height:64px; display:flex; align-items:center; justify-content:space-between; 
            box-shadow:0 4px 20px rgba(10,37,64,0.4); gap:4px; flex-wrap:nowrap; 
            border-bottom: 2px solid var(--gold-accent);
        }
        .navbar .brand { display:flex; align-items:center; gap:8px; color:#fff; font-weight:700; font-size:0.85rem; white-space:nowrap; }
        .navbar .brand i { color:var(--light-blue); font-size:1.1rem; }
        .navbar .brand span { font-size:0.6rem; font-weight:400; opacity:0.6; }
        .navbar .nav-links { display:flex; gap:2px; flex-wrap:nowrap; overflow-x:auto; }
        .navbar .nav-links a { color:rgba(255,255,255,0.6); text-decoration:none; padding:4px 10px; border-radius:30px; font-size:0.65rem; font-weight:600; transition:all 0.25s; white-space:nowrap; cursor:pointer; }
        .navbar .nav-links a:hover { color:#fff; background:rgba(255,255,255,0.08); }
        .navbar .nav-links a.active { color:var(--cobalt-blue); background:var(--light-blue); }
        .navbar .right-actions { display:flex; align-items:center; gap:6px; flex-shrink:0; }
        .navbar .print-btn { background:rgba(255,255,255,0.1); border:1px solid rgba(255,255,255,0.15); color:#fff; padding:3px 12px; border-radius:30px; font-size:0.6rem; font-weight:600; cursor:pointer; display:flex; align-items:center; gap:4px; }
        .navbar .print-btn:hover { background:rgba(255,255,255,0.2); }
        .container { max-width:1100px; margin:0 auto; padding:12px 14px 30px; }
        .page { display:none; animation:fadeUp 0.3s ease; }
        .page.active { display:block; }
        @keyframes fadeUp { from { opacity:0; transform:translateY(10px); } to { opacity:1; transform:translateY(0); } }
        
        .card { 
            background:#fff; border-radius:16px; padding:18px 20px; 
            box-shadow:0 4px 16px rgba(15,53,87,0.06); 
            margin-bottom:18px; border:1px solid #d6eaf8; 
            position: relative; overflow: hidden;
        }
        .card::before {
            content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
            background: linear-gradient(90deg, var(--mid-blue), var(--light-blue), var(--gold-accent));
        }
        .card-title { font-size:1.05rem; font-weight:700; color:var(--cobalt-blue); margin-bottom:12px; display:flex; align-items:center; gap:10px; }
        .card-title i { color:var(--mid-blue); font-size:1rem; }
        .card-title .sub { font-weight:400; font-size:0.7rem; color:#8a9eb0; margin-left:auto; }
        .section-desc { color:var(--text-muted); font-size:0.9rem; margin-bottom:12px; }
        .form-row { display:grid; grid-template-columns:repeat(auto-fit,minmax(180px,1fr)); gap:12px; }
        .form-group { display:flex; flex-direction:column; gap:3px; }
        .form-group label { font-weight:600; font-size:0.78rem; color:var(--cobalt-blue); }
        .form-group input { padding:6px 12px; border-radius:8px; border:1px solid #dce4ec; font-size:0.85rem; background:#fafcff; font-family:inherit; }
        .form-group input:focus { border-color:var(--mid-blue); outline:none; box-shadow:0 0 0 3px rgba(42,110,168,0.1); }
        .btn { padding:5px 16px; border-radius:30px; border:none; font-weight:600; font-size:0.75rem; cursor:pointer; transition:all 0.2s; display:inline-flex; align-items:center; gap:5px; }
        .btn-primary { background:var(--light-blue); color:var(--cobalt-blue); }
        .btn-primary:hover { background:#bae6fd; }
        .btn-success { background:#2d7d5a; color:#fff; }
        .btn-success:hover { background:#3a9d72; }
        .btn-outline { background:transparent; border:1.5px solid #dce4ec; color:var(--text-muted); }
        .btn-outline:hover { border-color:#b6cce0; background:#f7faff; }
        .btn-sm { padding:3px 12px; font-size:0.65rem; }
        .text-muted { color:#8a9eb0; font-size:0.78rem; }
        .text-gold { color:var(--gold-accent); }

        .case-banner {
            width: 100%; height: 200px; border-radius: 12px; margin-bottom: 16px;
            background: linear-gradient(135deg, #0f3557, #2a6ea8);
            display: flex; align-items: center; justify-content: center;
            color: #fff; position: relative; overflow: hidden;
            border: 2px solid var(--gold-accent);
            text-align: center;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80"><path d="M40 0 C55 20 65 20 80 40 C65 60 55 60 40 80 C25 60 15 60 0 40 C15 20 25 20 40 0 Z" fill="none" stroke="%23ffffff" stroke-opacity="0.08" stroke-width="1.5"/></svg>');
            background-size: 80px 80px;
        }
        .case-banner-text {
            padding: 20px;
            z-index: 1;
        }
        .case-banner-text h2 {
            font-size: 1.6rem; letter-spacing: 4px; color: #fff; margin: 0;
            text-shadow: 0 2px 8px rgba(0,0,0,0.2);
        }
        .case-banner-text p {
            font-size: 1rem; color: #bae6fd; margin-top: 6px; letter-spacing: 1px;
        }
        .case-banner-text span {
            display: inline-block; margin-top: 14px; background: rgba(255,255,255,0.15);
            padding: 5px 20px; border-radius: 30px; font-size: 0.8rem; backdrop-filter: blur(4px);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .vocab-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(250px,1fr)); gap:12px; }
        .vocab-card { background:#f0f8fd; border-radius:12px; padding:14px 16px; border:1px solid #d6eaf8; transition:0.2s; }
        .vocab-card:hover { border-color:var(--light-blue); background:#e0f2fe; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(42,110,168,0.1); }
        .vocab-card .word-row { display:flex; align-items:center; gap:8px; flex-wrap:wrap; }
        .vocab-card .word { font-weight:700; font-size:1.05rem; color:var(--cobalt-blue); cursor:pointer; padding:2px 6px; border-radius:6px; }
        .vocab-card .word:hover { color:var(--mid-blue); background:rgba(42,110,168,0.1); }
        .vocab-card .word.speaking { background:var(--mid-blue); color:#fff; animation:pulse-icon 0.8s infinite; }
        .vocab-card .phonetic { font-size:0.8rem; color:#8a9eb0; }
        .vocab-card .meaning { font-size:0.85rem; color:var(--text-muted); margin:4px 0 6px; }
        .vocab-card .actions { display:flex; align-items:center; gap:6px; flex-wrap:wrap; margin-top:6px; }
        .vocab-card .speak-btn { background:rgba(42,110,168,0.12); border:none; color:var(--mid-blue); width:30px; height:30px; border-radius:50%; cursor:pointer; font-size:0.8rem; }
        .vocab-card .speak-btn:hover { background:var(--mid-blue); color:#fff; }
        .vocab-card .record-btn { background:rgba(52,152,219,0.12); border:none; color:#2980b9; width:30px; height:30px; border-radius:50%; cursor:pointer; font-size:0.8rem; }
        .vocab-card .record-btn:hover { background:#2980b9; color:#fff; }
        .vocab-card .record-btn.recording { background:#c0392b; color:#fff; animation:pulse-icon 0.6s infinite; }
        .vocab-card .score-display { margin-top:6px; font-size:0.8rem; font-weight:600; display:flex; align-items:center; gap:6px; }
        .vocab-card .score-value { padding:2px 10px; border-radius:20px; font-size:0.85rem; }
        .score-excellent { background:#d4edda; color:#1a6e4a; }
        .score-good { background:#d6eaf8; color:#1a5276; }
        .score-fair { background:#fdebd0; color:#935e38; }
        .score-poor { background:#fadbd8; color:#922b21; }
        .score-none { background:#e6edf6; color:#8a9eb0; }
        @keyframes pulse-icon { 0%,100% { transform:scale(1); opacity:1; } 50% { transform:scale(0.85); opacity:0.6; } }
        .recognition-status { font-size:0.75rem; color:var(--text-muted); padding:4px 10px; border-radius:20px; background:#f0f4f9; display:inline-block; margin-top:4px; }
        .recognition-status.active { background:#d6eaf8; color:#1a5276; }
        .recognition-status.success { background:#d4edda; color:#1a6e4a; }
        .recognition-status.error { background:#fadbd8; color:#922b21; }

        .phrase-section { margin-bottom:20px; }
        .phrase-section-title { font-weight:700; font-size:0.95rem; color:var(--cobalt-blue); padding:8px 14px; background:#f0f8fd; border-radius:10px; margin-bottom:8px; display:flex; align-items:center; gap:10px; border-left: 4px solid var(--mid-blue); }
        .phrase-section-title .badge { font-size:0.65rem; font-weight:600; background:var(--mid-blue); color:#fff; padding:0 12px; border-radius:20px; line-height:1.8; }
        .phrase-item { padding:10px 14px; background:#f8fbff; border-radius:10px; border-left:4px solid var(--light-blue); margin-bottom:6px; transition:0.2s; }
        .phrase-item:hover { background:#e0f2fe; transform: translateX(4px); }
        .phrase-item .en-line { display:flex; flex-wrap:wrap; align-items:center; gap:3px; margin-bottom:6px; }
        .phrase-item .en-line .word-chip { display:inline-block; padding:2px 7px; border-radius:6px; font-weight:600; font-size:0.92rem; color:var(--cobalt-blue); cursor:pointer; user-select:none; transition:0.15s; }
        .phrase-item .en-line .word-chip:hover { background:rgba(42,110,168,0.15); color:var(--mid-blue); }
        .phrase-item .en-line .word-chip.speaking { background:var(--mid-blue); color:#fff; animation:pulse-icon 0.8s infinite; }
        .phrase-item .zh-line { color:var(--text-muted); font-size:0.85rem; padding-left:2px; margin-bottom:6px; }
        .phrase-item .sentence-actions { display:flex; align-items:center; gap:8px; flex-wrap:wrap; padding-top:6px; border-top:1px dashed #d6eaf8; }
        .btn-sentence { background:linear-gradient(135deg,var(--mid-blue),var(--light-blue)); border:none; color:#fff; padding:5px 14px; border-radius:20px; font-size:0.72rem; font-weight:600; cursor:pointer; display:inline-flex; align-items:center; gap:5px; transition:0.2s; box-shadow:0 2px 6px rgba(42,110,168,0.25); }
        .btn-sentence:hover { background:linear-gradient(135deg,#0f3557,var(--mid-blue)); transform:translateY(-1px); }
        .btn-sentence.playing { background:linear-gradient(135deg,#2d7d5a,#3a9d72); animation:pulse-icon 0.8s infinite; }

        .dialogue-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(500px,1fr)); gap:20px; }
        .dialogue-card { background:#ffffff; border-radius:16px; padding:20px 22px; border:1px solid #d6eaf8; box-shadow:0 2px 6px rgba(0,0,0,0.02); display:flex; flex-direction:column; }
        .dialogue-card:hover { border-color:var(--light-blue); box-shadow:0 8px 24px rgba(42,110,168,0.1); }
        .dialogue-card .d-header { display:flex; align-items:center; gap:12px; margin-bottom:14px; flex-wrap:wrap; border-bottom:1px solid #f0f8fd; padding-bottom:10px; }
        .dialogue-card .d-num { font-size:0.65rem; font-weight:700; color:var(--mid-blue); background:rgba(42,110,168,0.12); padding:3px 14px; border-radius:30px; }
        .dialogue-card .d-title { font-weight:700; font-size:1.05rem; color:var(--cobalt-blue); }
        .dialogue-card .d-scene-label { font-size:0.7rem; color:#8a9eb0; margin-left:auto; background:#d6eaf8; padding:2px 14px; border-radius:30px; }
        .dialogue-card .d-body { display:flex; flex-direction:column; gap:8px; margin:6px 0 12px; max-height:640px; overflow-y:auto; padding-right:4px; }
        .dialogue-card .d-body::-webkit-scrollbar { width:4px; }
        .dialogue-card .d-body::-webkit-scrollbar-thumb { background:var(--mid-blue); border-radius:10px; }
        .dialogue-card .d-line { padding:10px 14px; border-radius:12px; background:#f0f8fd; border-left:4px solid var(--light-blue); transition:0.15s; }
        .dialogue-card .d-line.crew { background:#e8f4fd; border-left-color:var(--cobalt-blue); }
        .dialogue-card .d-line.passenger { background:#f7faff; border-left-color:#2980b9; }
        .dialogue-card .d-line .d-speaker { font-weight:700; font-size:0.8rem; color:var(--text-muted); display:flex; align-items:center; gap:6px; margin-bottom:4px; }
        .dialogue-card .d-line .d-en-line { display:flex; flex-wrap:wrap; align-items:center; gap:3px; margin-bottom:4px; }
        .dialogue-card .d-line .d-en-line .word-chip { display:inline-block; padding:2px 7px; border-radius:6px; font-weight:600; font-size:0.98rem; color:var(--ink-blue); cursor:pointer; user-select:none; transition:0.15s; }
        .dialogue-card .d-line .d-en-line .word-chip:hover { background:rgba(42,110,168,0.15); color:var(--mid-blue); }
        .dialogue-card .d-line .d-en-line .word-chip.speaking { background:var(--mid-blue); color:#fff; animation:pulse-icon 0.8s infinite; }
        .dialogue-card .d-line .d-trans { font-size:0.88rem; color:var(--text-muted); line-height:1.5; padding-top:4px; border-top:1px dashed rgba(0,0,0,0.05); margin-bottom:6px; }
        .dialogue-card .d-line .d-actions { display:flex; align-items:center; gap:8px; flex-wrap:wrap; }
        .dialogue-card .d-audio-bar { display:flex; align-items:center; gap:8px; margin-top:12px; padding-top:12px; border-top:1px solid #d6eaf8; flex-wrap:wrap; }
        .dialogue-card .d-audio-bar .btn-audio-sm { background:rgba(42,110,168,0.1); border:none; color:var(--mid-blue); padding:5px 14px; border-radius:30px; font-size:0.7rem; font-weight:600; cursor:pointer; display:inline-flex; align-items:center; gap:6px; }
        .dialogue-card .d-audio-bar .btn-audio-sm:hover { background:var(--mid-blue); color:#fff; }
        .dialogue-card .d-audio-bar .btn-audio-sm.playing { background:#2d7d5a; color:#fff; animation:pulse-icon 0.8s infinite; }
        .dialogue-card .d-audio-bar .btn-recording-sm { background:rgba(41,128,185,0.1); border:none; color:#2980b9; padding:5px 14px; border-radius:30px; font-size:0.7rem; font-weight:600; cursor:pointer; display:inline-flex; align-items:center; gap:6px; }
        .dialogue-card .d-audio-bar .btn-recording-sm:hover { background:#2980b9; color:#fff; }
        .dialogue-card .d-audio-bar .btn-recording-sm.recording { background:#c0392b; color:#fff; animation:pulse-icon 0.6s infinite; }
        .dialogue-card .d-audio-bar .btn-recording-sm:disabled { opacity:0.45; cursor:not-allowed; }
        .dialogue-card .d-audio-bar .d-status { font-size:0.7rem; color:#8a9eb0; }
        .dialogue-card .d-audio-bar .d-status.done { color:#2d7d5a; font-weight:600; }

        .case-card { display:grid; grid-template-columns:1fr 1fr; gap:16px; }
        .case-card .info-item { background:#f8fbff; border-radius:10px; padding:12px 16px; border:1px solid #d6eaf8; border-left: 4px solid var(--mid-blue); }
        .case-card .info-item .label { font-weight:600; font-size:0.75rem; color:#8a9eb0; }
        .case-card .info-item .value { font-weight:700; font-size:1rem; color:var(--cobalt-blue); margin-top:2px; }
        .case-card .info-item .value.en { color:var(--mid-blue); font-weight:600; font-size:0.9rem; }
        .case-card .info-item .value.zh { color:var(--text-muted); font-size:0.85rem; }
        @media (max-width:600px) { .case-card { grid-template-columns:1fr; } }

        .role-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(180px,1fr)); gap:12px; }
        .role-card { background:#f8fbff; border-radius:12px; padding:12px 14px; border:1px solid #d6eaf8; border-top: 3px solid var(--light-blue); }
        .role-card .r-title { font-weight:700; font-size:0.85rem; color:var(--cobalt-blue); display:flex; align-items:center; gap:6px; }
        .role-card .r-title .icon { color:var(--mid-blue); }
        .role-card .r-name input { width:100%; padding:4px 10px; border-radius:6px; border:1px solid #dce4ec; font-size:0.8rem; background:#fff; margin-top:4px; }

        .script-step { display:flex; align-items:center; gap:10px; padding:8px 12px; background:#f8fbff; border-radius:8px; border:1px solid #d6eaf8; margin-bottom:6px; flex-wrap:wrap; }
        .script-step .step-num { font-weight:700; font-size:0.75rem; color:#8a9eb0; min-width:30px; }
        .script-step select, .script-step input { padding:4px 8px; border-radius:6px; border:1px solid #dce4ec; font-size:0.8rem; background:#fff; flex:1 1 140px; min-width:100px; }
        .script-step .custom-input { flex:2 1 180px; }
        .script-step .btn-remove-step { background:transparent; border:none; color:#c0392b; cursor:pointer; font-size:0.8rem; padding:2px 6px; }
        .script-preview { background:#f8fbff; border-radius:10px; padding:12px 16px; border:1px solid #d6eaf8; margin-top:10px; white-space:pre-wrap; font-family:'Consolas',monospace; font-size:0.85rem; line-height:1.8; max-height:300px; overflow-y:auto; }

        .eval-item { display:flex; align-items:center; gap:12px; padding:8px 14px; background:#f8fbff; border-radius:10px; border:1px solid #d6eaf8; flex-wrap:wrap; }
        .eval-item .e-label { font-weight:600; font-size:0.82rem; color:var(--cobalt-blue); min-width:100px; }
        .eval-item .e-desc { font-size:0.75rem; color:var(--text-muted); flex:1; min-width:80px; }
        .eval-item .e-score-input select { padding:3px 8px; border-radius:6px; border:1px solid #dce4ec; font-size:0.8rem; background:#fff; font-weight:600; width:70px; }
        .score-summary { display:grid; grid-template-columns:repeat(auto-fit,minmax(160px,1fr)); gap:14px; margin-bottom:16px; }
        .score-box { background:#f8fbff; border-radius:12px; padding:14px 16px; text-align:center; border:1px solid #d6eaf8; border-top: 3px solid var(--gold-accent); }
        .score-box .label { font-size:0.72rem; color:var(--text-muted); }
        .score-box .value { font-size:1.8rem; font-weight:700; color:var(--cobalt-blue); }
        .score-box .value.gold { color:var(--mid-blue); }
        .score-box .value.green { color:#2d7d5a; }
        .score-box .weight { font-size:0.65rem; color:#8a9eb0; }
        .score-detail table { width:100%; border-collapse:collapse; font-size:0.82rem; }
        .score-detail th { background:#f0f8fd; padding:6px 10px; text-align:left; font-weight:700; color:var(--cobalt-blue); border-bottom:2px solid #d6eaf8; }
        .score-detail td { padding:5px 10px; border-bottom:1px solid #d6eaf8; }

        .toast { position:fixed; bottom:24px; right:24px; background:var(--cobalt-blue); color:#fff; padding:8px 20px; border-radius:12px; box-shadow:0 8px 24px rgba(0,0,0,0.2); font-weight:600; transform:translateY(100px); opacity:0; transition:all 0.4s ease; z-index:999; max-width:380px; font-size:0.8rem; }
        .toast.show { transform:translateY(0); opacity:1; }
        .toast.success { background:#2d7d5a; }
        .toast.error { background:#c0392b; }
        .toast.info { background:var(--mid-blue); }
        .footer { text-align:center; padding:14px 0 4px; color:#8a9eb0; font-size:0.65rem; border-top:1px solid #d6eaf8; margin-top:4px; }
        .footer i { color:var(--mid-blue); }

        @media print {
            body { padding-top:0; background:#fff; }
            .navbar { display:none !important; }
            .page { display:block !important; animation:none !important; }
            .card { box-shadow:none !important; border:1px solid #ddd; }
            .btn { display:none !important; }
            .btn-sentence { display:none !important; }
            .dialogue-grid { grid-template-columns:repeat(2,1fr); }
            .vocab-grid { grid-template-columns:repeat(2,1fr); }
        }
        @media (max-width:820px) {
            .navbar { padding:0 10px; height:56px; }
            .navbar .brand { font-size:0.7rem; }
            .navbar .brand span { display:none; }
            .navbar .nav-links a { font-size:0.55rem; padding:3px 8px; }
            body { padding-top:60px; }
            .dialogue-grid { grid-template-columns:1fr; }
            .vocab-grid { grid-template-columns:repeat(auto-fill,minmax(180px,1fr)); }
        }
        @media (max-width:480px) {
            .vocab-grid { grid-template-columns:1fr; }
            .dialogue-grid { grid-template-columns:1fr; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="brand">
            <i class="fas fa-train"></i>
            百工专列 <span>· 景德镇站英语实训</span>
        </div>
        <div class="nav-links">
            <a class="active" data-page="page-info"><i class="fas fa-info-circle"></i> 小组</a>
            <a data-page="page-case"><i class="fas fa-clipboard-list"></i> 案例信息</a>
            <a data-page="page-vocab"><i class="fas fa-book-open"></i> 词汇</a>
            <a data-page="page-phrases"><i class="fas fa-comment-dots"></i> 句型</a>
            <a data-page="page-dialogue"><i class="fas fa-comments"></i> 对话卡片</a>
            <a data-page="page-performance"><i class="fas fa-user-tag"></i> 模拟展演</a>
            <a data-page="page-eval"><i class="fas fa-chalkboard-teacher"></i> 师评成绩</a>
        </div>
        <div class="right-actions">
            <button class="print-btn" onclick="window.print()"><i class="fas fa-print"></i> <span>打印</span></button>
        </div>
    </nav>

    <div class="container">

        <div class="page active" id="page-info">
            <div class="card">
                <div class="card-title"><i class="fas fa-info-circle"></i> 小组基本信息</div>
                <div class="form-row">
                    <div class="form-group"><label><i class="fas fa-school"></i> 班级</label><input type="text" id="className" placeholder="请输入班级" /></div>
                    <div class="form-group"><label><i class="fas fa-tag"></i> 小组名称</label><input type="text" id="groupName" placeholder="如：第1组 / 青花瓷乘务组" /></div>
                    <div class="form-group"><label><i class="fas fa-hashtag"></i> 小组编号</label><input type="text" id="groupId" placeholder="如：G01" /></div>
                    <div class="form-group"><label><i class="fas fa-tasks"></i> 实训任务</label><input type="text" id="taskName" value="百工专列·景德镇站 高铁乘务英语实训" /></div>
                    <div class="form-group"><label><i class="fas fa-user-tie"></i> 指导教师</label><input type="text" id="teacherName" placeholder="请输入姓名" /></div>
                </div>
                <div style="margin-top:10px;">
                    <button class="btn btn-success" id="saveInfoBtn"><i class="fas fa-save"></i> 保存信息</button>
                    <span class="text-muted" style="margin-left:10px;">数据自动保存在浏览器</span>
                </div>
            </div>
            <div class="card">
                <div class="card-title"><i class="fas fa-clipboard-list"></i> 任务说明</div>
                <p style="color:var(--text-muted);font-size:0.92rem;">
                    本实训系统基于 <strong>“百工专列”南昌西→景德镇北 高铁乘务服务</strong> 真实案例设计。
                    围绕 <strong>登车迎客、车厢广播、主题特产销售、车厢主题互动</strong> 四大情境，
                    通过 <strong>词汇跟读评分</strong>、<strong>句型逐词学习</strong>、<strong>对话卡片演练</strong>、<strong>模拟展演编排</strong> 四个环节，
                    掌握 <strong>40个景德镇主题列车与青花瓷工艺核心词汇、4类情境句型、4个完整对话</strong>，感悟中国工匠精神。
                </p>
                <div style="background:#f0f8fd;border-radius:10px;padding:12px 16px;border-left:4px solid var(--mid-blue);margin-top:10px;">
                    <strong style="color:var(--cobalt-blue);">💡 特色功能：</strong>
                    <span style="color:var(--text-muted);font-size:0.88rem;">① 每个单词可<strong>单独点击发音</strong>；② 每个句子提供<strong>“整句朗读”按钮</strong>；③ 支持跟读评分与对话录音；④ 词汇聚焦<strong>青花瓷制瓷工艺</strong>（拉坯、绘瓷、施釉、烧窑），体现<strong>工匠精神</strong>。</span>
                </div>
            </div>
        </div>

        <div class="page" id="page-case">
            <div class="card">
                <div class="card-title"><i class="fas fa-clipboard-list"></i> 百工专列·景德镇站 乘务服务案例 <span class="sub">案例详情</span></div>

                <div class="case-banner">
                    <div class="case-banner-text">
                        <i class="fas fa-train" style="font-size:2.5rem; margin-bottom:8px; color:#7dd3fc;"></i>
                        <h2>百工专列 · 景德镇站</h2>
                        <p>Craftsmen-Themed Train · Jingdezhen</p>
                        <span>车厢广播 · 景德镇与青花瓷文化</span>
                    </div>
                </div>

                <p class="section-desc">以下为本次高铁乘务英语实训所使用的完整案例信息。</p>
                <div style="background:#f0f8fd;border-radius:10px;padding:14px 16px;border-left:4px solid var(--mid-blue);margin-bottom:14px;">
                    <p style="color:var(--cobalt-blue);font-size:0.92rem;line-height:1.8;">
                        <strong>🚄 车次：</strong> G488 “百工专列” 南昌西（NCX）→ 景德镇北（JDZ）<br>
                        <strong>📅 日期：</strong> 2025年4月18日 &nbsp;|&nbsp; <strong>车型：</strong> 复兴号 CR400AF<br>
                        <strong>⏰ 阶段：</strong> 全程乘务服务（登车迎客 → 车厢广播 → 特产销售 → 主题互动 → 到站送别）
                    </p>
                </div>

                <div style="background:#fcf9f0;border-radius:10px;padding:12px 16px;border-left:4px solid var(--gold-accent);margin-bottom:14px;">
                    <p style="color:var(--cobalt-blue);font-size:0.9rem;line-height:1.8;">
                        <strong>📋 案例描述：</strong><br>
                        在一趟由南昌西开往景德镇的“百工专列”高铁上，4人乘务组为旅客提供全程服务。服务内容包括：<strong>登车迎客</strong>（站台迎客、检票验票、座位指引、行李协助），<strong>车厢广播</strong>（欢迎词、安全提示、到站提醒、换乘引导，<strong>重点介绍景德镇与青花瓷文化</strong>），<strong>主题特产销售</strong>（景德镇青花瓷茶具、花瓶、手工艺品、礼盒、扫码支付与折扣），<strong>车厢主题互动</strong>（瓷都文化讲解、青花瓷制瓷工艺展示、陶瓷知识问答、奖品赠送）。乘务员需用英语专业、礼貌、热情地与旅客沟通，在服务中传递<strong>中国工匠精神</strong>与<strong>青花瓷文化</strong>，让旅客在旅途中感受“瓷都”魅力。
                    </p>
                </div>

                <div class="case-card">
                    <div class="info-item"><div class="label">情景一 / Scenario 1</div><div class="value en">Boarding &amp; Welcome</div><div class="value zh">登车迎客 · 检票 · 座位指引</div></div>
                    <div class="info-item"><div class="label">情景二 / Scenario 2</div><div class="value en">Onboard Announcements</div><div class="value zh">车厢广播 · 景德镇与青花瓷文化</div></div>
                    <div class="info-item"><div class="label">情景三 / Scenario 3</div><div class="value en">Specialty Product Sales</div><div class="value zh">主题特产销售 · 瓷器 · 扫码支付</div></div>
                    <div class="info-item"><div class="label">情景四 / Scenario 4</div><div class="value en">Onboard Theme Interaction</div><div class="value zh">主题互动 · 青花瓷工艺 · 知识问答</div></div>
                </div>
                <div style="margin-top:14px;background:#fcf9f0;border-radius:10px;padding:10px 16px;border-left:4px solid var(--gold-accent);">
                    <strong style="color:var(--cobalt-blue);">📌 案例要点：</strong>
                    <span style="color:var(--text-muted);font-size:0.9rem;">4人乘务组分工协作，覆盖四大核心情境。乘务员需用英语向旅客提供专业、礼貌、灵活的服务，并具备景德镇陶瓷文化讲解能力，重点呈现<strong>青花瓷制作工艺</strong>（拉坯、修坯、绘瓷、施釉、烧窑）与<strong>工匠精神</strong>。</span>
                </div>
            </div>
        </div>

        <div class="page" id="page-vocab">
            <div class="card">
                <div class="card-title"><i class="fas fa-book-open"></i> 景德镇主题列车 &amp; 青花瓷工艺词汇 <span class="sub">点击单词听发音 · 点击🎤跟读评分</span></div>
                <p class="section-desc">共 <strong>40个</strong> 核心词汇，涵盖 <strong>主题列车服务、青花瓷制瓷工艺、瓷都文化与工匠精神</strong>，<strong>点击单词即可听发音</strong>，点击麦克风跟读评分。</p>
                <div class="vocab-grid" id="vocabGrid"></div>
                <div style="margin-top:12px;display:flex;gap:10px;flex-wrap:wrap;align-items:center;">
                    <button class="btn btn-outline btn-sm" id="resetVocabScoresBtn"><i class="fas fa-redo-alt"></i> 重置所有评分</button>
                    <span class="text-muted" id="vocabProgress">已学 0/40 个词汇</span>
                </div>
            </div>
        </div>

        <div class="page" id="page-phrases">
            <div class="card">
                <div class="card-title"><i class="fas fa-comment-dots"></i> 高铁乘务常用句型 <span class="sub">4类情境 · 点击单词听单词 · 点击按钮听整句</span></div>
                <p class="section-desc">
                    <strong>①</strong> 点击句中任意单词 → 听该单词发音；
                    <strong>②</strong> 点击 <i class="fas fa-volume-up text-gold"></i> <strong>整句朗读</strong>按钮 → 听整句标准发音。
                </p>
                <div id="phraseContainer"></div>
            </div>
        </div>

        <div class="page" id="page-dialogue">
            <div class="card">
                <div class="card-title"><i class="fas fa-comments"></i> 高铁乘务服务对话卡片 <span class="sub">4个情境 · 点击单词听单词 · 点击按钮听整句</span></div>
                <p class="section-desc">
                    <strong>点击台词中任意单词</strong>可听该单词发音；<strong>点击台词下方的“整句朗读”按钮</strong>可听整句发音。
                </p>
                <div class="dialogue-grid" id="dialogueGrid"></div>
                <div style="margin-top:12px;display:flex;gap:10px;flex-wrap:wrap;align-items:center;">
                    <button class="btn btn-outline btn-sm" id="clearDialogueRecordingsBtn"><i class="fas fa-trash-alt"></i> 清除所有录音</button>
                    <span class="text-muted" id="dialogueProgress">已录音 0/4 个对话</span>
                </div>
            </div>
        </div>

        <div class="page" id="page-performance">
            <div class="card">
                <div class="card-title"><i class="fas fa-user-tag"></i> 1. 角色分工（4人一组）</div>
                <p class="section-desc">4人乘务组，为每个岗位分配成员姓名。</p>
                <div class="role-grid" id="roleGrid"></div>
                <div style="margin-top:12px;">
                    <button class="btn btn-success" id="saveRolesBtn"><i class="fas fa-save"></i> 保存角色分配</button>
                </div>
            </div>
            <div class="card">
                <div class="card-title"><i class="fas fa-pen-fancy"></i> 2. 对话文本编写</div>
                <p class="section-desc">按四大情境顺序，为每个步骤选择角色和对应台词。</p>
                <div id="scriptEditor">
                    <div id="scriptStepsContainer"></div>
                    <div style="margin-top:8px;display:flex;gap:8px;flex-wrap:wrap;">
                        <button class="btn btn-primary btn-sm" id="addStepBtn"><i class="fas fa-plus"></i> 添加步骤</button>
                        <button class="btn btn-outline btn-sm" id="resetScriptBtn"><i class="fas fa-redo-alt"></i> 重置为默认流程</button>
                        <span class="text-muted" style="font-size:0.7rem;">共 <span id="stepCount">0</span> 个步骤</span>
                    </div>
                </div>
                <div style="margin-top:14px;">
                    <button class="btn btn-success" id="previewScriptBtn"><i class="fas fa-eye"></i> 预览对话</button>
                    <button class="btn btn-primary" id="downloadScriptBtn"><i class="fas fa-download"></i> 下载对话文本</button>
                </div>
                <div id="scriptPreviewContainer" style="margin-top:12px;display:none;">
                    <div class="card" style="background:#f0f8fd;border:1px solid #d6eaf8;border-radius:10px;padding:12px 16px;">
                        <div class="card-title" style="font-size:0.95rem;margin-bottom:6px;"><i class="fas fa-file-alt text-gold"></i> 对话预览</div>
                        <div class="script-preview" id="scriptPreviewText"></div>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="card-title"><i class="fas fa-clipboard-check"></i> 3. 模拟展演评分（教师用）</div>
                <div id="roleplayEvalContainer"></div>
                <div style="margin-top:10px;">
                    <button class="btn btn-success" id="saveRoleplayEvalBtn"><i class="fas fa-save"></i> 保存评分</button>
                </div>
            </div>
        </div>

        <div class="page" id="page-eval">
            <div class="card">
                <div class="card-title"><i class="fas fa-chalkboard-teacher"></i> 教师综合评价</div>
                <div id="teacherEvalContainer"></div>
                <div style="margin-top:10px;">
                    <button class="btn btn-success" id="saveTeacherEvalBtn"><i class="fas fa-save"></i> 保存师评</button>
                </div>
            </div>
            <div class="card">
                <div class="card-title"><i class="fas fa-chart-bar"></i> 成绩总览</div>
                <p class="text-muted" style="margin-bottom:10px;">最终成绩 = 词汇掌握 × 20% + 对话理解 × 30% + 模拟展演 × 50%</p>
                <div id="scoreSummary"></div>
                <div id="scoreDetail" class="score-detail"></div>
            </div>
        </div>

        <div class="footer">
            <i class="fas fa-train"></i> 百工专列英语 · 景德镇站 &nbsp;|&nbsp; 高铁乘务英语实训系统 &nbsp;|&nbsp; 数据本地存储
            <br><span style="font-size:0.6rem;">“微笑服务，专业沟通，讲好瓷都故事” —— 以专业态度，学好高铁乘务英语</span>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <script>
        const STORAGE_KEY = 'hsr_jdz_baigong_v6';

        // ===== 40个核心词汇（主题列车 + 青花瓷工艺 + 工匠精神） =====
        const VOCAB_DATA = [
            // ===== 主题列车乘务服务（10词） =====
            { word: 'themed train', phonetic: '/θiːmd treɪn/', meaning: 'n. 主题列车' },
            { word: 'craftsmen-themed train', phonetic: '/ˈkræftsmən θiːmd treɪn/', meaning: 'n. 工匠主题专列' },
            { word: 'steward', phonetic: '/ˈstuːərd/', meaning: 'n. 乘务员' },
            { word: 'carriage', phonetic: '/ˈkærɪdʒ/', meaning: 'n. 车厢' },
            { word: 'platform', phonetic: '/ˈplætfɔːrm/', meaning: 'n. 站台' },
            { word: 'boarding', phonetic: '/ˈbɔːrdɪŋ/', meaning: 'n. 登车' },
            { word: 'announcement', phonetic: '/əˈnaʊnsmənt/', meaning: 'n. 广播通知' },
            { word: 'souvenir', phonetic: '/ˌsuːvəˈnɪr/', meaning: 'n. 纪念品' },
            { word: 'passenger', phonetic: '/ˈpæsɪndʒər/', meaning: 'n. 旅客' },
            { word: 'onboard service', phonetic: '/ˌɑːnbɔːrd ˈsɜːrvɪs/', meaning: 'n. 车厢服务' },

            // ===== 青花瓷制瓷工艺——拉坯塑形（8词） =====
            { word: 'porcelain', phonetic: '/ˈpɔːrsəlɪn/', meaning: 'n. 瓷器' },
            { word: 'blue-and-white porcelain', phonetic: '/bluː ənd waɪt ˈpɔːrsəlɪn/', meaning: 'n. 青花瓷' },
            { word: 'kaolin', phonetic: '/ˈkeɪəlɪn/', meaning: 'n. 高岭土' },
            { word: 'clay', phonetic: '/kleɪ/', meaning: 'n. 陶土' },
            { word: 'wheel throwing', phonetic: '/wiːl ˈθroʊɪŋ/', meaning: 'n. 拉坯' },
            { word: 'shaping', phonetic: '/ˈʃeɪpɪŋ/', meaning: 'n. 塑形' },
            { word: 'trimming', phonetic: '/ˈtrɪmɪŋ/', meaning: 'n. 修坯' },
            { word: 'drying', phonetic: '/ˈdraɪɪŋ/', meaning: 'n. 晾干' },

            // ===== 青花瓷制瓷工艺——绘瓷施釉（10词） =====
            { word: 'underglaze', phonetic: '/ˈʌndərɡleɪz/', meaning: 'n. 釉下彩' },
            { word: 'cobalt pigment', phonetic: '/ˈkoʊbɔːlt ˈpɪɡmənt/', meaning: 'n. 钴蓝颜料' },
            { word: 'brushwork', phonetic: '/ˈbrʌʃwɜːrk/', meaning: 'n. 笔法' },
            { word: 'painting', phonetic: '/ˈpeɪntɪŋ/', meaning: 'n. 绘画' },
            { word: 'motif', phonetic: '/moʊˈtiːf/', meaning: 'n. 纹样' },
            { word: 'dragon pattern', phonetic: '/ˈdræɡən ˈpætərn/', meaning: 'n. 龙纹' },
            { word: 'glazing', phonetic: '/ˈɡleɪzɪŋ/', meaning: 'n. 施釉' },
            { word: 'glaze', phonetic: '/ɡleɪz/', meaning: 'n. 釉' },
            { word: 'kiln', phonetic: '/kɪln/', meaning: 'n. 窑' },
            { word: 'firing', phonetic: '/ˈfaɪərɪŋ/', meaning: 'n. 烧制' },

            // ===== 瓷都文化与工匠精神（12词） =====
            { word: 'Jingdezhen', phonetic: '/ˈdʒɪŋdə dʒən/', meaning: 'n. 景德镇' },
            { word: 'Porcelain Capital', phonetic: '/ˈpɔːrsəlɪn ˈkæpɪtl/', meaning: 'n. 瓷都' },
            { word: 'imperial kiln', phonetic: '/ɪmˈpɪriəl kɪln/', meaning: 'n. 御窑' },
            { word: 'ancient kiln', phonetic: '/ˈeɪnʃənt kɪln/', meaning: 'n. 古窑' },
            { word: 'craftsman', phonetic: '/ˈkræftsmən/', meaning: 'n. 工匠' },
            { word: 'craftsmanship', phonetic: '/ˈkræftsmənʃɪp/', meaning: 'n. 工匠精神' },
            { word: 'handcrafted', phonetic: '/ˌhændˈkræftɪd/', meaning: 'adj. 手工制作的' },
            { word: 'heritage', phonetic: '/ˈherɪtɪdʒ/', meaning: 'n. 遗产' },
            { word: 'tradition', phonetic: '/trəˈdɪʃn/', meaning: 'n. 传统' },
            { word: 'masterpiece', phonetic: '/ˈmæstərpiːs/', meaning: 'n. 杰作' },
            { word: 'artisan', phonetic: '/ˈɑːrtəzn/', meaning: 'n. 手艺人' },
            { word: 'cultural legacy', phonetic: '/ˈkʌltʃərəl ˈleɡəsi/', meaning: 'n. 文化遗产' }
        ];

        // ===== 核心句型（4类情境 × 8句） =====
        const PHRASE_DATA = [
            // 情境一：登车迎客
            { en: 'Good morning, welcome aboard the Craftsmen-Themed Train.', zh: '早上好，欢迎乘坐百工专列。', tag: '登车迎客' },
            { en: 'May I see your ticket and ID card, please?', zh: '请出示您的车票和身份证好吗？', tag: '登车迎客' },
            { en: 'Your seat is 12A in Car 5. Please go this way.', zh: '您的座位是5号车厢12A，请这边走。', tag: '登车迎客' },
            { en: 'Let me help you with your carry-on.', zh: '我来帮您拿随身行李。', tag: '登车迎客' },
            { en: 'Please place your suitcase on the overhead rack.', zh: '请把行李箱放在头顶行李架上。', tag: '登车迎客' },
            { en: 'Mind your step and hold the handrail, please.', zh: '请小心台阶，扶好扶手。', tag: '登车迎客' },
            { en: 'This is a themed train decorated with blue-and-white porcelain patterns.', zh: '这是一列以青花瓷纹样装饰的主题列车。', tag: '登车迎客' },
            { en: 'If you need anything, please let me know.', zh: '如果您需要什么，请告诉我。', tag: '登车迎客' },
            // 情境二：车厢广播（景德镇与青花瓷文化介绍）
            { en: 'Ladies and gentlemen, welcome aboard the Craftsmen-Themed Train, bound for Jingdezhen, the Porcelain Capital of China.', zh: '女士们、先生们，欢迎乘坐百工专列，本次列车开往中国瓷都景德镇。', tag: '车厢广播' },
            { en: 'Jingdezhen has a history of more than 1,700 years of porcelain making.', zh: '景德镇拥有超过1700年的制瓷历史。', tag: '车厢广播' },
            { en: 'Jingdezhen porcelain is famous for being as white as jade, as thin as paper, as bright as a mirror, and as resonant as a bell.', zh: '景德镇瓷器以“白如玉、薄如纸、明如镜、声如磬”闻名于世。', tag: '车厢广播' },
            { en: 'Blue-and-white porcelain is the most famous type of porcelain in Jingdezhen, known for its cobalt-blue patterns.', zh: '青花瓷是景德镇最著名的瓷器品种，以其钴蓝色纹样著称。', tag: '车厢广播' },
            { en: 'The making of blue-and-white porcelain involves several steps: wheel throwing, trimming, painting, glazing, and high-temperature firing.', zh: '青花瓷的制作需经过拉坯、修坯、绘瓷、施釉和高温烧制等多道工序。', tag: '车厢广播' },
            { en: 'Craftsmen shape the kaolin clay with their hands and paint the motifs stroke by stroke.', zh: '工匠们用双手将高岭土塑造成器，一笔一画绘制出精美的纹样。', tag: '车厢广播' },
            { en: 'This handcrafted technique, passed down from generation to generation, reflects the spirit of Chinese artisans.', zh: '这种代代相传的手工技艺，体现了中国工匠精益求精的精神。', tag: '车厢广播' },
            { en: 'During today\'s journey, you will have the chance to learn about the craft of blue-and-white porcelain and feel the charm of porcelain culture.', zh: '在今天的旅途中，您将有机会近距离了解青花瓷的制作工艺，感受瓷都文化的魅力。', tag: '车厢广播' },
            // 情境三：主题特产销售
            { en: 'Would you like to see some local specialties from Jingdezhen?', zh: '您想看看景德镇的当地特产吗？', tag: '特产销售' },
            { en: 'This is a handmade blue-and-white porcelain tea set.', zh: '这是一套手工青花瓷茶具。', tag: '特产销售' },
            { en: 'It is handcrafted by a local craftsman with traditional skills.', zh: '它由当地工匠采用传统技艺手工制作。', tag: '特产销售' },
            { en: 'The price is 280 yuan, and we offer a 10% discount today.', zh: '价格是280元，今天我们有九折优惠。', tag: '特产销售' },
            { en: 'You can scan the QR code to pay.', zh: '您可以扫码支付。', tag: '特产销售' },
            { en: 'Would you like a gift box? It\'s complimentary.', zh: '您需要礼盒吗？是免费赠送的。', tag: '特产销售' },
            { en: 'Here is your receipt. Please keep it well.', zh: '这是您的收据，请收好。', tag: '特产销售' },
            { en: 'This vase is a perfect souvenir for your family.', zh: '这个花瓶是带给家人的绝佳纪念品。', tag: '特产销售' },
            // 情境四：车厢主题互动
            { en: 'Welcome to our porcelain culture corner.', zh: '欢迎来到我们的陶瓷文化角。', tag: '主题互动' },
            { en: 'Would you like to join our quiz about Jingdezhen porcelain?', zh: '您想参加我们的景德镇陶瓷知识问答吗？', tag: '主题互动' },
            { en: 'Jingdezhen is known as the Porcelain Capital of China.', zh: '景德镇被誉为中国瓷都。', tag: '主题互动' },
            { en: 'The craftsman shapes the clay by wheel throwing.', zh: '工匠通过拉坯为陶土塑形。', tag: '主题互动' },
            { en: 'Then the artisan paints the motif with cobalt pigment.', zh: '然后手艺人用钴蓝颜料绘制纹样。', tag: '主题互动' },
            { en: 'After glazing, the piece is fired in the kiln at high temperature.', zh: '施釉之后，瓷器在窑中高温烧制。', tag: '主题互动' },
            { en: 'This craftsmanship reflects the spirit of Chinese artisans.', zh: '这种工艺体现了中国工匠的精神。', tag: '主题互动' },
            { en: 'Thank you for participating. We hope you had a memorable time.', zh: '感谢您的参与，希望您度过了难忘的时光。', tag: '主题互动' }
        ];

        // ===== 4个完整对话 =====
        const DIALOGUE_DATA = [{
            id: 1,
            title: '登车迎客',
            scene: '站台迎客，检票验票并引导旅客入座，介绍主题列车特色。',
            lines: [
                { speaker: 'Crew', text: 'Good morning, welcome aboard the Craftsmen-Themed Train.', trans: '早上好，欢迎乘坐百工专列。' },
                { speaker: 'Passenger', text: 'Thank you. Here is my ticket.', trans: '谢谢，这是我的车票。' },
                { speaker: 'Crew', text: 'May I see your ticket and ID card, please? Your seat is 12A in Car 5. Please go this way.', trans: '请出示您的车票和身份证好吗？您的座位是5号车厢12A，请这边走。' },
                { speaker: 'Passenger', text: 'Great. This train looks beautiful.', trans: '好的。这列车真漂亮。' },
                { speaker: 'Crew', text: 'Yes, it is a themed train decorated with blue-and-white porcelain patterns.', trans: '是的，这是一列以青花瓷纹样装饰的主题列车。' },
                { speaker: 'Passenger', text: 'Could you help me with my carry-on?', trans: '能帮我拿一下随身行李吗？' },
                { speaker: 'Crew', text: 'Of course. Please place it on the overhead rack. Mind your step and hold the handrail, please.', trans: '当然可以。请把它放在头顶行李架上。请小心台阶，扶好扶手。' },
                { speaker: 'Passenger', text: 'I will. Thank you.', trans: '我会的。谢谢。' },
                { speaker: 'Crew', text: 'If you need anything, please let me know. Enjoy your journey.', trans: '如果您需要什么，请告诉我。祝您旅途愉快。' }
            ]
        }, {
            id: 2,
            title: '车厢广播：景德镇与青花瓷文化',
            scene: '列车发车后，列车员通过车厢广播介绍景德镇与青花瓷文化，旅客聆听并互动。',
            lines: [
                { speaker: 'Crew', text: 'Ladies and gentlemen, welcome aboard the Craftsmen-Themed Train, bound for Jingdezhen, the Porcelain Capital of China.', trans: '女士们、先生们，欢迎乘坐百工专列，本次列车开往中国瓷都景德镇。' },
                { speaker: 'Crew', text: 'Jingdezhen has a history of more than 1,700 years of porcelain making.', trans: '景德镇拥有超过1700年的制瓷历史。' },
                { speaker: 'Passenger', text: 'Wow, that\'s amazing! I can\'t wait to learn more.', trans: '哇，太了不起了！我迫不及待想了解更多。' },
                { speaker: 'Crew', text: 'Jingdezhen porcelain is famous for being as white as jade, as thin as paper, as bright as a mirror, and as resonant as a bell.', trans: '景德镇瓷器以“白如玉、薄如纸、明如镜、声如磬”闻名于世。' },
                { speaker: 'Passenger', text: 'That\'s incredible. What about blue-and-white porcelain?', trans: '太不可思议了。那青花瓷呢？' },
                { speaker: 'Crew', text: 'Blue-and-white porcelain is the most famous type of porcelain in Jingdezhen, known for its cobalt-blue patterns.', trans: '青花瓷是景德镇最著名的瓷器品种，以其钴蓝色纹样著称。' },
                { speaker: 'Crew', text: 'The making of blue-and-white porcelain involves several steps: wheel throwing, trimming, painting, glazing, and high-temperature firing.', trans: '青花瓷的制作需经过拉坯、修坯、绘瓷、施釉和高温烧制等多道工序。' },
                { speaker: 'Passenger', text: 'That sounds very complicated. It must take a lot of work.', trans: '听起来非常复杂。肯定要花很多功夫吧。' },
                { speaker: 'Crew', text: 'Indeed. Craftsmen shape the kaolin clay with their hands and paint the motifs stroke by stroke.', trans: '的确。工匠们用双手将高岭土塑造成器，一笔一画绘制出精美的纹样。' },
                { speaker: 'Crew', text: 'This handcrafted technique, passed down from generation to generation, reflects the spirit of Chinese artisans.', trans: '这种代代相传的手工技艺，体现了中国工匠精益求精的精神。' },
                { speaker: 'Passenger', text: 'That\'s truly admirable. I\'m looking forward to seeing it myself.', trans: '真令人敬佩。我期待亲眼看看。' },
                { speaker: 'Crew', text: 'During today\'s journey, you will have the chance to learn about the craft of blue-and-white porcelain and feel the charm of porcelain culture.', trans: '在今天的旅途中，您将有机会近距离了解青花瓷的制作工艺，感受瓷都文化的魅力。' }
            ]
        }, {
            id: 3,
            title: '主题特产销售',
            scene: '乘务员推车售卖景德镇特产，介绍青花瓷茶具、工匠制作、礼盒与扫码支付。',
            lines: [
                { speaker: 'Crew', text: 'Good afternoon, would you like to see some local specialties from Jingdezhen?', trans: '下午好，您想看看景德镇的当地特产吗？' },
                { speaker: 'Passenger', text: 'Sure. What do you have?', trans: '好的。你们有什么？' },
                { speaker: 'Crew', text: 'This is a handmade blue-and-white porcelain tea set. It is handcrafted by a local craftsman with traditional skills.', trans: '这是一套手工青花瓷茶具。它由当地工匠采用传统技艺手工制作。' },
                { speaker: 'Passenger', text: 'It\'s beautiful. How much is it?', trans: '很漂亮。多少钱？' },
                { speaker: 'Crew', text: 'The price is 280 yuan, and we offer a 10% discount today.', trans: '价格是280元，今天我们有九折优惠。' },
                { speaker: 'Passenger', text: 'That sounds good. I\'ll take it.', trans: '听起来不错，我要一套。' },
                { speaker: 'Crew', text: 'Would you like a gift box? It\'s complimentary.', trans: '您需要礼盒吗？是免费赠送的。' },
                { speaker: 'Passenger', text: 'Yes, please. Can I pay by phone?', trans: '好的，谢谢。可以用手机支付吗？' },
                { speaker: 'Crew', text: 'Sure. You can scan the QR code to pay. Here is your receipt.', trans: '可以，您可以扫码支付。这是您的收据。' },
                { speaker: 'Passenger', text: 'Thank you very much.', trans: '非常感谢。' },
                { speaker: 'Crew', text: 'This vase is also a perfect souvenir for your family. Hope you enjoy your trip.', trans: '这个花瓶也是带给家人的绝佳纪念品。祝您旅途愉快。' }
            ]
        }, {
            id: 4,
            title: '车厢主题互动',
            scene: '乘务员组织瓷都文化知识问答，讲解青花瓷制瓷工艺，展示工匠精神。',
            lines: [
                { speaker: 'Crew', text: 'Welcome to our porcelain culture corner. Would you like to join our quiz about Jingdezhen porcelain?', trans: '欢迎来到我们的陶瓷文化角。您想参加我们的景德镇陶瓷知识问答吗？' },
                { speaker: 'Passenger', text: 'I\'d love to. What\'s the quiz about?', trans: '我很乐意。问答是关于什么的？' },
                { speaker: 'Crew', text: 'It\'s about how blue-and-white porcelain is made. Jingdezhen is known as the Porcelain Capital of China.', trans: '是关于青花瓷如何制作的。景德镇被誉为中国瓷都。' },
                { speaker: 'Passenger', text: 'Interesting! What\'s the question?', trans: '有意思！问题是什么？' },
                { speaker: 'Crew', text: 'What is the first step of making porcelain?', trans: '制作瓷器的第一步是什么？' },
                { speaker: 'Passenger', text: 'Is it shaping the clay by wheel throwing?', trans: '是用拉坯的方式为陶土塑形吗？' },
                { speaker: 'Crew', text: 'Correct! The craftsman shapes the clay by wheel throwing. Then the artisan paints the motif with cobalt pigment. After glazing, the piece is fired in the kiln at high temperature.', trans: '答对了！工匠通过拉坯为陶土塑形。然后手艺人用钴蓝颜料绘制纹样。施釉之后，瓷器在窑中高温烧制。' },
                { speaker: 'Passenger', text: 'Wow, that\'s a lot of work. It\'s really a masterpiece.', trans: '哇，工作量真大。真是一件杰作。' },
                { speaker: 'Crew', text: 'Yes. This craftsmanship reflects the spirit of Chinese artisans. You\'ve won a small porcelain gift. Congratulations!', trans: '是的。这种工艺体现了中国工匠的精神。您赢得了一份小瓷器礼品。恭喜！' },
                { speaker: 'Passenger', text: 'Thank you so much!', trans: '太感谢了！' },
                { speaker: 'Crew', text: 'Thank you for participating. We hope you had a memorable time.', trans: '感谢您的参与，希望您度过了难忘的时光。' }
            ]
        }];

        // ===== 4人乘务组角色 =====
        const ROLE_DATA = [
            { id: 'r1', title: '列车长 / 乘务长 (Train Chief)', icon: 'fa-user-shield' },
            { id: 'r2', title: '乘务员1 (CA1 · 迎客)', icon: 'fa-user-tie' },
            { id: 'r3', title: '乘务员2 (CA2 · 销售)', icon: 'fa-user' },
            { id: 'r4', title: '列车员 (Attendant)', icon: 'fa-user' }
        ];

        const TEACHER_EVAL_ITEMS = [
            { id: 't1', label: '词汇掌握度', desc: '40个主题列车与青花瓷工艺词汇的认读与发音准确度', weight: 20 },
            { id: 't2', label: '对话理解与应答', desc: '4个对话卡片的理解、跟读与应答熟练度', weight: 30 },
            { id: 't3', label: '模拟展演表现', desc: '角色投入度、语言流畅度、服务礼仪与瓷都文化讲解', weight: 50 }
        ];

        const ROLEPLAY_DIMENSIONS = [
            { id: 'rp1', label: '语言流畅度', desc: '英语表达自然、连贯，无明显卡顿' },
            { id: 'rp2', label: '服务专业度', desc: '服务用语规范、得体、有礼貌，流程完整' },
            { id: 'rp3', label: '文化呈现与互动', desc: '青花瓷工艺讲解、工匠精神传递、互动组织能力' }
        ];

        function getDefaultData() {
            return {
                groupInfo: { className: '', groupName: '', groupId: '', taskName: '百工专列·景德镇站 高铁乘务英语实训', teacher: '' },
                vocabScores: {},
                roles: ROLE_DATA.map(r => ({ ...r, member: '' })),
                scriptSteps: [
                    { roleId: 'r2', phraseIdx: 0, customText: '' },
                    { roleId: 'r4', phraseIdx: 8, customText: '' },
                    { roleId: 'r3', phraseIdx: 16, customText: '' },
                    { roleId: 'r1', phraseIdx: 24, customText: '' }
                ],
                dialogueRecordings: {},
                roleplayEval: {},
                teacherEval: {},
                teacherComment: '',
                updatedAt: ''
            };
        }

        function loadData() {
            try {
                const raw = localStorage.getItem(STORAGE_KEY);
                if (raw) {
                    const parsed = JSON.parse(raw);
                    if (!parsed.groupInfo) parsed.groupInfo = getDefaultData().groupInfo;
                    if (!parsed.vocabScores) parsed.vocabScores = {};
                    if (!parsed.roles || parsed.roles.length !== 4) {
                        parsed.roles = ROLE_DATA.map(r => ({ ...r, member: '' }));
                    } else {
                        parsed.roles = parsed.roles.map((r, idx) => ({ ...ROLE_DATA[idx], member: r.member || '' }));
                    }
                    if (!parsed.scriptSteps || !Array.isArray(parsed.scriptSteps) || parsed.scriptSteps.length === 0) {
                        parsed.scriptSteps = getDefaultData().scriptSteps;
                    }
                    if (!parsed.dialogueRecordings) parsed.dialogueRecordings = {};
                    if (!parsed.roleplayEval) parsed.roleplayEval = {};
                    if (!parsed.teacherEval) parsed.teacherEval = {};
                    if (parsed.teacherComment === undefined) parsed.teacherComment = '';
                    return parsed;
                }
            } catch (e) { console.warn('加载数据失败', e); }
            return getDefaultData();
        }

        function saveData(data) {
            data.updatedAt = new Date().toLocaleString();
            localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
            return data;
        }

        let appData = loadData();

        function showToast(msg, type = 'success') {
            const el = document.getElementById('toast');
            el.textContent = msg;
            el.className = 'toast ' + type + ' show';
            clearTimeout(el._timer);
            el._timer = setTimeout(() => el.classList.remove('show'), 2800);
        }

        function speakText(text, lang = 'en-US', rate = 0.8, callback) {
            if (!window.speechSynthesis) { showToast('浏览器不支持语音合成', 'error'); return; }
            window.speechSynthesis.cancel();
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.lang = lang;
            utterance.rate = rate;
            utterance.pitch = 1.0;
            utterance.volume = 1;
            utterance.onend = () => {
                document.querySelectorAll('.speaking, .playing').forEach(el => el.classList.remove('speaking', 'playing'));
                if (callback) callback();
            };
            utterance.onerror = () => {
                document.querySelectorAll('.speaking, .playing').forEach(el => el.classList.remove('speaking', 'playing'));
                if (callback) callback();
            };
            window.speechSynthesis.speak(utterance);
        }

        function buildClickableWords(sentence) {
            const parts = sentence.split(/(\s+)/);
            let html = '';
            parts.forEach(part => {
                if (/^\s+$/.test(part)) {
                    html += ' ';
                } else if (part.trim() === '') {
                    // skip
                } else {
                    const cleanWord = part.replace(/[.,!?;:'"]/g, '').trim();
                    if (cleanWord) {
                        html += `<span class="word-chip" data-word="${cleanWord.replace(/"/g, '&quot;')}">${part}</span>`;
                    } else {
                        html += `<span>${part}</span>`;
                    }
                }
            });
            return html;
        }

        function bindWordClicks(container) {
            container.querySelectorAll('.word-chip').forEach(chip => {
                chip.addEventListener('click', function(e) {
                    e.stopPropagation();
                    const word = this.dataset.word;
                    if (!word) return;
                    document.querySelectorAll('.word-chip.speaking').forEach(el => el.classList.remove('speaking'));
                    this.classList.add('speaking');
                    speakText(word, 'en-US', 0.75, () => { this.classList.remove('speaking'); });
                });
            });
        }

        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const pageId = this.dataset.page;
                document.querySelectorAll('.nav-links a').forEach(l => l.classList.remove('active'));
                this.classList.add('active');
                document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
                document.getElementById(pageId).classList.add('active');
                if (pageId === 'page-info') loadInfoToForm();
                if (pageId === 'page-vocab') renderVocab();
                if (pageId === 'page-phrases') renderPhrases();
                if (pageId === 'page-dialogue') renderDialogues();
                if (pageId === 'page-performance') { renderRoles(); renderScriptEditor(); renderRoleplayEval(); }
                if (pageId === 'page-eval') { renderTeacherEval(); renderScore(); }
            });
        });

        function loadInfoToForm() {
            const info = appData.groupInfo;
            document.getElementById('className').value = info.className || '';
            document.getElementById('groupName').value = info.groupName || '';
            document.getElementById('groupId').value = info.groupId || '';
            document.getElementById('taskName').value = info.taskName || '百工专列·景德镇站 高铁乘务英语实训';
            document.getElementById('teacherName').value = info.teacher || '';
        }
        document.getElementById('saveInfoBtn').addEventListener('click', function() {
            appData.groupInfo.className = document.getElementById('className').value.trim();
            appData.groupInfo.groupName = document.getElementById('groupName').value.trim();
            appData.groupInfo.groupId = document.getElementById('groupId').value.trim();
            appData.groupInfo.taskName = document.getElementById('taskName').value.trim();
            appData.groupInfo.teacher = document.getElementById('teacherName').value.trim();
            saveData(appData);
            showToast('小组信息已保存');
        });

        let recognition = null;

        function initSpeechRecognition() {
            if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) return null;
            const SR = window.SpeechRecognition || window.webkitSpeechRecognition;
            const rec = new SR();
            rec.lang = 'en-US';
            rec.continuous = false;
            rec.interimResults = false;
            rec.maxAlternatives = 1;
            return rec;
        }

        function calculateScore(recognized, target) {
            recognized = recognized.toLowerCase().trim();
            target = target.toLowerCase().trim();
            if (!recognized || !target) return 0;
            if (recognized === target) return 100;
            if (recognized.includes(target)) return 92;
            if (target.includes(recognized)) return 88;
            const recWords = recognized.split(/\s+/);
            const tarWords = target.split(/\s+/);
            let matchCount = 0;
            tarWords.forEach(tw => { if (recWords.some(rw => rw === tw)) matchCount++; });
            if (tarWords.length > 0) {
                const ratio = matchCount / tarWords.length;
                if (ratio >= 0.8) return 85;
                if (ratio >= 0.6) return 70;
                if (ratio >= 0.4) return 55;
            }
            const dist = levenshteinDistance(recognized, target);
            const maxLen = Math.max(recognized.length, target.length);
            if (maxLen === 0) return 0;
            return Math.round((1 - dist / maxLen) * 60);
        }

        function levenshteinDistance(a, b) {
            const matrix = [];
            for (let i = 0; i <= b.length; i++) matrix[i] = [i];
            for (let j = 0; j <= a.length; j++) matrix[0][j] = j;
            for (let i = 1; i <= b.length; i++) {
                for (let j = 1; j <= a.length; j++) {
                    if (b[i - 1] === a[j - 1]) { matrix[i][j] = matrix[i - 1][j - 1]; } else {
                        matrix[i][j] = Math.min(matrix[i - 1][j - 1] + 1, matrix[i][j - 1] + 1, matrix[i - 1][j] + 1);
                    }
                }
            }
            return matrix[b.length][a.length];
        }

        function getScoreClass(score) {
            if (score >= 80) return 'score-excellent';
            if (score >= 60) return 'score-good';
            if (score >= 40) return 'score-fair';
            if (score > 0) return 'score-poor';
            return 'score-none';
        }

        function getScoreLabel(score) {
            if (score >= 80) return '🌟 优秀';
            if (score >= 60) return '👍 良好';
            if (score >= 40) return '📖 一般';
            if (score > 0) return '💪 需练习';
            return '⏳ 待跟读';
        }

        function renderVocab() {
            const grid = document.getElementById('vocabGrid');
            grid.innerHTML = '';
            VOCAB_DATA.forEach((item, idx) => {
                const scoreData = appData.vocabScores[item.word] || { score: 0, attempts: 0 };
                const div = document.createElement('div');
                div.className = 'vocab-card';
                div.innerHTML = `
                    <div class="word-row">
                        <span class="word" data-word="${item.word}">${item.word}</span>
                        <span class="phonetic">${item.phonetic}</span>
                    </div>
                    <div class="meaning">${item.meaning}</div>
                    <div class="actions">
                        <button class="speak-btn" data-word="${item.word}"><i class="fas fa-volume-up"></i></button>
                        <button class="record-btn" data-word="${item.word}" data-idx="${idx}"><i class="fas fa-microphone"></i></button>
                        <span class="recognition-status" id="status-${idx}">点击🎤开始跟读</span>
                    </div>
                    <div class="score-display">
                        评分：<span class="score-value ${getScoreClass(scoreData.score)}" id="score-${idx}">${scoreData.score > 0 ? scoreData.score : '—'}</span>
                        <span style="font-size:0.7rem;color:#8a9eb0;">${getScoreLabel(scoreData.score)}</span>
                    </div>`;
                grid.appendChild(div);
                div.querySelector('.word').addEventListener('click', function(e) {
                    e.stopPropagation();
                    const word = this.dataset.word;
                    document.querySelectorAll('.vocab-card .word.speaking').forEach(el => el.classList.remove('speaking'));
                    this.classList.add('speaking');
                    speakText(word, 'en-US', 0.7, () => { this.classList.remove('speaking'); });
                });
                div.querySelector('.speak-btn').addEventListener('click', function(e) {
                    e.stopPropagation();
                    speakText(this.dataset.word, 'en-US', 0.7);
                });
                const recordBtn = div.querySelector('.record-btn');
                const statusEl = document.getElementById(`status-${idx}`);
                const scoreEl = document.getElementById(`score-${idx}`);
                recordBtn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    const word = this.dataset.word;
                    if (this.classList.contains('recording')) {
                        if (recognition) { try { recognition.stop(); } catch (e) {} }
                        this.classList.remove('recording');
                        return;
                    }
                    if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) {
                        showToast('当前浏览器不支持语音识别', 'error'); return;
                    }
                    if (!recognition) { recognition = initSpeechRecognition(); if (!recognition) return; }
                    recognition.lang = 'en-US';
                    recognition.continuous = false;
                    recognition.interimResults = false;
                    recognition.onstart = function() {
                        recordBtn.classList.add('recording');
                        statusEl.textContent = '🎤 正在听...';
                        statusEl.className = 'recognition-status active';
                    };
                    recognition.onresult = function(event) {
                        const result = event.results[0];
                        const transcript = result[0].transcript.toLowerCase().trim();
                        const confidence = result[0].confidence || 0;
                        const score = calculateScore(transcript, word);
                        const finalScore = Math.min(100, Math.round(score * 0.85 + confidence * 15));
                        if (!appData.vocabScores[word]) appData.vocabScores[word] = { score: 0, attempts: 0 };
                        appData.vocabScores[word].score = Math.max(appData.vocabScores[word].score, finalScore);
                        appData.vocabScores[word].attempts += 1;
                        saveData(appData);
                        statusEl.textContent = `✅ ${finalScore}分`;
                        statusEl.className = 'recognition-status success';
                        scoreEl.textContent = finalScore;
                        scoreEl.className = `score-value ${getScoreClass(finalScore)}`;
                        recordBtn.classList.remove('recording');
                        updateVocabProgress();
                    };
                    recognition.onerror = function(event) {
                        recordBtn.classList.remove('recording');
                        statusEl.textContent = '❌ 错误';
                        statusEl.className = 'recognition-status error';
                    };
                    recognition.onend = function() { recordBtn.classList.remove('recording'); };
                    try { recognition.start(); } catch (e) { recordBtn.classList.remove('recording'); }
                });
            });
            updateVocabProgress();
        }

        function updateVocabProgress() {
            let learned = 0;
            VOCAB_DATA.forEach(item => {
                const data = appData.vocabScores[item.word];
                if (data && data.score > 0) learned++;
            });
            document.getElementById('vocabProgress').textContent = `已学 ${learned}/${VOCAB_DATA.length} 个词汇`;
        }

        document.getElementById('resetVocabScoresBtn').addEventListener('click', function() {
            if (!confirm('重置所有词汇评分数据？')) return;
            appData.vocabScores = {};
            saveData(appData);
            renderVocab();
            showToast('所有评分已重置');
        });

        function renderPhrases() {
            const container = document.getElementById('phraseContainer');
            container.innerHTML = '';
            const categoryMap = {
                '登车迎客': '🚄 情境一：登车迎客',
                '车厢广播': '📢 情境二：车厢广播 · 景德镇与青花瓷文化',
                '特产销售': '🏺 情境三：主题特产销售',
                '主题互动': '🎨 情境四：车厢主题互动'
            };
            const groups = {};
            PHRASE_DATA.forEach(p => {
                if (!groups[p.tag]) groups[p.tag] = [];
                groups[p.tag].push(p);
            });
            const order = ['登车迎客', '车厢广播', '特产销售', '主题互动'];
            order.forEach(tag => {
                if (!groups[tag]) return;
                const items = groups[tag];
                const section = document.createElement('div');
                section.className = 'phrase-section';
                let itemsHtml = '';
                items.forEach(item => {
                    itemsHtml += `
                        <div class="phrase-item">
                            <div class="en-line">${buildClickableWords(item.en)}</div>
                            <div class="zh-line">${item.zh}</div>
                            <div class="sentence-actions">
                                <button class="btn-sentence" data-sentence="${item.en.replace(/"/g, '&quot;')}"><i class="fas fa-volume-up"></i> 整句朗读</button>
                            </div>
                        </div>
                    `;
                });
                section.innerHTML = `
                    <div class="phrase-section-title">
                        <span>${categoryMap[tag] || tag}</span>
                        <span class="badge">${items.length} 句</span>
                    </div>
                    ${itemsHtml}
                `;
                container.appendChild(section);
                bindWordClicks(section);
                section.querySelectorAll('.btn-sentence').forEach(btn => {
                    btn.addEventListener('click', function(e) {
                        e.stopPropagation();
                        const sentence = this.dataset.sentence;
                        document.querySelectorAll('.btn-sentence.playing').forEach(b => b.classList.remove('playing'));
                        this.classList.add('playing');
                        speakText(sentence, 'en-US', 0.8, () => { this.classList.remove('playing'); });
                        showToast('🔊 正在朗读整句...', 'info');
                    });
                });
            });
        }

        function renderDialogues() {
            const grid = document.getElementById('dialogueGrid');
            grid.innerHTML = '';
            DIALOGUE_DATA.forEach(dial => {
                const rec = appData.dialogueRecordings[dial.id] || null;
                const card = document.createElement('div');
                card.className = 'dialogue-card';

                let linesHtml = '';
                dial.lines.forEach(line => {
                    const cls = line.speaker === 'Crew' ? 'crew' : 'passenger';
                    const speakerLabel = line.speaker === 'Crew' ? '👩‍✈️ 列车员' : '🧑 旅客';
                    linesHtml += `
                        <div class="d-line ${cls}">
                            <div class="d-speaker"><i class="fas fa-${line.speaker === 'Crew' ? 'user' : 'user'}"></i> ${speakerLabel}</div>
                            <div class="d-en-line">${buildClickableWords(line.text)}</div>
                            <div class="d-trans">${line.trans}</div>
                            <div class="d-actions">
                                <button class="btn-sentence" data-sentence="${line.text.replace(/"/g, '&quot;')}"><i class="fas fa-volume-up"></i> 整句朗读</button>
                            </div>
                        </div>
                    `;
                });

                const fullText = dial.lines.map(l => l.text).join(' ');

                card.innerHTML = `
                    <div class="d-header">
                        <span class="d-num">情境 ${dial.id}</span>
                        <span class="d-title">${dial.title}</span>
                        <span class="d-scene-label">${dial.scene}</span>
                    </div>
                    <div class="d-body">${linesHtml}</div>
                    <div class="d-audio-bar">
                        <button class="btn-audio-sm play-full" data-text="${fullText}" title="播放整段对话"><i class="fas fa-play"></i> 整段播放</button>
                        <button class="btn-recording-sm start-rec" data-id="${dial.id}"><i class="fas fa-circle" style="color:#c0392b;"></i> 录音</button>
                        <button class="btn-recording-sm stop-rec" data-id="${dial.id}" style="display:none;"><i class="fas fa-stop"></i> 停止</button>
                        <button class="btn-recording-sm play-rec" data-id="${dial.id}" ${!rec ? 'disabled' : ''}><i class="fas fa-play"></i> 播放</button>
                        <button class="btn-recording-sm delete-rec" data-id="${dial.id}" ${!rec ? 'disabled' : ''}><i class="fas fa-trash-alt"></i> 删除</button>
                        <span class="d-status" id="dial-status-${dial.id}">${rec ? '✅ 已录音 ' + (rec.duration || 0) + 's' : '⏳ 未录音'}</span>
                    </div>
                `;
                grid.appendChild(card);
                bindWordClicks(card);

                card.querySelectorAll('.btn-sentence').forEach(btn => {
                    btn.addEventListener('click', function(e) {
                        e.stopPropagation();
                        const sentence = this.dataset.sentence;
                        document.querySelectorAll('.btn-sentence.playing').forEach(b => b.classList.remove('playing'));
                        this.classList.add('playing');
                        speakText(sentence, 'en-US', 0.8, () => { this.classList.remove('playing'); });
                        showToast('🔊 正在朗读整句...', 'info');
                    });
                });

                card.querySelector('.play-full').addEventListener('click', function(e) {
                    e.stopPropagation();
                    this.classList.add('playing');
                    speakText(this.dataset.text, 'en-US', 0.78, () => { this.classList.remove('playing'); });
                    showToast(`🔊 播放完整对话`, 'info');
                });

                const startBtn = card.querySelector('.start-rec');
                const stopBtn = card.querySelector('.stop-rec');
                const playBtn = card.querySelector('.play-rec');
                const deleteBtn = card.querySelector('.delete-rec');
                const statusEl = document.getElementById(`dial-status-${dial.id}`);
                let mediaRecorder = null;
                let audioChunks = [];
                let recordingStartTime = 0;

                startBtn.addEventListener('click', async function(e) {
                    e.stopPropagation();
                    if (appData.dialogueRecordings[dial.id] && appData.dialogueRecordings[dial.id].audioData) {
                        if (!confirm('已有录音，重新录音将覆盖之前的内容？')) return;
                    }
                    try {
                        const stream = await navigator.mediaDevices.getUserMedia({ audio: true });
                        mediaRecorder = new MediaRecorder(stream, { mimeType: 'audio/webm' });
                        audioChunks = [];
                        mediaRecorder.ondataavailable = (event) => { if (event.data.size > 0) audioChunks.push(event.data); };
                        mediaRecorder.onstop = () => {
                            const blob = new Blob(audioChunks, { type: 'audio/webm' });
                            const reader = new FileReader();
                            reader.onload = () => {
                                const base64 = reader.result.split(',')[1];
                                const duration = Math.round((Date.now() - recordingStartTime) / 1000);
                                appData.dialogueRecordings[dial.id] = { audioData: base64, duration, timestamp: new Date().toISOString() };
                                saveData(appData);
                                statusEl.textContent = `✅ 已录音 ${duration}s`;
                                statusEl.className = 'd-status done';
                                playBtn.disabled = false;
                                deleteBtn.disabled = false;
                                updateDialogueProgress();
                            };
                            reader.readAsDataURL(blob);
                            stream.getTracks().forEach(track => track.stop());
                            startBtn.style.display = 'inline-flex';
                            stopBtn.style.display = 'none';
                        };
                        mediaRecorder.start();
                        recordingStartTime = Date.now();
                        startBtn.style.display = 'none';
                        stopBtn.style.display = 'inline-flex';
                        showToast('🎤 录音中...', 'info');
                    } catch (err) { showToast('无法访问麦克风', 'error'); }
                });

                stopBtn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    if (mediaRecorder && mediaRecorder.state === 'recording') mediaRecorder.stop();
                });

                playBtn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    const data = appData.dialogueRecordings[dial.id];
                    if (!data || !data.audioData) return;
                    new Audio(`data:audio/webm;base64,${data.audioData}`).play();
                });

                deleteBtn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    if (!confirm('确定删除此对话的录音吗？')) return;
                    delete appData.dialogueRecordings[dial.id];
                    saveData(appData);
                    statusEl.textContent = '⏳ 未录音';
                    statusEl.className = 'd-status';
                    playBtn.disabled = true;
                    deleteBtn.disabled = true;
                    updateDialogueProgress();
                });
            });
            updateDialogueProgress();
        }

        function updateDialogueProgress() {
            let count = 0;
            DIALOGUE_DATA.forEach(d => {
                if (appData.dialogueRecordings[d.id] && appData.dialogueRecordings[d.id].audioData) count++;
            });
            document.getElementById('dialogueProgress').textContent = `已录音 ${count}/${DIALOGUE_DATA.length} 个对话`;
        }

        document.getElementById('clearDialogueRecordingsBtn').addEventListener('click', function() {
            if (!confirm('确定清除所有对话的录音数据吗？')) return;
            appData.dialogueRecordings = {};
            saveData(appData);
            renderDialogues();
            showToast('所有录音已清除');
        });

        function renderRoles() {
            const grid = document.getElementById('roleGrid');
            grid.innerHTML = '';
            appData.roles.forEach((role, idx) => {
                const div = document.createElement('div');
                div.className = 'role-card';
                div.innerHTML = `
                    <div class="r-title"><span class="icon"><i class="fas ${role.icon}"></i></span> ${role.title}</div>
                    <div class="r-name"><input type="text" class="role-member-input" data-idx="${idx}" value="${role.member}" placeholder="姓名..." /></div>`;
                grid.appendChild(div);
                div.querySelector('.role-member-input').addEventListener('change', function() {
                    appData.roles[parseInt(this.dataset.idx)].member = this.value.trim();
                    saveData(appData);
                    renderScriptEditor();
                });
            });
        }

        document.getElementById('saveRolesBtn').addEventListener('click', function() {
            document.querySelectorAll('.role-member-input').forEach(inp => {
                appData.roles[parseInt(inp.dataset.idx)].member = inp.value.trim();
            });
            saveData(appData);
            renderScriptEditor();
            showToast('角色分配已保存');
        });

        function renderScriptEditor() {
            const container = document.getElementById('scriptStepsContainer');
            const steps = appData.scriptSteps || [];
            container.innerHTML = '';
            steps.forEach((step, idx) => {
                const div = document.createElement('div');
                div.className = 'script-step';
                const roleSelect = document.createElement('select');
                appData.roles.forEach(r => {
                    const opt = document.createElement('option');
                    opt.value = r.id;
                    opt.textContent = r.member ? `${r.title} (${r.member})` : r.title;
                    if (r.id === step.roleId) opt.selected = true;
                    roleSelect.appendChild(opt);
                });
                const phraseSelect = document.createElement('select');
                const defaultOpt = document.createElement('option');
                defaultOpt.value = '-1';
                defaultOpt.textContent = '✏️ 自定义';
                phraseSelect.appendChild(defaultOpt);
                PHRASE_DATA.forEach((p, pi) => {
                    const opt = document.createElement('option');
                    opt.value = pi;
                    opt.textContent = p.en.substring(0, 40) + '...';
                    if (pi === step.phraseIdx) opt.selected = true;
                    phraseSelect.appendChild(opt);
                });
                const customInput = document.createElement('input');
                customInput.type = 'text';
                customInput.placeholder = '自定义台词...';
                customInput.value = step.customText || '';
                const numSpan = document.createElement('span');
                numSpan.className = 'step-num';
                numSpan.textContent = `#${idx+1}`;
                const delBtn = document.createElement('button');
                delBtn.className = 'btn-remove-step';
                delBtn.innerHTML = '<i class="fas fa-trash-alt"></i>';
                delBtn.addEventListener('click', function() {
                    if (steps.length <= 1) return;
                    steps.splice(idx, 1);
                    saveData(appData);
                    renderScriptEditor();
                });
                div.appendChild(numSpan);
                div.appendChild(roleSelect);
                div.appendChild(phraseSelect);
                div.appendChild(customInput);
                div.appendChild(delBtn);
                container.appendChild(div);
                const saveStep = () => {
                    appData.scriptSteps[idx].roleId = roleSelect.value;
                    appData.scriptSteps[idx].phraseIdx = parseInt(phraseSelect.value);
                    appData.scriptSteps[idx].customText = customInput.value.trim();
                    saveData(appData);
                };
                roleSelect.addEventListener('change', saveStep);
                phraseSelect.addEventListener('change', saveStep);
                customInput.addEventListener('input', saveStep);
            });
            document.getElementById('stepCount').textContent = steps.length;
        }

        document.getElementById('addStepBtn').addEventListener('click', function() {
            appData.scriptSteps.push({ roleId: 'r2', phraseIdx: -1, customText: '' });
            saveData(appData);
            renderScriptEditor();
            showToast('已添加新步骤');
        });

        document.getElementById('resetScriptBtn').addEventListener('click', function() {
            if (!confirm('重置为默认对话流程？')) return;
            appData.scriptSteps = getDefaultData().scriptSteps;
            saveData(appData);
            renderScriptEditor();
        });

        function generatePreview() {
            const steps = appData.scriptSteps || [];
            const previewContainer = document.getElementById('scriptPreviewContainer');
            const previewText = document.getElementById('scriptPreviewText');
            if (steps.length === 0) { previewText.textContent = '暂无步骤。'; previewContainer.style.display = 'block'; return; }
            const groupInfo = appData.groupInfo;
            let lines = `百工专列·景德镇站 高铁乘务英语对话脚本\n小组：${groupInfo.groupName || '未命名'} (${groupInfo.groupId || ''})\n${'='.repeat(40)}\n\n`;
            steps.forEach((step) => {
                const role = appData.roles.find(r => r.id === step.roleId);
                const roleName = role ? `${role.title} (${role.member || '未分配'})` : '未知角色';
                let phrase = '';
                if (step.phraseIdx >= 0 && step.phraseIdx < PHRASE_DATA.length) phrase = PHRASE_DATA[step.phraseIdx].en;
                else phrase = step.customText || '（未填写）';
                lines += `【${roleName}】${phrase}\n`;
            });
            previewText.textContent = lines;
            previewContainer.style.display = 'block';
            return lines;
        }

        document.getElementById('previewScriptBtn').addEventListener('click', function() {
            generatePreview();
            showToast('对话预览已更新');
        });

        document.getElementById('downloadScriptBtn').addEventListener('click', function() {
            const fullText = generatePreview();
            if (!fullText) return;
            const blob = new Blob([fullText], { type: 'text/plain;charset=utf-8' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `百工专列英语对话_${appData.groupInfo.groupId || '小组'}.txt`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
            showToast('✅ 已下载');
        });

        function renderRoleplayEval() {
            const container = document.getElementById('roleplayEvalContainer');
            let html = '';
            ROLEPLAY_DIMENSIONS.forEach(item => {
                const score = appData.roleplayEval[item.id] || 0;
                html += `<div class="eval-item">
                    <span class="e-label">${item.label}</span>
                    <span class="e-desc">${item.desc}</span>
                    <div class="e-score-input">
                        <select class="roleplay-score" data-id="${item.id}">
                            ${[0,10,20,30,40,50,60,70,80,90,100].map(v => `<option value="${v}" ${score===v?'selected':''}>${v}</option>`).join('')}
                        </select><span>/ 100</span>
                    </div>
                </div>`;
            });
            const total = ROLEPLAY_DIMENSIONS.reduce((sum, item) => sum + (appData.roleplayEval[item.id] || 0), 0);
            const avg = Math.round(total / ROLEPLAY_DIMENSIONS.length);
            html += `<div style="margin-top:8px;padding:8px 14px;background:#f0f8fd;border-radius:8px;font-weight:700;color:var(--cobalt-blue);">模拟展演平均分：<span id="roleplayAvg">${avg}</span> / 100</div>`;
            container.innerHTML = html;
            container.querySelectorAll('.roleplay-score').forEach(sel => {
                sel.addEventListener('change', function() {
                    appData.roleplayEval[this.dataset.id] = parseInt(this.value);
                    saveData(appData);
                    const newAvg = Math.round(ROLEPLAY_DIMENSIONS.reduce((s, item) => s + (appData.roleplayEval[item.id] || 0), 0) / ROLEPLAY_DIMENSIONS.length);
                    document.getElementById('roleplayAvg').textContent = newAvg;
                    renderScore();
                });
            });
        }

        document.getElementById('saveRoleplayEvalBtn').addEventListener('click', function() {
            saveData(appData);
            showToast('模拟展演评分已保存');
            renderScore();
        });

        function renderTeacherEval() {
            const container = document.getElementById('teacherEvalContainer');
            let html = '';
            TEACHER_EVAL_ITEMS.forEach(item => {
                const score = appData.teacherEval[item.id] || 0;
                html += `<div class="eval-item">
                    <span class="e-label">${item.label}</span>
                    <span class="e-desc">${item.desc}（权重 ${item.weight}%）</span>
                    <div class="e-score-input">
                        <select class="teacher-score" data-id="${item.id}">
                            ${[0,10,20,30,40,50,60,70,80,90,100].map(v => `<option value="${v}" ${score===v?'selected':''}>${v}</option>`).join('')}
                        </select><span>/ 100</span>
                    </div>
                </div>`;
            });
            const weightedTotal = TEACHER_EVAL_ITEMS.reduce((sum, item) => sum + (appData.teacherEval[item.id] || 0) * (item.weight / 100), 0);
            html += `<div style="margin-top:10px;padding:8px 14px;background:#f0f8fd;border-radius:8px;font-weight:700;color:var(--cobalt-blue);">师评加权总分：<span id="teacherWeightedTotal">${Math.round(weightedTotal)}</span> / 100</div>`;
            html += `<div style="margin-top:10px;"><label style="font-weight:600;font-size:0.8rem;color:var(--cobalt-blue);display:block;margin-bottom:3px;"><i class="fas fa-comment"></i> 教师评语</label><textarea id="teacherComment" rows="3" style="width:100%;padding:8px 12px;border-radius:8px;border:1px solid #dce4ec;font-size:0.85rem;font-family:inherit;resize:vertical;">${appData.teacherComment || ''}</textarea></div>`;
            container.innerHTML = html;
            container.querySelectorAll('.teacher-score').forEach(sel => {
                sel.addEventListener('change', function() {
                    appData.teacherEval[this.dataset.id] = parseInt(this.value);
                    saveData(appData);
                    const newWeighted = TEACHER_EVAL_ITEMS.reduce((sum, item) => sum + (appData.teacherEval[item.id] || 0) * (item.weight / 100), 0);
                    document.getElementById('teacherWeightedTotal').textContent = Math.round(newWeighted);
                    renderScore();
                });
            });
            const commentArea = document.getElementById('teacherComment');
            if (commentArea) commentArea.addEventListener('input', function() { appData.teacherComment = this.value; saveData(appData); });
        }

        document.getElementById('saveTeacherEvalBtn').addEventListener('click', function() {
            const comment = document.getElementById('teacherComment');
            if (comment) appData.teacherComment = comment.value;
            saveData(appData);
            showToast('师评已保存');
            renderScore();
        });

        function renderScore() {
            const container = document.getElementById('scoreSummary');
            const detailContainer = document.getElementById('scoreDetail');
            let vocabTotal = 0, vocabCount = 0;
            VOCAB_DATA.forEach(item => {
                const data = appData.vocabScores[item.word];
                if (data && data.score > 0) { vocabTotal += data.score; vocabCount++; }
            });
            const vocabAvg = vocabCount > 0 ? Math.round(vocabTotal / vocabCount) : 0;
            const dialogueScore = appData.teacherEval['t2'] || 0;
            const rpTotal = ROLEPLAY_DIMENSIONS.reduce((sum, item) => sum + (appData.roleplayEval[item.id] || 0), 0);
            const rpAvg = ROLEPLAY_DIMENSIONS.length > 0 ? Math.round(rpTotal / ROLEPLAY_DIMENSIONS.length) : 0;
            const teacherWeighted = TEACHER_EVAL_ITEMS.reduce((sum, item) => sum + (appData.teacherEval[item.id] || 0) * (item.weight / 100), 0);
            const finalScore = Math.round(teacherWeighted);
            let grade = '待评定', gradeColor = '#8a9eb0';
            if (finalScore >= 90) { grade = '优秀'; gradeColor = '#2d7d5a'; }
            else if (finalScore >= 80) { grade = '良好'; gradeColor = '#2d7d5a'; }
            else if (finalScore >= 70) { grade = '中等'; gradeColor = '#c99f4a'; }
            else if (finalScore >= 60) { grade = '及格'; gradeColor = '#c99f4a'; }
            else if (finalScore > 0) { grade = '待提高'; gradeColor = '#c0392b'; }

            container.innerHTML = `
                <div class="score-box"><div class="label">词汇掌握</div><div class="value">${vocabAvg}</div><div class="weight">${vocabCount}/${VOCAB_DATA.length} 个已评分</div></div>
                <div class="score-box"><div class="label">对话理解</div><div class="value gold">${dialogueScore}</div><div class="weight">权重 30%</div></div>
                <div class="score-box"><div class="label">模拟展演</div><div class="value gold">${rpAvg}</div><div class="weight">权重 50%</div></div>
                <div class="score-box" style="background:#fdf8ee;border-color:var(--light-blue);"><div class="label">最终成绩</div><div class="value green" style="font-size:2rem;">${finalScore}</div><div class="weight" style="color:${gradeColor};font-weight:700;font-size:0.85rem;">${grade}</div></div>`;
            let detailHtml = `<h4 style="color:var(--cobalt-blue);margin:10px 0 6px;">📋 评分明细</h4>
                <table><thead><tr><th>评价维度</th><th>得分</th><th>权重</th><th>加权得分</th></tr></thead><tbody>
                    <tr><td>词汇掌握度</td><td>${vocabAvg}</td><td>—</td><td>—</td></tr>
                    <tr><td>对话理解与应答</td><td>${dialogueScore}</td><td>30%</td><td>${Math.round(dialogueScore * 0.3)}</td></tr>
                    <tr><td>模拟展演表现</td><td>${rpAvg}</td><td>50%</td><td>${Math.round(rpAvg * 0.5)}</td></tr>
                    <tr style="font-weight:700;background:#f0f8fd;"><td><strong>师评加权总分</strong></td><td colspan="3"><strong>${Math.round(teacherWeighted)}</strong> 分（${grade}）</td></tr>
                </tbody></table>`;
            detailContainer.innerHTML = detailHtml;
        }

        function init() {
            loadInfoToForm();
            renderVocab();
            renderPhrases();
            renderDialogues();
            renderRoles();
            renderScriptEditor();
            renderRoleplayEval();
            renderTeacherEval();
            renderScore();
            showToast('🚄 百工专列·景德镇站 高铁乘务英语实训系统已加载（40个词汇 · Craftsmen-Themed Train）', 'success');
        }

        setInterval(() => { saveData(appData); }, 30000);
        window.addEventListener('beforeunload', () => { saveData(appData); });

        if (document.readyState === 'complete') init();
        else window.addEventListener('load', init);
    </script>
</body>
</html>[Uploading index.html.html…]()
# English-for-Craftemen-Themed-Train
