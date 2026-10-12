<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Sopaan · Equivalent Algebraic Expressions</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700&family=Source+Sans+3:wght@400;600;700&family=IBM+Plex+Mono:wght@500;600&display=swap">
<style>
  html,body{margin:0;} img{max-width:100%;} [hidden]{display:none !important;}
  :root{
    --navy:#16264A; --navy-2:#1F3B6B; --gold:#C79A3E; --gold-soft:#F3E7C9;
    --paper:#FBF9F4; --paper-2:#F1EAD8; --card:#FFFFFF;
    --ink:#211E1A; --ink-soft:#655D4C; --rule:#E4DCC8;
    --success:#2E8B57; --success-soft:#E1F2E7;
    --danger:#BF4B45; --danger-soft:#FAE3E1;
    --locked:#C7BEA9;
    --focus:#1F3B6B;
    --accent-text:#1F3B6B; --retry-text:#8A661F;
    color-scheme:light;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
      --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
      --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
      --success:#7BC79A; --success-soft:#1B2E22;
      --danger:#E38884; --danger-soft:#331D1B;
      --locked:#4A4436;
      --focus:#E0B75B;
      --accent-text:#E0B75B; --retry-text:#E0B75B;
      color-scheme:dark;
    }
  }
  :root[data-theme="dark"]{
    --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
    --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
    --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
    --success:#7BC79A; --success-soft:#1B2E22;
    --danger:#E38884; --danger-soft:#331D1B;
    --locked:#4A4436;
    --focus:#E0B75B;
    --accent-text:#E0B75B; --retry-text:#E0B75B;
    color-scheme:dark;
  }

  *{box-sizing:border-box;}
  body{background:var(--paper); color:var(--ink); font-family:'Source Sans 3',-apple-system,'Segoe UI',sans-serif; padding-inline:0; padding-block:0;}
  h1,h2,h3{font-family:'Fraunces',Georgia,serif; text-wrap:balance; margin:0;}
  .num{font-family:'IBM Plex Mono',ui-monospace,monospace; font-variant-numeric:tabular-nums;}

  header.brand{
    background:linear-gradient(155deg,var(--navy) 0%, var(--navy-2) 100%);
    color:#F4EFDF; padding-block:calc(20px + env(safe-area-inset-top,0px)) 18px; padding-inline:20px;
  }
  .brand-row{display:flex; align-items:center; gap:12px; max-width:900px; margin:0 auto;}
  .crest{
    width:42px; height:42px; border-radius:10px; background:var(--gold); color:var(--navy);
    display:flex; align-items:center; justify-content:center; font-family:'Fraunces',serif; font-weight:700; font-size:18px; flex-shrink:0;
  }
  .brand-name{font-size:12px; letter-spacing:.08em; text-transform:uppercase; color:var(--gold); font-weight:700;}
  .series-name{font-size:19px; font-weight:700; font-family:'Fraunces',serif;}
  .chapter-eyebrow{max-width:900px; margin:14px auto 0; font-size:12px; letter-spacing:.06em; text-transform:uppercase; color:#AEB9D6;}
  .chapter-title{font-size:28px; max-width:900px; margin:2px auto 0;}
  .chapter-sub{font-size:14.5px; color:var(--gold); font-weight:700; max-width:900px; margin:3px auto 0;}

  .chapter-progress{max-width:900px; margin:14px auto 0; display:flex; align-items:center; gap:10px;}
  .cp-track{flex:1; height:6px; border-radius:99px; background:rgba(255,255,255,.18); overflow:hidden;}
  .cp-fill{height:100%; background:var(--gold); border-radius:99px; transition:width .3s ease;}
  .cp-label{font-size:11.5px; color:#CFD7EA; white-space:nowrap;}

  .tabbar{position:sticky; top:env(safe-area-inset-top,0px); z-index:15; background:var(--paper); border-bottom:1px solid var(--rule); overflow-x:auto; white-space:nowrap;}
  .tabbar-inner{max-width:900px; margin:0 auto; display:flex; padding-inline:16px;}
  .tab-btn{font-family:inherit; font-size:14px; font-weight:600; color:var(--ink-soft); background:none; border:none; padding:13px 16px; cursor:pointer; position:relative; flex-shrink:0;}
  .tab-btn.active{color:var(--accent-text);}
  .tab-btn.active::after{content:''; position:absolute; left:12px; right:12px; bottom:0; height:3px; background:var(--gold); border-radius:3px 3px 0 0;}
  .tab-count{font-size:11px; color:var(--ink-soft); margin-left:5px;}

  .slide-progress{max-width:900px; margin:0 auto; padding:10px 16px 0; display:flex; align-items:center; gap:10px;}
  .sp-track{flex:1; height:5px; border-radius:99px; background:var(--rule); overflow:hidden;}
  .sp-fill{height:100%; background:var(--accent-text); border-radius:99px; transition:width .3s ease;}
  .sp-label{font-size:12px; color:var(--ink-soft); white-space:nowrap; font-weight:600;}

  .wrap{max-width:900px; margin:0 auto; padding:16px 16px calc(110px + env(safe-area-inset-bottom,0px));}

  .qcard{background:var(--card); border:1px solid var(--rule); border-radius:14px; padding:18px;}
  .qhead{display:flex; align-items:flex-start; gap:10px; margin-bottom:10px;}
  .qnum{width:32px; height:32px; border-radius:8px; background:var(--gold-soft); color:var(--accent-text); display:flex; align-items:center; justify-content:center; font-weight:700; font-family:'Fraunces',serif; flex-shrink:0; font-size:14px;}
  .qtext{font-size:16px; line-height:1.55; flex:1;}
  .qtag{font-size:10.5px; color:var(--gold); background:var(--gold-soft); padding:2px 7px; border-radius:99px; font-weight:700; margin-left:6px; white-space:nowrap;}
  .marks-pill{font-size:11px; font-weight:700; color:var(--ink-soft); border:1px solid var(--rule); padding:3px 9px; border-radius:99px; margin-left:auto; flex-shrink:0; white-space:nowrap;}
  .step-badge{font-size:11px; font-weight:700; color:var(--accent-text); background:var(--paper-2); border:1px solid var(--rule); padding:3px 9px; border-radius:99px; display:inline-block; margin-bottom:12px;}

  .options{display:flex; flex-direction:column; gap:8px; margin-top:10px;}
  .opt{display:flex; align-items:center; gap:10px; padding:11px 12px; border:1.5px solid var(--rule); border-radius:10px; cursor:pointer; font-size:15px; background:var(--paper);}
  .opt input{accent-color:var(--navy-2);}
  .opt.is-correct{border-color:var(--success); background:var(--success-soft);}
  .opt.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .opt.locked{cursor:not-allowed;}

  .subpart-label{font-weight:700; font-size:12.5px; color:var(--accent-text); text-transform:uppercase; letter-spacing:.03em; margin:14px 0 6px;}
  .or-divider{text-align:center; font-size:11px; font-weight:700; letter-spacing:.08em; color:var(--ink-soft); margin:8px 0;}

  .steps{display:flex; flex-direction:column; gap:10px;}
  .step-line{font-size:14.5px; line-height:1.9; background:var(--paper); border:1px dashed var(--rule); border-radius:10px; padding:9px 12px;}
  .step-line.resolved{opacity:.9;}
  .blank-input{font-family:'IBM Plex Mono',monospace; font-size:14px; border:1.5px solid var(--rule); border-radius:6px; padding:3px 8px; width:120px; background:var(--card); color:var(--ink); margin:0 2px;}
  .blank-input:focus{outline:none; border-color:var(--focus); box-shadow:0 0 0 3px var(--gold-soft);}
  .blank-input.is-correct{border-color:var(--success); background:var(--success-soft);}
  .blank-input.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .blank-input[disabled]{opacity:.85;}
  .reveal-note{font-size:12px; color:var(--danger); padding-left:2px; margin-top:-2px;}

  .feedback{font-size:13.5px; padding:10px 12px; border-radius:9px; margin-top:14px; display:none;}
  .feedback.show{display:block;}
  .feedback.ok{background:var(--success-soft); color:var(--success);}
  .feedback.retry{background:var(--gold-soft); color:var(--retry-text);}
  .feedback.reveal{background:var(--danger-soft); color:var(--danger);}
  .feedback.err{background:var(--danger-soft); color:var(--danger);}
  .attempts-dots{display:inline-flex; gap:4px; margin-left:2px;}
  .attempts-dots span{width:6px; height:6px; border-radius:50%; background:var(--ink-soft); opacity:.3; display:inline-block;}
  .attempts-dots span.used{opacity:1; background:var(--danger);}

  .ar-box{background:var(--paper-2); border-radius:10px; padding:10px 12px; margin-bottom:12px; font-size:13px; color:var(--ink-soft);}

  .navbar{
    position:fixed; left:0; right:0; bottom:0; z-index:30; background:var(--paper);
    border-top:1px solid var(--rule); padding:10px 16px calc(10px + env(safe-area-inset-bottom,0px));
  }
  .navbar-inner{max-width:900px; margin:0 auto; display:flex; gap:8px; flex-wrap:wrap; align-items:center;}
  .btn{font-family:inherit; font-size:13.5px; font-weight:700; padding:10px 14px; border-radius:9px; border:1.5px solid var(--rule); background:var(--card); color:var(--ink); cursor:pointer;}
  .btn:hover{border-color:var(--navy-2);}
  .btn:disabled{opacity:.4; cursor:not-allowed;}
  .btn-primary{background:var(--navy-2); color:#fff; border-color:var(--navy-2);}
  .navbar .spacer{flex:1;}

  .fab{position:fixed; right:16px; bottom:calc(74px + env(safe-area-inset-bottom,0px)); background:var(--gold); color:var(--navy); border:none; border-radius:999px; padding:11px 16px; font-family:inherit; font-weight:700; font-size:13px; display:flex; align-items:center; gap:7px; cursor:pointer; box-shadow:0 6px 16px rgba(0,0,0,.18); z-index:35;}
  .fab-badge{background:rgba(255,255,255,.55); border-radius:99px; padding:1px 7px; font-size:11px;}

  .overlay{position:fixed; inset:0; background:rgba(20,18,14,.45); z-index:50; display:none; align-items:flex-end; justify-content:center;}
  .overlay.show{display:flex;}
  .palette{background:var(--card); width:min(480px,100%); max-height:78vh; overflow-y:auto; border-radius:18px 18px 0 0; padding:18px 18px calc(18px + env(safe-area-inset-bottom,0px)); border:1px solid var(--rule); border-bottom:none;}
  @media (min-width:640px){ .overlay{align-items:center;} .palette{border-radius:18px; border-bottom:1px solid var(--rule); max-height:74vh;} }
  .palette-head{display:flex; align-items:center; justify-content:space-between; margin-bottom:6px;}
  .palette-head h2{font-size:16px;}
  .palette-close{background:none; border:none; font-size:20px; color:var(--ink-soft); cursor:pointer; padding:4px;}
  .palette-legend{display:flex; gap:12px; flex-wrap:wrap; font-size:11px; color:var(--ink-soft); margin:10px 0 14px;}
  .palette-legend span{display:inline-flex; align-items:center; gap:5px;}
  .dot{width:9px; height:9px; border-radius:50%; display:inline-block;}
  .dot.correct{background:var(--success);} .dot.revealed{background:var(--danger);}
  .dot.skipped{background:var(--gold);} .dot.locked{background:var(--locked);}
  .dot.current{background:var(--navy-2);}
  .chip-grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(48px,1fr)); gap:8px;}
  .chip{border:1.5px solid var(--rule); border-radius:9px; padding:8px 4px; text-align:center; font-family:'IBM Plex Mono',monospace; font-size:12.5px; font-weight:600; cursor:pointer; background:var(--paper); color:var(--ink);}
  .chip[data-status="correct"]{border-color:var(--success); background:var(--success-soft); color:var(--success);}
  .chip[data-status="revealed"]{border-color:var(--danger); background:var(--danger-soft); color:var(--danger);}
  .chip[data-status="skipped"]{border-color:var(--gold); background:var(--gold-soft); color:var(--retry-text);}
  .chip[data-status="locked"]{border-color:var(--rule); color:var(--locked); cursor:not-allowed; background:var(--paper-2);}
  .chip[data-status="current"]{outline:2px solid var(--navy-2); outline-offset:1px;}

  .toast{position:fixed; left:50%; bottom:calc(140px + env(safe-area-inset-bottom,0px)); transform:translateX(-50%); background:var(--ink); color:var(--paper); padding:9px 16px; border-radius:99px; font-size:13px; opacity:0; pointer-events:none; transition:opacity .25s ease; z-index:60;}
  .toast.show{opacity:1;}

  .done-card{text-align:center; padding:36px 20px;}
  .done-card .big{font-size:38px; margin-bottom:6px;}
  .score-pills{display:flex; gap:10px; justify-content:center; flex-wrap:wrap; margin:16px 0;}
  .score-pill{padding:8px 16px; border-radius:99px; font-size:13px; font-weight:700;}

  footer.brandfoot{max-width:900px; margin:14px auto 0; padding:0 16px calc(110px + env(safe-area-inset-bottom,0px)); text-align:center; font-size:12px; color:var(--ink-soft);}

  .mode-pill{font-family:inherit; font-size:12.5px; font-weight:700; color:var(--navy); background:var(--gold); border:none; border-radius:99px; padding:6px 14px; cursor:pointer; margin-top:12px; display:inline-flex; align-items:center; gap:6px;}
  .mode-pick{display:flex; flex-direction:column; gap:14px; padding:8px 0 24px;}
  .mode-card{background:var(--card); border:1.5px solid var(--rule); border-radius:16px; padding:22px; cursor:pointer; text-align:left;}
  .mode-card:hover{border-color:var(--navy-2);}
  .mode-card .mode-icon{font-size:26px; margin-bottom:8px;}
  .mode-card h3{font-size:18px; margin-bottom:6px;}
  .mode-card p{font-size:13.5px; color:var(--ink-soft); line-height:1.5; margin:0;}
  .quiz-hint{font-size:12.5px; color:var(--ink-soft); background:var(--paper-2); border-radius:9px; padding:8px 12px; margin-bottom:14px;}
  .review-row{border:1px solid var(--rule); border-radius:10px; padding:11px 13px; margin-bottom:10px;}
  .review-tag{font-size:11.5px; font-weight:700; margin-bottom:4px; display:block;}
  .review-tag.ok{color:var(--success);} .review-tag.bad{color:var(--danger);} .review-tag.na{color:var(--ink-soft);}
  .review-q{font-size:13.5px; margin-bottom:6px; color:var(--ink-soft);}
  .review-ans{font-size:13px; margin-bottom:2px;}

  .who-row{max-width:900px; margin:12px auto 0; display:flex; flex-wrap:wrap; gap:8px; align-items:center;}
  .who-row .mode-pill{margin-top:0;}
  .who{display:inline-flex; flex-wrap:wrap; align-items:center; gap:6px; font-size:12.5px; color:#CFD7EA;}
  .who b{color:#F4EFDF;}
  .who button{font-family:inherit; font-size:12px; font-weight:700; color:#F4EFDF; background:rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.22); border-radius:99px; padding:5px 11px; cursor:pointer;}
  .who button:hover{background:rgba(255,255,255,.2);}
  .login-card{max-width:460px; margin:8px auto 0; background:var(--card); border:1px solid var(--rule); border-radius:16px; padding:22px;}
  .login-card h2{font-size:21px; margin-bottom:4px;}
  .login-card p.lead{font-size:13.5px; color:var(--ink-soft); margin:0 0 16px; line-height:1.5;}
  .fld{display:flex; flex-direction:column; gap:5px; margin-bottom:12px;}
  .fld label{font-size:12px; font-weight:700; letter-spacing:.04em; text-transform:uppercase; color:var(--ink-soft);}
  .fld input{font-family:inherit; font-size:15px; padding:10px 12px; border:1.5px solid var(--rule); border-radius:9px; background:var(--paper); color:var(--ink);}
  .fld input:focus{outline:none; border-color:var(--focus); box-shadow:0 0 0 3px var(--gold-soft);}
  .fld-row{display:grid; grid-template-columns:1fr 1fr; gap:10px;}
  .login-err{font-size:13px; color:var(--danger); background:var(--danger-soft); border-radius:8px; padding:8px 10px; margin-bottom:12px;}
  .login-note{font-size:12px; color:var(--ink-soft); margin-top:12px; line-height:1.5;}
  .known{margin:0 0 16px; display:flex; flex-direction:column; gap:6px;}
  .known-label{font-size:12px; font-weight:700; letter-spacing:.04em; text-transform:uppercase; color:var(--ink-soft);}
  .known-btn{display:flex; justify-content:space-between; align-items:center; gap:10px; text-align:left; font-family:inherit; font-size:14.5px; padding:10px 12px; border:1.5px solid var(--rule); border-radius:10px; background:var(--paper); color:var(--ink); cursor:pointer;}
  .known-btn:hover{border-color:var(--navy-2);}
  .known-btn small{font-size:12px; color:var(--ink-soft);}
  .rec-card{background:var(--card); border:1px solid var(--rule); border-radius:14px; padding:18px; margin-bottom:14px;}
  .rec-card h2{font-size:19px; margin-bottom:10px;}
  .rec-card h3{font-size:15px; margin:4px 0 8px;}
  .rec-table-wrap{overflow-x:auto;}
  .rec-table{width:100%; border-collapse:collapse; font-size:13.5px; font-variant-numeric:tabular-nums;}
  .rec-table th{text-align:left; font-size:11.5px; text-transform:uppercase; letter-spacing:.04em; color:var(--ink-soft); padding:6px 8px; border-bottom:1px solid var(--rule); white-space:nowrap;}
  .rec-table td{padding:8px; border-bottom:1px solid var(--rule); white-space:nowrap;}
  .rec-bar{display:inline-block; width:70px; height:6px; border-radius:99px; background:var(--rule); overflow:hidden; vertical-align:middle; margin-right:6px;}
  .rec-bar i{display:block; height:100%; background:var(--success);}
  .rec-empty{font-size:13.5px; color:var(--ink-soft);}
  .sec-sub{max-width:900px; margin:0 auto; padding:10px 16px 0; font-size:12.5px; font-weight:700; color:var(--accent-text); letter-spacing:.02em;}
  .opt{flex-wrap:wrap;}
  .opt-l{font-family:'IBM Plex Mono',monospace; font-size:13px; font-weight:600; color:var(--ink-soft);}
  .opt-t{flex:1; min-width:0;}
  .opt.is-chosen:not(.is-correct):not(.is-wrong){border-color:var(--navy-2); background:var(--gold-soft);}
  .opt-tag{font-size:11px; font-weight:700; padding:2px 8px; border-radius:99px; background:var(--card); border:1px solid currentColor; white-space:nowrap;}
  .opt.is-correct .opt-tag{color:var(--success);} .opt.is-wrong .opt-tag{color:var(--danger);} .opt.is-chosen:not(.is-correct):not(.is-wrong) .opt-tag{color:var(--accent-text);}
  .chosen{font-size:13.5px; margin-top:10px; padding:8px 12px; border-radius:9px;}
  .chosen.ok{background:var(--success-soft); color:var(--success);} .chosen.bad{background:var(--danger-soft); color:var(--danger);}
  .chosen + .chosen{margin-top:6px;}
  .solution{margin-top:14px; border:1px solid var(--rule); border-left:4px solid var(--gold); background:var(--paper-2); border-radius:10px; padding:12px 14px;}
  .sol-h{font-family:'Fraunces',Georgia,serif; font-weight:700; font-size:14px; color:var(--accent-text); margin-bottom:6px;}
  .sol-line{font-size:14.5px; line-height:1.7;}
  .rev-sol summary{cursor:pointer; font-size:12.5px; font-weight:700; color:var(--accent-text); margin-top:6px;}
  .rev-sol .solution{margin-top:8px;}
  .chapter-credit{max-width:900px; margin:4px auto 0; font-size:12px; color:#CFD7EA;}
  footer.brandfoot a{color:inherit;}
  .blank-input.wide{width:260px; max-width:100%; font-family:'Source Sans 3',sans-serif;}
  .blank-input.expr{width:170px; max-width:100%;}
  /*fix-layout*/ .cp-fill,.sp-fill{width:0;} .fld{min-width:0;} .fld input{width:100%; min-width:0; box-sizing:border-box;}
  .fig{margin:6px 0 10px; display:flex; justify-content:center;}
  .figsvg{width:100%; max-width:340px; height:auto; overflow:visible;}
  .figsvg .ln,.figsvg .arm{stroke:var(--ink); stroke-width:1.6; fill:none;}
  .figsvg .arm{stroke:var(--accent-text); stroke-width:2;}
  .figsvg .pt{fill:var(--ink);}
  .figsvg .lb{fill:var(--ink); font:600 13px 'Source Sans 3',sans-serif;}
  .figsvg .al{fill:var(--accent-text); font:700 12px 'Source Sans 3',sans-serif;}
  .figsvg .wg{fill:var(--gold-soft); stroke:var(--gold); stroke-width:1.2;}
  .figsvg .wg2{fill:rgba(199,154,62,.35); stroke:var(--gold); stroke-width:1.2;}
  .figsvg .ra{fill:none; stroke:var(--ink); stroke-width:1.2;}
  .figsvg .ahd{fill:var(--ink);}
  .figsvg .pr{fill:var(--paper-2); stroke:var(--ink-soft); stroke-width:1.2;}
  .figsvg .tk{stroke:var(--ink-soft); stroke-width:.8;}
  .figsvg .po{fill:var(--ink); font:600 8.5px 'IBM Plex Mono',monospace;}
  .figsvg .pi{fill:var(--danger); font:600 7.5px 'IBM Plex Mono',monospace;}
  .figsvg .sh{fill:var(--gold-soft); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .sh2{fill:rgba(199,154,62,.38); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .sh3{fill:rgba(199,154,62,.22); stroke:var(--ink); stroke-width:1.5; stroke-linejoin:round;}
  .figsvg .none{fill:none;}
  .figsvg .hid{stroke-dasharray:5 4; fill:none;}
  .figsvg .tick{stroke:var(--ink); stroke-width:1.4; fill:none;}
  .figsvg .shd{fill:var(--accent-text); fill-opacity:.55;}
  .figsvg .cell{fill:var(--card); stroke:var(--ink); stroke-width:1.1;}
  .figsvg .dr{fill:var(--danger);} .figsvg .dw{fill:var(--card); stroke:var(--ink); stroke-width:1.2;}
  .figsvg .dotfill{fill:var(--danger);}
  .tt{border-collapse:collapse; font-size:13.5px; margin:4px auto; font-variant-numeric:tabular-nums;} .tt th,.tt td{border:1px solid var(--rule); padding:4px 9px; text-align:left;} .tt th{background:var(--paper-2); font-weight:700;} .ttw{overflow-x:auto; max-width:100%;}
  .fq{display:inline-flex; flex-direction:column; vertical-align:middle; text-align:center; font-size:.82em; line-height:1.12; margin:0 2px;}
  .fq>span:first-child{border-bottom:1.5px solid currentColor; padding:0 2px;}
  .fq>span:last-child{padding:0 2px;}
  .mx{white-space:nowrap;}
  .blank-input.fr{width:110px;}
  @media (prefers-reduced-motion:reduce){ *{transition:none !important;} }
.datline{display:block;margin-top:8px;padding:8px 10px;border-radius:8px;background:var(--paper-2);font:500 14px/1.7 'IBM Plex Mono',monospace;word-spacing:2px;overflow-wrap:anywhere;}

  .theory{display:flex;flex-direction:column;gap:16px;padding-bottom:40px;}
  .hub{display:grid;grid-template-columns:1fr;gap:12px;}
  @media (min-width:640px){ .hub{grid-template-columns:repeat(3,1fr);} }
  .hub-card{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:16px;display:flex;flex-direction:column;gap:8px;}
  .hub-card h3{font-family:'Fraunces',serif;font-size:18px;margin:0;color:var(--accent-text);}
  .hub-card p{margin:0;font-size:14px;color:var(--ink-soft);line-height:1.5;}
  .hub-btns{display:flex;flex-wrap:wrap;gap:8px;margin-top:auto;}
  .hub-btn{min-height:40px;border:1.5px solid var(--rule);background:var(--paper-2);color:var(--ink);border-radius:10px;padding:8px 12px;font:600 14px 'Source Sans 3',sans-serif;cursor:pointer;text-align:left;}
  .hub-btn:hover{border-color:var(--gold);}
  .hub-btn.primary{background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .note{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:18px;scroll-margin-top:120px;}
  .note h2{font-family:'Fraunces',serif;font-size:22px;margin:0 0 4px;color:var(--ink);}
  .note .lt{font-size:13.5px;color:var(--ink-soft);margin:0 0 12px;}
  .note .lt b{color:var(--accent-text);}
  .note h4{font:700 15px 'Source Sans 3',sans-serif;margin:16px 0 6px;color:var(--accent-text);}
  .note p,.note li{font-size:15.5px;line-height:1.6;}
  .note ul{padding-left:20px;margin:6px 0;}
  .keybox{background:var(--gold-soft);border-left:4px solid var(--gold);border-radius:8px;padding:10px 12px;margin:10px 0;font-size:15px;line-height:1.6;}
  .keybox b{color:var(--ink);}
  .ex{background:var(--paper-2);border-radius:10px;padding:12px;margin:10px 0;}
  .ex .exh{font-family:'Fraunces',serif;font-weight:700;color:var(--accent-text);margin-bottom:4px;}
  .ex .exl{font-size:15px;line-height:1.7;}
  .ttab{width:100%;border-collapse:collapse;font-size:14.5px;margin:8px 0;}
  .ttab th,.ttab td{border:1px solid var(--rule);padding:7px 8px;text-align:left;vertical-align:top;}
  .ttab th{background:var(--paper-2);}
  .tscroll{overflow-x:auto;}
  .mono{font-family:'IBM Plex Mono',monospace;font-size:.92em;}
  @media (max-width:480px){ .ttab{font-size:13.5px;} .ttab th,.ttab td{padding:6px;} }
  .note .figsvg{max-width:100%;height:auto;display:block;margin:8px auto;}


  .rep-top{display:flex;flex-wrap:wrap;gap:18px;align-items:center;justify-content:center;margin-top:8px;}
  .rep-legend{flex:1;min-width:220px;display:flex;flex-direction:column;gap:8px;}
  .rep-cap{font:700 13px 'Source Sans 3',sans-serif;color:var(--ink-soft);text-transform:uppercase;letter-spacing:.05em;}
  .rep-li{display:flex;align-items:center;gap:6px;font-size:15px;}
  .rep-n{margin-left:auto;white-space:nowrap;padding-left:8px;font-family:'IBM Plex Mono',monospace;font-weight:600;}
  .sw{display:inline-block;width:12px;height:12px;border-radius:3px;flex:none;}
  .rep-grid{display:grid;grid-template-columns:1fr;gap:12px;}
  @media (min-width:640px){ .rep-grid{grid-template-columns:1fr 1fr;} }
  .rep-card{background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:14px;display:flex;flex-direction:column;gap:10px;}
  .rep-h{display:flex;align-items:center;gap:8px;font:700 16px 'Source Sans 3',sans-serif;}
  .crit{display:inline-grid;place-items:center;width:28px;height:28px;border-radius:50%;color:var(--card);font:700 15px Fraunces,serif;flex:none;}
  .rep-row{display:flex;gap:14px;align-items:center;}
  .rep-stats{display:flex;flex-direction:column;gap:5px;font-size:14.5px;}
  .rep-stats div{display:flex;align-items:center;gap:6px;}
  .rep-lvl{margin-top:4px;color:var(--accent-text);} .rep-lvl span{color:var(--ink-soft);font-size:13px;}
  .rep-note{font-size:13px;color:var(--ink-soft);}


  .skip-chips{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin:12px 0;}
  .skip-chips .chip{min-width:48px;min-height:40px;cursor:pointer;border:1.5px solid var(--gold);background:var(--gold-soft);color:var(--retry-text);border-radius:10px;font:600 14px 'IBM Plex Mono',monospace;}
  .skip-btns{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin-top:12px;}


  .kb-toggle{border:none;background:transparent;font-size:15px;cursor:pointer;padding:0 2px;vertical-align:middle;opacity:.7;}
  .vkb{position:fixed;left:0;right:0;bottom:0;z-index:80;background:var(--paper-2);border-top:1px solid var(--rule);box-shadow:0 -6px 20px rgba(0,0,0,.12);padding:6px 6px 8px;display:none;}
  .vkb.show{display:block;}
  .vkb-top{display:flex;justify-content:space-between;align-items:center;max-width:640px;margin:0 auto 4px;font:600 12px 'Source Sans 3',sans-serif;color:var(--ink-soft);}
  .vkb-link{border:none;background:none;color:var(--accent-text);font:600 12px 'Source Sans 3',sans-serif;cursor:pointer;text-decoration:underline;}
  .vkb-row{display:flex;gap:5px;max-width:640px;margin:0 auto 5px;}
  .vkb-k{flex:1;min-height:42px;border:1px solid var(--rule);border-radius:8px;background:var(--card);color:var(--ink);font:600 17px 'IBM Plex Mono',monospace;cursor:pointer;padding:0;}
  .vkb-k.fn{font:600 13px 'Source Sans 3',sans-serif;background:var(--gold-soft);}
  .vkb-k.done{background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .vkb-k:active{transform:scale(.96);}
  body.kb-open .wrap{padding-bottom:360px;}
  body.kb-open .fab{display:none;}
  .tool-bar{display:flex;gap:8px;flex-wrap:wrap;margin:-4px 0 10px;}
  .tool-btn{min-height:36px;border:1.5px solid var(--gold);background:var(--gold-soft);color:var(--ink);border-radius:18px;padding:4px 12px;font:600 13.5px 'Source Sans 3',sans-serif;cursor:pointer;}
  .tool-panel{position:fixed;z-index:85;background:var(--card);border:1px solid var(--rule);border-radius:14px;box-shadow:0 10px 30px rgba(0,0,0,.25);display:none;}
  .tool-panel.show{display:block;}
  .tp-head{display:flex;align-items:center;gap:8px;padding:8px 10px;border-bottom:1px solid var(--rule);font:600 14px 'Source Sans 3',sans-serif;}
  .tp-note{font-size:12px;color:var(--ink-soft);font-weight:500;}
  .tp-x{margin-left:auto;border:1px solid var(--rule);background:var(--paper-2);color:var(--ink);border-radius:8px;min-height:32px;padding:2px 10px;cursor:pointer;font:600 13px 'Source Sans 3',sans-serif;}
  .tp-x + .tp-x{margin-left:0;}
  .calc{right:12px;bottom:84px;width:min(330px,calc(100vw - 24px));}
  body.calc-open .wrap{padding-bottom:440px;}
  body.calc-open .fab{display:none;}
  @media (max-width:640px){ .calc{left:6px;right:6px;width:auto;} .calc-keys button{min-height:36px;} }
  .calc-disp{padding:8px 12px;text-align:right;background:var(--paper-2);}
  .calc-expr{font:500 13px 'IBM Plex Mono',monospace;color:var(--ink-soft);min-height:18px;word-break:break-all;}
  .calc-res{font:600 24px 'IBM Plex Mono',monospace;color:var(--ink);word-break:break-all;}
  .calc-keys{display:grid;grid-template-columns:repeat(6,1fr);gap:5px;padding:8px;}
  .calc-keys button{min-height:40px;border:1px solid var(--rule);border-radius:8px;background:var(--card);color:var(--ink);font:600 14px 'IBM Plex Mono',monospace;cursor:pointer;padding:0;}
  .calc-keys button.fn{background:var(--gold-soft);font-family:'Source Sans 3',sans-serif;font-size:13px;}
  .calc-keys button.eq{grid-column:span 2;background:var(--navy);color:#F4EFDF;border-color:var(--navy);}
  .desmos{left:50%;top:50%;transform:translate(-50%,-50%);width:min(760px,calc(100vw - 16px));height:min(560px,calc(100vh - 90px));flex-direction:column;}
  .desmos.show{display:flex;}
  #desmosBox{flex:1;min-height:0;border-radius:0 0 14px 14px;overflow:hidden;}
  .desmos-msg{padding:24px;text-align:center;color:var(--ink-soft);}
  .chip[data-status="skipped"]{cursor:pointer;}
  .chip[data-status="answered"]{border-color:var(--accent-text);color:var(--accent-text);}


  button.crest-home{border:none;padding:0;position:relative;cursor:pointer;transition:transform .15s ease;}
  button.crest-home:hover,button.crest-home:focus-visible{transform:scale(1.06);outline:2px solid var(--gold);outline-offset:2px;}
  .crest-h{position:absolute;right:-7px;bottom:-7px;width:18px;height:18px;border-radius:50%;background:#F4EFDF;color:var(--navy);font:700 12px/18px 'Source Sans 3',sans-serif;text-align:center;box-shadow:0 1px 3px rgba(0,0,0,.3);}
  .brand .brand-row{position:relative;}
  .bmasw{position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);display:flex;flex-shrink:0;white-space:nowrap;align-items:center;gap:6px;background:rgba(255,255,255,.12);border:1px solid rgba(255,255,255,.25);border-radius:99px;padding:5px 14px;color:#F4EFDF;}
  .bmasw-ic{font-size:16px;} .bmasw-t{font:600 20px 'IBM Plex Mono',monospace;letter-spacing:.02em;min-width:62px;text-align:center;}
  .bmasw-b{border:none;background:rgba(255,255,255,.18);color:#F4EFDF;border-radius:50%;width:30px;height:30px;cursor:pointer;font-size:13px;}
  .bmasw.off{display:none;}
  @media (max-width:560px){ .bmasw{position:static;transform:none;margin-left:auto;padding:4px 5px 4px 8px;gap:4px;} .bmasw-ic{display:none;} .bmasw-t{font-size:16px;min-width:48px;} .bmasw-b{width:26px;height:26px;} .brand .series-name{font-size:15px;} .brand .brand-name{font-size:10.5px;} .brand .brand-row>div:not(.bmasw){min-width:0;} }
  .bmasw-done{font:600 15px 'IBM Plex Mono',monospace;color:var(--accent-text);margin:4px 0 8px;}
  .sp-fab{position:fixed;left:14px;bottom:84px;z-index:60;border:1.5px solid var(--navy-2);background:var(--card);color:var(--ink);border-radius:99px;padding:9px 14px;font:700 14px 'Source Sans 3',sans-serif;box-shadow:0 4px 14px rgba(0,0,0,.15);cursor:pointer;}
  .sp-fab.on{background:var(--navy);color:#F4EFDF;}
  body.kb-open .sp-fab{display:none;}
  .sp-canvas{position:absolute;z-index:55;display:none;touch-action:none;cursor:crosshair;}
  .sp-canvas.passive{pointer-events:none;cursor:default;}
  .sp-bar{position:fixed;top:8px;left:8px;right:8px;margin:0 auto;width:max-content;z-index:90;display:none;align-items:center;gap:6px;background:var(--card);border:1px solid var(--rule);border-radius:14px;padding:6px 8px;box-shadow:0 6px 20px rgba(0,0,0,.2);max-width:calc(100vw - 16px);flex-wrap:wrap;justify-content:center;}
  .sp-lbl{font:700 13px 'Source Sans 3',sans-serif;color:var(--ink-soft);margin-right:2px;}
  .sp-pen,.sp-tool{width:38px;height:38px;border-radius:10px;border:1.5px solid var(--rule);background:var(--paper);cursor:pointer;display:inline-flex;align-items:center;justify-content:center;font-size:17px;padding:0;color:var(--ink);}
  .sp-pen i{width:20px;height:20px;border-radius:50%;display:block;}
  .sp-pen.on,.sp-tool.on{border-color:var(--navy-2);box-shadow:0 0 0 3px var(--gold-soft);}
  @media (max-width:560px){ .sp-lbl{display:none;} .sp-pen,.sp-tool{width:34px;height:34px;} .sp-fab span{display:none;} }

  /* larger reading sizes */
  .chapter-eyebrow{font-size:13.5px;}
  .chapter-title{font-size:36px;line-height:1.15;}
  .chapter-sub{font-size:16.5px;}
  .tab-btn{font-size:15.5px;}
  .sec-sub{font-size:15px;}
  .qtext{font-size:19px;line-height:1.55;}
  .qnum{width:36px;height:36px;font-size:16px;}
  .opt{font-size:17.5px;padding:12px 14px;}
  .step-line{font-size:17.5px;line-height:2;}
  .blank-input{font-size:16px;}
  .sol-line{font-size:16.5px;}
  .feedback{font-size:15px;}
  .note h2{font-size:28px;}
  .note h4{font-size:19px;}
  .note p,.note li{font-size:17.5px;line-height:1.65;}
  .note .lt{font-size:15.5px;}
  .ex .exh{font-size:18px;} .ex .exl{font-size:16.5px;}
  .keybox{font-size:16.5px;}
  .ttab{font-size:15.5px;}
  .hub-card h3{font-size:21px;} .hub-card p{font-size:15.5px;} .hub-btn{font-size:15px;}
  @media (max-width:480px){ .chapter-title{font-size:30px;} .qtext{font-size:18px;} .opt,.step-line{font-size:16.5px;} .note h2{font-size:24px;} .note p,.note li{font-size:16.5px;} }

  /* v4 celebration */
  .v4conf{position:fixed;inset:0;width:100vw;height:100vh;pointer-events:none;z-index:9999;}
  .v4ban{background:linear-gradient(135deg,var(--gold-soft),var(--card));border:2px solid var(--gold);border-radius:18px;padding:18px 14px 16px;margin:-4px 0 18px;text-align:center;animation:v4pop .55s cubic-bezier(.2,1.6,.4,1);}
  @keyframes v4pop{0%{transform:scale(.6);opacity:0}100%{transform:scale(1);opacity:1}}
  .v4trophy{font-size:54px;line-height:1;animation:v4bob 1.4s ease-in-out infinite;}
  @keyframes v4bob{0%,100%{transform:translateY(0) rotate(-6deg)}50%{transform:translateY(-6px) rotate(6deg)}}
  .v4h{font-size:28px;font-weight:800;color:var(--accent-text);margin-top:6px;}
  .v4m{font-size:19px;color:var(--ink);margin-top:4px;}
  .v4pills{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:12px;}
  .v4p{font-size:16px;font-weight:700;border-radius:999px;padding:6px 12px;}
  .v4p.g{background:var(--success-soft);color:var(--success);} .v4p.o{background:var(--gold-soft);color:var(--retry-text);}
  .v4p.r{background:var(--danger-soft);color:var(--danger);} .v4p.s{background:var(--rule);color:var(--ink);}
  .v4next{margin-top:14px;} .v4go{font-size:18px !important;padding:13px 20px !important;}
  .v4rec td.v4g{color:var(--success);font-weight:700;} .v4rec td.v4o{color:var(--retry-text);font-weight:700;} .v4rec td.v4r{color:var(--danger);font-weight:700;}
  .v4rec tr.v4tot td{font-weight:800;border-top:2px solid var(--rule);}
  .v4rec th{font-size:12.5px;padding:6px 3px !important;white-space:nowrap;} .v4rec td{font-size:15px;padding:7px 3px !important;text-align:center;}
  .v4rec td:first-child,.v4rec th:first-child{text-align:left;white-space:normal;min-width:92px;max-width:150px;font-size:14.5px;}
  @media(max-width:460px){ .v4left{display:none;} }
  .v4leg{font-size:14.5px;color:var(--ink-soft);margin:2px 0 8px;line-height:1.5;}
  body.v4done .fab-q,body.v4done #qFab{display:none;}
  .v4sum{font-size:16px;margin-top:10px;}
  /* v4 larger reading sizes */
  body{font-size:18px;}
  .chapter-title{font-size:38px !important;line-height:1.15;}
  .chapter-sub{font-size:17px !important;}
  .tab-btn{font-size:16.5px !important;}
  .sec-sub{font-size:16.5px !important;}
  .qtext{font-size:21px !important;line-height:1.6 !important;}
  .qnum{width:38px !important;height:38px !important;font-size:17px !important;}
  .opt{font-size:19.5px !important;padding:13px 15px !important;}
  .step-line{font-size:19.5px !important;line-height:2.1 !important;}
  .blank-input{font-size:18px !important;min-height:40px;}
  .sol-line{font-size:18px !important;line-height:1.6;}
  .feedback{font-size:16.5px !important;}
  .note h2{font-size:29px !important;}
  .note h3{font-size:22px !important;}
  .note h4{font-size:20px !important;}
  .note p,.note li,.note td,.note th{font-size:18.5px !important;line-height:1.7 !important;}
  .ex .exh{font-size:19px !important;} .ex .exl{font-size:18px !important;}
  .keybox{font-size:18px !important;}
  .hub-card p{font-size:17.5px !important;} .hub-btn{font-size:16.5px !important;}
  .review-q,.review-ans{font-size:17.5px !important;}
  .rec-table td{font-size:16px;}
  .vkb-k{font-size:19px !important;}
  .fq{font-size:0.95em;}

  header.brand{background:linear-gradient(180deg,rgba(20,20,20,.55),rgba(20,20,20,.78)),url('data:image/jpeg;base64,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') center/cover no-repeat, #2b2b2b !important;}
  .crest,button.crest-home{width:58px !important;height:54px !important;background:transparent !important;border-radius:12px !important;}
  .crest img{width:58px;height:53px;display:block;filter:drop-shadow(0 1px 2px rgba(0,0,0,.5));}
  button.crest-home .crest-h{right:-4px;bottom:-4px;}
  .brand-name{color:#F4EFDF !important;font-family:'Fraunces',Georgia,serif;font-size:13px !important;letter-spacing:.06em;}
  .series-name{color:#E8D9A8;}
  .chapter-eyebrow{color:#D9D4C7 !important;}
  .chapter-sub{color:#F1D58A !important;}
</style>
</head>
<body>
<header class="brand">
  <div class="brand-row">
    <div class="crest"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIQAAAB4CAYAAAAzFFrFAAAiZUlEQVR42u1deZwcVbX+TvfMZBICIQSTsATEQAgQUHYwbIIgEhSMqOyLyvbQh+AKylORJfhYRBRFRHiACoKgIIsgS1gjyL4vIexZSAIkJJmlu7/3R52TOXNTVV3V3TOZCVO/3/y6p6vqruee9Tv3Cgau1IukABAAFBGuwP0sAhgs/bTxBZ0k337qpFUaSAgFESkH9aJRdTSgjc02DiLS/mFcrUWdqNSJJNlU7bkMxLB00EmuS3LlkDD6yJg0kWzNsoiyjIn0I46wlGWT/CiAMQA2AbAGgAUAngXwmog86wnIr/CsdYlIheSqAE4BMBnACAAfAHgCwE9FZJo9NyBUl49ss+9fIXk7yQWMvzpJTiN5DMnB4ftZOIOupNVJPplQRxvJSXnLHrgaSAwkx5L8VzAxZZIlJYKS/u+vp0jummfiXH2/cZNfcX8d+vtMksOVgGRgpnpPTIDkViTfchygpJMTd1WUMDrdb0eZrM2iNyh3eE/LqSRwIZI8SrnJoCy6TS9bRTVxYABo6qvEoHJ8AwA3ARgJoBNAcwadSAAUAJjucBHJThG5tIpOIWqprAJgZS0jycwkgE1Uh2gPBlcAVKqZqc5S8vWXazVtleAJoJlku9O3RERIcpS2a65aSlZPgdFDlb7KGUyOF0n+O1iVea+y/rWR3CjNQnAc6aOuvkpKuW0k7yJ5EsmdSQ5LsIqawjrTrJRaOY2NW4yVZJxvpSQuuVxFn1ZuA+X/ip61kzxaB7+D9V0l/bzN6k4bFJJDSL7uiCnpmh/8P5vkdSSPJTmB5KAEc7jJicILtV03kzzOzMeemhxtw6p9QrwpERSzNFo//+N0AjaIKHZMUzIdUZ7m3qvoZ8lxjvtVqdyC5MnKKZYEdb5M8hK1jMYE9Xwzgev9h+QYv9p7gCCGuDEeop8j1MnV834Ic/2ajCK5EoAtAawJYBSAVQGMBjALwBki0klyPfUrtKpcrLedJQBFAH8UkUNINolIKcVNXQBwAYCjY+qeC2AzEZkZvDsKwHYA9gCwE4AJ7nYFwIMAbgMwA8Dl+nun1gXVeVoA3A1gt0Z6RJN8JiQnAngcwMYAZojI3N70IWxD8vck30xYxR0mh0l+2snqRlymC7zt/BNShUusQ7Kd5CKS95G8nuQr2s49nRdzGa+ocsMNSR5B8qqEPldq5WQNNOd7zzpylY4meUXMYHTqX4cOxDySo5187UxR6mohCKtz0yrKpbX7bH33Z+7eDvrbMyRbvDvY60YxZa5E8hMk/0uJspJi0lZI/k8WUzkvl3BtbY1TPHuDGHYk+Zpb7UmTbJxgZ31vGMm5VTT9vJfJ7P2TBtspliNIvqvcYbT+NkifuVrL+VbSKnaWUlN4n+S9Ti9JauPJpoT2tq7XE4pLQUTKJHcB8E8A66gML6jfI44aTb6Z8rVIZS3dvYY1MeVeUe3zQ1S3uVFEZmnbO3UlnQJgCYAfkRwJoBJyGxGhiFREpKRjIcpRmgA87XweSe27YYUItRtbIrk2yTmBXMyyev/iyjqpTh9EUh1fieMQjjsMIvlcwLGKwed5ev/XWWW9G5sNSc5SrtjhRKcfpysdey80eI489zIzd0iP6Cuu03fknEyTqe87Fr26io1yg5TLagRh/oFJ+txjocKo/SuQHKl+hw6nk2QhiqZA7ITXHSRn6PerSbY0kihUx1ldv6+qHA5xzrNG6g2Ta1zZ9vwPXZnH5HBOlVyQq1wDQZiX7wZ97rCE54rOl0CSt2YhCPfe3tqW10geT/Ickue7do1zRHELyaGNtDh6zSvpuMPdKUpTVi4xxk3QdXq/vUpAq2YO4eraWNs90wAxMSalsdzBJF/QMvep4vAqOK5nJuiXU9znY0k+rc/d7szxYr/RHfRzTJ2uZiOimxwrayH5j4ALMMZPMZXkIWrZ3BVzP5YgdLJMlv6vPnN2mtkXww2fUJ9ELCopRlRcrf+3xLju7XOUWiQk+SDJtfoNUbhOTGqAQ6nkRYcjil8GXMFjEw4M2nN4jNhahiC83NQVP1vr3yhDEMr6bPrSCXET5p47wMU8RqW5p907K6vYIMlnNfobcjfpc7gMtwKOc+zdtOdyHURxYhDf2FPjCHY9p25u35Z1SF4bY+GEBGEK2wYkDyP5a2/pVFOy3KRtqwQ6VxXionKLouMao5UQvB+kmJHrNqm3kyRfJbmh85KGUdSasKQNJybX+E2dQykO3VQLUUwJQaQkJ5I8V7GV9tvHSf6V5AdZdAh95/MBHK+ikcfmjIBeI4qL9P1LE56zCb0sjwfS6R4F5+19neQE98yqavUM7jXPY85Y/GiSe5A8UAfq+Rh8Ql6ieIzk3in1fy6INqZZGQfoOx9z77QH+slJgYwvxhGIm7A1FWVV0ujm3vq5uyKrqFbFcDNdcyrrNra/0rLeIrm/Ktzzte5XSZ7urBJZLrpDBtY3RAfolpiJzkMUpjjup/LeYgnrklzozNNKFQ5xkLbrRzEmrcHmZlhoOElEOkJp1t9OrALU+VRepdA7p4LQfJo7fxrJob2qV4TatA7MaiTHk9xElaZBMe/tS3J6DUQRcpb9XZm/zeirCAniZzH4Sx87makRznOUoD/pczNiFsb/BbjPTicqKyRPDSKkcX/FLPkTyg1KbgHYX5u24axes0iCkPYklW0z1FXdro2cq42+guRng/dHKkqINegV7TrIezot/M2U6GFacGuiI6RSQBwLEvwec0g+qqz7eJK7KPEfliKqvJ9k9zoW4DAdu8NTfC/2+0ynNOfiEk15iUGDNRMA/BLApxIeHaF/6wI4mORUAN8TkYdEZI7mNdwAYE8FhmSl5KIFmvT/oQCGVQkWJQW3HgRwJYCDg2DfIgC7A3gDwHoAtgawOaKkoE0BfET/t2sxuoC1cYO/FHQL4FQVMaMBDAewmvZJAAzWvtjvw7R/BQCDAAzRzxZXblLAcrC2862cY5OdIBwxfBIREnpVnUxqIyRm4G2QdgZwH8kjROSP+t7BAP6jRFPJGHmVegg6IIgCgEMBPAPgS1r2qwBOF5FH9Jm3AdzvxmAtncztAXxMP9dDhPyqRshAhKi6KUdb2xFljC0EMF/HbSWtM61/FX0PeYgh84C6kPbmAG5BBFUvVXlf0B0e1gTgSpJlEbkKwDySx2p5eVe3XW3ogtvnDn9riHmK/oVmtCd0AqiIyFu66h5xz64O4FEN3ScRtsEAFyKC5nVqu+chguS9qxPe7sauTZ//QEQ+cPWNUmhAa8wiqSjx3S8i7+dNNzQFOWu4dLAihWoNSXtI/Dhzojjro5TD4vi0tm01RVplAdLYu1/yThwzJ10/C9VMQK8IOm9lmq/FdJT76wlIufpOC1z5Hnn2NsnN8gJ11Wobn+WFolLZVxGBMUs1suqCUvAgAFMUPEJdJaiRS5QBdNQgKjyQpayfBmpJXFF2X9teckrbn9E9OSi8ynr/L4ZDCCyLorMwio7wllocOlZlFd0/AvAv5QZFnY9m/X6NiDzp5i3TJSIdIvJ8VupsVjdxI2Dx9v6v1JGSBztp7+7ivHTvZOQQqeHvOp1yTS73tOTc9h74MlW5bIH1JeMIyVWc6XmO5necpo62d0mO6xGz03nItsho2vXkVXaRxaG6kkY6p1TDCCIhmagYigv3uyXA/Dmh7muSwuk1xoy+oeXeGNw/NcBo1LVPRloDjmognK3iyspTnj17iWvfETna1elxCHEAmXq4hvMqbkfyJyT/pJ8TGxFjcNyhVZOAqK7xonKeZv18Vu99tRYukXUAVm4UjTmtPe/gF1UH2Z/kbQBeA3Cqsway1L1MvTpgpjtYMtFI9T8MBbAtoqSiFtV/FmgfngXwFLo2KmlTWTwNwLQ4q6VO4GxRREoa0xkL4DEAd2q5S1S3WELyGwDuADCF5C0AZjVscxPHIb7dQA7RthzFDUluH2dikdxS3dn3qRzO05/XNaJ5sOEUfXCskeECjVWQ5NdjsBEW77hMn7mqkfpSiHOo1EEQpox+neQa6vevBWbHQJfJotNYHYtIfs0Tgw7ygS5XgjkDcHH1zyZ5AcmN49z9dQKQdtc63lDFUhJAwKMV2U2Sn9d7g5IyzWppyD51IKEqbkJW0fI2bjDEvhoxvEFyy6Bvuyk0Lcya8tcCXZH3avzlBv28l+TDMQm+HUHc5Xck13QBMKlzHgxKeErSyneL+DAHqhmWFpOqRZFZWSm/Vki8hZV3cLb2tW7gKj1IDM+QHOv6tLKaaYwB7y4meatq8VvYZKaMz7qM9oY4k933pPJOqrdJHhxabjVYepsowS0yYFAGCJ4FES9QBPvZ+jm6HqIwijslByQ+aXJuc+bQUIck8l43/1epkxgeDWT6Nk4L9/2YofiIsSme2tBpFIfG3oXk5Y7IPLFdUkuehRt/A8f8OYPZbKbw+ASd7R2Sh9dEFM4mH0ry8TpYvU3SdwMqPsFleTVSgXzZkn4cqmqx3jNW/z7J75ko8+ZnFmSTI5LQctlMsRQhF7pXYxGZiMJx6I84aOLO1SbSje3p7J5YHZr6B+QiCkcMpoSNcxp4Zw26hK36b8ZgJL6mq+sehavf6gaykqOOiipU41z5kx2hGGf4p6GYHdcq1Kv8BXiRQ12sxYjwaadXFDJyB0Nj3V3tPWeNfDxGCfeLs6K4iWF1oavU8TInA2StmoVwmWIRm1Pq2kkHspyTC33WlbGrQy8ZEZ8ZEEJDoWYB5G1jx1mNKB5RB5Mk5HGIswiGsiuD/gspyqS50C3H5IdVFm4pK8cJQbOnkrzJEkX0tw0ZbX+TpqGnsXQbmPuSwq5O3l6X0US1+2e4PnxMAajeZD7Sm2g9jC6zFT5MOZ4niuviJiJGNzlYn39BPZHi/opM3rDkT1XGzbjE3qkEQbcxl8MJWqLIOu65oZrp1B5U4jcSLQchWr/S71dnkE38tuoiP8wFrwokv5BBRJUdO27RAWkl+ZBzHlVM29fV1ysAVDeWzYzS8rxz7sSAcMQ9+xV1lE3Xttt+m61xhKz60mTNL3kqg6gtZ+IQrgM/dgpRh9PGNw+e30SBru9k5BCvquezJVDC5gccZ6yTh7dWsXCsczu5Ms8OVuSJmUEgjSeKguMUzwX40C0ColjDeSO9qJ1Gco3AfN5N5+mumLGZkeJgswU72/mGJK3hm7tVXYnx+J0Y4/odTfLLJC8mead2/Al1/vyd5Fkk9wqRywqrn+cm3FbP3xyXGKWExIADeVFwleNw2+g9415X9jZnSFloG+sYWrsfCqKn9ziC6QzY/s0kv6/jOS/GlLyW5JG6wFrZtY9F2elQfk6PS9WjHEHclEBdnuU/omytNWEAhij7TtrcayyjTcjiyi4F/voCyfUZZZYnobHXd7L1PlfOq7oye1xnyKFThHtwHua8p0niMVSsFykG44eKIB+WoNyeF1NeB3XvrMQxCTxipRTNPlRUnla2tWVcLkZQx0rq2btEO+S9mHGxjw7TJ1wHP6e4g8fVbFpA8nzHHfYJBntyQwM8DQDT6Pe7XP+n62/fTcgVofv9So1pjEwwe5t8KF9dBW2MdgWeQvJb7NrkRLJQ78kZ/Qxxbuzp2uBfqp4wmVGK/jkaB3g9RwDJCOV9n5jjAaHqsBntfQgkH3AENrVHkEP1+ypEE3/8OO/qLIrOFDzHpBgnWlyaoc2n7ex/YBwDyKL4/DNnEk05p5OqksNM9c9crZaIpLR927jEmL7AHRLae7fr53WqK8Ud92DfP2C0f1exiqfS7289R7noR5R4mnOJTkabc9Ya2SwHWMIS08+0yOvMovo/pih7najKk3lSf+uee7xelFJP6hLKJQ5149amIe3/jrEGDFF9dBaO57iDic+/1Bq3KDh4VqN2kW109DK8tta2r8LuO8Z+py9yh2AFj1CRaNfhTmwvilEED8zSJ2fRXKPv7pdrLNg9lT9rnkO9uMo4Z1VWLmTb+X3g4gI7BrrNprWEm5eD2LjDjcmf3f2Pqpm+E6Md9qle1w2rhL6t3DU1mPcuyeFZuWXB4Q2BrhzEHhkDRPkJlt5n+QSFnHUW0LUJ6hMAZuvv27v7bwB4KehbX7ts7O/VTwGwifkjRORVEblZRO4Rkd8AuAxRvuclas0lBaSs3L0R5XheLyLvapnM1Cj34DsKIm30QHoiKCDa+f4BAL9DlN8pOetbmrDrTsjZyN3/t4i0KfC0r+8I+6Qbo40ArK1g2iZnRhYBnADgBQATAZyq/S4mjDUA2E4519bLwm6qA++YJvs7Nbz9aeouJw7rd3dOy8asmi853ecBd//krDIzzXSrETeSqSwn5ycGvphlNjxzz27vPLl7hYqim8P1dIxm580HKcR8v7mGFZt0GRU/CGBbETlURP7lk1f1RNpZNZZvZ160Isoit2tRxgks+D2p9WyqYg3EUHRpgb6sQhWuCQDTtb02YWs4EWJjVFaW/yCAn+rPv9fYht9r2z73U5F6jYgszCougO45CtbA6wCcgSgnoZ7DSywH9BoAB4lIpxvAtRHlPRDRgSNf1u9ZJ0OCNofHPs9OE3vUg8mir9wEwPra3gdU3mbOY2BXZnwRwA6Itkl4T0Sm6kFy1cpagq79LoAoBwQx415WjvdzADsC+CyAi0Vkbwfpq6gJbk6oP9Ul/h1rmlInKtpY/x1BOH0so43I3m+QGPqcc8C87e7vm2R3O7Y6XINBHnM4k+T3strsrl/7uSim95dskWQRBM6jd2JMz6YqFoSZ2NbewSquNnIQwuZ60VAGKF2F5Is1EkXZhVbXdp34qppNDKKWpToIYh83qDPd/Vh7nd1P/LsrpfwfVzNZuexutnH+krlqPi6Tmu8IYlgQuTwkTf9x9e7rdL3t3f1T9PfTWGd6YkiFWznnSGcNk+U3BjupRnRVNaXyC04xne7uH59AEH4wrZyHSX5Ggz6znWv9Y2mrW/9WY9dRB52KLpugHNb8KxcntMUfC7nY+SL2qsahnCfy1y7AeLTGkOZoOds1zDHnBm47ki/F4BDCY5bte5t+/scN3FZuwBrl/exGEFrX3939kxImwQbyUhfz2MLd386JkJ+msG4r53hX54nBM/doHU+HiKhgjHcNPMOfyMCdvBi+PcHx91QtzrnYB01J0sTViYg2CGtyfoSCcyz5TSsG6ecvnH/jO66eRnsNt3bf33bfx1ZRpsQpvrMUt9Gq/b3LlF2dwHKKH2QX/T4LwAUqimx/y6e0npVVQU9qw3D3/1x1qmVRBKkOqk59tkP7Y0nNEwBcr4goZtUjEtmJI4o5APZRf/ghWlErgFcQHSn4OqINrkYj2nluMYC/GkgG0YZjeSyIPNc49/0hAMfo9+10VSRp9/8GcBiiXVcmicjFqoA1a5/2BDAewEgRmR1jKVSciShaHhFlaC8mOR7RRmYEMAdA2n5POzqCmC4i85wVlHRZJvjX1NqwIx49sXXowjhORM5ULlVqFKjDs7pW841nCN6Mc0CVRsZGyg5/McjpPObgabMsrMDB44+AWuDS945idJ6oZYFbW3fXd5pjsrfWdDjQc1wduzHKJbXrK3E6gXNkPeHG55Kc0czfpcAPTFe7IY8uUZWF2/5LNhAi0iYi7wYNHEJyLeeBtMo30FVYQX2HsVaUuksuHlICsJauZCA63Mz2ZRykq7xbH3WFFkTkTUR7ZnWqv/8iAI8qhH8zRDvAAcCW6rjqdPtLlbWckcruCeA9hRPeAOB2AGvr+xeJyNXmqwh8F8bWJ7jxuSnBB5Eksgb1gBiuKWy7p1oO/1Dz7XmNqr1EPXNSn9ujzlB6FgyFT6S9zK3uh5JctoFC90yK0vq+Aobv0X7erv/fqX0NtxS2a4ELvxdS0ExnufGZlYqAjn8/zV9knPn0HoEBODNpXIaJHK8scb3ApKoV+/C64ijPZbQL/F7ub4Rr215BEspOKQ6qonPoHKxOqrfqEGOLNXflDJLrpxCjmazDnclKkufljL+Y2FrI7tsSlhwxlHS+Gn+WuKNKc4gsYfeDzyoutW8XN9h58RWeGK7VYNiQam1j1/5LL7pB/leaTI5xFg1T/MFlro9XKE70j8GfJd++q0Q6Psg1KVYZx++4/na4RVTIoNNZGd9N4aDtLvjXI0cwWiOOTGFTtjIvVWLYVzubRWT4COudJLdNaUsrg7MmHYzu2IBlfqHKBJlyV3QicZLrzzYJ71kq4wMxxFmo4gleTd3V1t/rMyqTEpNItVCz3c5ntB/EHZobs1leH0StBHF2Ru/l2zksDA+MPSVGTDUpp/iFOqBeUOznw8pFjrABVWKZ7pxnr6hrO8uxA0YYY13G1/Hs2mzUEnA3YNd2iBfpOy05ZP+5gSWwdQbvpCeGnzsE1SerifmeJoizcuRa5kFh04FIbbU3q0n4VIZyNndt/VKQQ3l+FvnsOMQoZ5Ze7oiy6ExTu87MWLYR92a6UDqCDLViRjFxrhNVn9TfWpw5LOyJg1lTCCLrnpVZNzrtDOIPls6+M7tnmJdj3Odldm1JNE0Hw4jpFidLmaZgxvS1mV0p/H/33EO/7+/aNSmr70AnbKoTae2MzimTaiJNv/8ihhiWD4jYNeozOdFNWRTIvwTEcBC7b3BazkhUpzktfD01G+3950zvSGPtbiUbQT3jnF9GbKe5urfPsMJt7I4LONd5wWKTIPsq7ryt+cudGGLCte/ktBzSMrPmWBKJlr+LU0RLOcVOhbpTvpZ1YDABP682kG7ybnZy2s7Ltq0Lfqb35pEckyavHRsfo2VZ315UAi2kcQgt47euvu2WOzHEDNbldQJoPHc42g3cug48Uws833wWI11br3AsusN0jRQWHe6N4QnCiPYPeu+5HGP218D62dmJIq+7fJHRueKbK8FYO5Zurdhnck0Cpapch9gwzvKaWgA2IDc2CKl1vRvsEWrxWJn3VJHZYY6r3wbQ+m9HML+Ycbx2C/SZC0MTVf0S82JyZQ39tFGfIoaUFVTL5HX6gXGiohG6iZV9rCv7gARgTTGFIA53Ze4Z9N0Oar87g0eywGh7RPOz2C60BaeTnBAQtR/TNgfF6/HNTmoxTQzl+y1EG5A3If8xRzaAD7ho6okull/PVdT2THEQvqsQnZ1lG6ifoYoiqwTU7BoZtNv6+6KrMy5ETUT5EZtrIK0I4AciskDvdzLapvAnWmbZYUuo77QA2IZdxz7VE7UuNpwgLE6vEc8DEEHIizmJwk6feVzLGwlgV3Ql89RzWQrBKgB+phFKAvgxuk7IGw9gP0VFNyVEEhfG/FZhdKSyudLnp7TDxuPb+n4zorO6/hRM7kRta4gZsTPLBMD+6DpcrbZB0TSBnuAQ0IEsap7AJAXFFB16p1ooWxAdJGYrbGNEp83VA/sPgT8VAAcpxlEQHSXwsFt9xxp0PYEgXnOT2uLC52ujCyqfqJgqZGBnAFtqOQLgTCVO38fBKRNtz60eVS+Vns5mL9RBcZY8MhVRbsXLugrE4RaYEs9vE5GOAPlUbmDfKtqeHximA8D57t72ACZY7kTM+7OU0AFgHff7cMch2qq04QhHOC8BuEHRUH5s5qTMg+XaPukWIfskQShRlLSR9yM6aORCRNAtw1oa+y65P+MQKzlqr/RA34pa92SSds7lP9wEFADsEzMONuDtrl3rx9wHonM+l5HVuliGIDoQ1lb6FZqsVHTiRwBMRXR2aJOOnRFB2XHMy5P8Qn2KIBynKIjIfBE5DhHwdQoinGG7dqgp+CvpADGN9TZAlygrSz5I2/o+IlSSDeYeKQTpD6f1G3qt4r5PjyESG9OtEGEuDd11na9L+15QLnkookTrFldvUTnchSJya4i6AtCatJsOq+z1VU3WogFEYdRe0CMCn9TGjUEEc9sUETC3oqLleRF5TblLGRHaGA3SH8JJJSKQ8Fm6Qm9UVk4AnyA5Uo+fDoGtSUdAevGxKEXu746uFMMXATzn9JBwMT2q7ujvIwIlr6bv/F5E/hBnYYjIkpQ+N6HrUNjeJwhH8WVtfAFAWUTeQAQrn5bA8mxw7ld53NpAxRJuQsY4pXeaTuRKiCDyGzkx4lfgEgDvqULnx2n9KhzWFofHUdzrdIByzGIqiMjLAI7UeM4qinY3EZTn/E0TzctHZMRxCzuk1aGUlznu0IN3ESXn3l+vaZVi+t1p+0Xo5L/sWP3WfmU7LtHmONdgV+Ygx/rbvMhwk9eECDxr1zNpHNCIQgmmzTjW8tjfokdj5g6lXHJ/5ZDi9f9z0LhtCBBwmguMI+oKfcpN0PqhHuBQ0bZtwTB2bdBqRPYelj2V2Or7KKIscPv9gWrKs42VOeqy+g36FUHkUEqLInKLKl5N6J4eX+tVUjFxhYg8qNyh7ExKuz6eohgaQQxBVyJMi+MgSxL0hw30HSOABTkdSMtt15u+siGX+QKOVoW0uU6i6NQyHlMHVJjF9Yj7btC3ggPBhPtArgzAMJyDHcFVguebgveKqkPNjCG6Pnn1CYJw7vC5ago+hq4En3KOgbTnm1VuTxaRRa4OK+d9N0HrABjsxFlZRNqVXXc4vWGh/rbUKSUi7wa7xth7m7o2zRGRBRnS85JlXy/utdlnQqlO255N8lMAznOePjjNuRAoZ+bIKToC/yuAo0RkfkJO5RKnwK4O4FqSL+jqL7h72zrfw8Uk5wHYTX9bQ1PvCs6CsRzLvZ27eq5rd7nWBaO+hdLy0CuW6xXkYn5KkUtZQ+yP0O3pnLJJx3AF4vikljzZY1lC9O0+s4z1H+Za6A1OIX2UKAQazNH/J6go2QHAemoZCKJYw8MAHgVwG4D73GZfscqZ+QI0j/OkHu7KreoeL6H+s78zj1099Uh/4Bae5SuxjDAxIiLvxU14NXmshPMdFQEtzsNnCmizfvfxF7tncZJCIMLs/fmIthU4U0Ta650kxXIW7MD5mP4M0j61rZAcIoEwCs4T140AnP+iknXgq01SyKX8O+4z1GeK4cTVSwxaxlAAHxGRGa7uFvWrLFYfyWg1k0si8l4j6u0vOoY/lU5WkD4V0v5P0IOabU8Ld2809aC8WsdG8CG6bNU7dn8gov0gWtRKENTvOvcAm0t1BVflRllWswsglhutO3woL5fmJuw6oKwnr5uZ98CSBnDPFV6HaLQGrujl2eqB7GiQg87HYYwDDQIwVkReybM77sCVzxavyx53UPof9gKHuLE3OcQK64eoMqFNql23NYBTfAbRXlRUj6JhQc2SMbe5ucOHYNm9qc0kbVeOMF7Nz7cA/Eo3Hx+Q7/1EwRy4gqtpgDA4ChFmclAg/yXgAHaPgTUxVO9bLGOIfn9FROYNkFg/svtJnq7JvH6/rFLMFs7hofb+L24XnJJuxh67R+WADtHHiEEjq+MQHVmU178Qjh1j/jcuMxdRzsl7QDd4Xp+9Ch9GBqGf89GViseMi8f/hb/H/V/ub4vuQ6lYOS7xeQCnA9jQjYXXHczqWKx6QZtbSAXVH1ZFd/ym+RqeA3CMwvf6jQ/iQ6tpO9OziChf00A2SwNl6NpGuV2JoxPdo5yDEcH5/WVc4U0DzQ6YnP1Mueyv5Q9wiJ7zR9g4nIIoqadVTdEh+ieIHFNQLlFB5PJejCjpZ5FyjMsRZZlbotIAZ+inRGHu7PPrdFVv2l85wworAmqZDIevGOJ2x1+S4pfwm4wv9lsY9Sefw8CVQd7roWjTg/2eym4j1nLMPlA9cwTBwNVniGIdkrdmEBGzSR63InGGgQBPgo9Cv+8I4IuIzsWy87XaEGWQ3wPgbyIyc0XCOgwQRDKnWAqbV0vE/A1lvzdDNZR3f7v+H4BuAUkEujQ+AAAAAElFTkSuQmCC" alt="Brain and Mind"></div>
    <div>
      <div class="brand-name">Brain &amp; Mind Academy</div>
      <div class="series-name">Sopaan <span style="font-weight:400;font-size:14px;color:#CFD7EA;">Practice Series</span></div>
    </div>
  </div>
  <div class="chapter-eyebrow">Functions 11 · Chapter 2 Review</div>
  <div class="chapter-title">Equivalent Algebraic Expressions</div>
  <div class="chapter-sub">Theory Notes · Chapter Review Practice · Test</div><div class="chapter-credit">Theory · Step-by-step practice · Learning assessment</div>
  <div class="chapter-progress">
    <div class="cp-track"><div class="cp-fill" id="cpFill"></div></div>
    <div class="cp-label" id="cpLabel">0% complete</div>
  </div>
  <div class="who-row"><button class="mode-pill" id="modePill" hidden>Choose a mode</button><span class="who" id="whoBar" hidden></span></div>
</header>

<nav class="tabbar"><div class="tabbar-inner" id="tabbar"></div></nav>
<div class="sec-sub" id="secSub"></div><div class="slide-progress"><div class="sp-track"><div class="sp-fill" id="spFill"></div></div><div class="sp-label" id="spLabel">Question 1 of 49</div></div>
<div class="wrap" id="wrap"></div>
<footer class="brandfoot">Brain &amp; Mind Academy · Sopaan Practice Series<br>Questions: Chapter 2 Review, <i>Functions 11</i> (Nelson Education), pp. 131–133. Theory notes, step-by-step solutions and test written by Brain &amp; Mind Academy.</footer>

<div class="navbar"><div class="navbar-inner" id="navbarInner"></div></div>
<button class="fab" id="paletteFab"><span>Questions</span><span class="fab-badge" id="fabBadge">0/49</span></button>

<div class="overlay" id="overlay">
  <div class="palette" role="dialog" aria-label="Question palette">
    <div class="palette-head"><h2 id="paletteTitle">Question palette</h2><button class="palette-close" id="paletteClose">&times;</button></div>
    <div class="palette-legend">
      <span><i class="dot current"></i>Current</span><span><i class="dot correct"></i>Correct</span>
      <span><i class="dot revealed"></i>Revealed</span><span><i class="dot skipped"></i>Skipped</span>
      <span><i class="dot locked"></i>Locked</span>
    </div>
    <div class="chip-grid" id="paletteBody"></div>
  </div>
</div>
<div class="toast" id="toast"></div>

<script>
(function(){
"use strict";

/* ================= audio ================= */
var audioCtx=null;
function ensureAudio(){ if(!audioCtx){ try{ audioCtx=new (window.AudioContext||window.webkitAudioContext)(); }catch(e){} } return audioCtx; }
function playTone(freqs,dur,type){
  var ctx=ensureAudio(); if(!ctx) return;
  try{
    var t0=ctx.currentTime;
    freqs.forEach(function(f,i){
      var o=ctx.createOscillator(), g=ctx.createGain();
      o.type=type||'sine'; o.frequency.value=f;
      var start=t0+i*dur;
      g.gain.setValueAtTime(0.0001,start);
      g.gain.exponentialRampToValueAtTime(0.16,start+0.02);
      g.gain.exponentialRampToValueAtTime(0.0001,start+dur);
      o.connect(g); g.connect(ctx.destination);
      o.start(start); o.stop(start+dur+0.02);
    });
  }catch(e){}
}
function playSuccess(){ playTone([523.25,659.25,783.99],0.11,'sine'); }
function playWrong(){ playTone([220,185],0.14,'square'); }
function playReveal(){ playTone([300,220],0.16,'triangle'); }

/* ================= helpers ================= */
function norm(s){
  return String(s===undefined||s===null?'':s).trim().toLowerCase().replace(/\s+/g,'')
    .replace(/[×∗*·]/g,'x').replace(/÷/g,'/').replace(/–|—|−/g,'-')
    .replace(/[²]/g,'^2').replace(/[³]/g,'^3').replace(/[⁴]/g,'^4').replace(/[⁵]/g,'^5')
    .replace(/[⁶]/g,'^6').replace(/[⁷]/g,'^7').replace(/[⁸]/g,'^8').replace(/[⁹]/g,'^9')
    .replace(/\^/g,'');
}
function parseNum(s){
  if(s===undefined||s===null) return null;
  var t=String(s).trim().replace(/,/g,'').replace(/[−–—]/g,'-').replace(/\s+/g,''); if(t==='') return null;
  var neg=false; if(t[0]==='-'){neg=true;t=t.slice(1);}
  var m=t.match(/^(\d+)\/(\d+)$/);
  if(m){ var v=parseInt(m[1],10)/parseInt(m[2],10); return neg?-v:v; }
  if(/^\d+(\.\d+)?$/.test(t)){ var v2=parseFloat(t); return neg?-v2:v2; }
  return null;
}
/* ---- expression checker: compares answers like (P-2w)/2 and P/2-w at random values ---- */
function exprPrep(s){
  return String(s).toLowerCase().replace(/\s+/g,'').replace(/^[a-z]\(x\)=/i,'').replace(/^[a-z]=/i,'').replace(/[×∗·]/g,'*').replace(/÷/g,'/').replace(/[−–—]/g,'-')
    .replace(/²/g,'^2').replace(/³/g,'^3').replace(/⁴/g,'^4').replace(/⁵/g,'^5').replace(/⁶/g,'^6').replace(/⁷/g,'^7').replace(/⁸/g,'^8').replace(/⁹/g,'^9').replace(/π/g,'#').replace(/pi/gi,'#').replace(/½/g,'(1/2)');
}
function exprCompile(src){
  var s=exprPrep(src), i=0, toks=[], absDepth=0;
  while(i<s.length){
    var ch=s[i];
    if(/[0-9.]/.test(ch)){ var j=i; while(j<s.length && /[0-9.]/.test(s[j])) j++; toks.push({k:'n',v:parseFloat(s.slice(i,j))}); i=j; continue; }
    if(/[a-zA-Z#]/.test(ch)){ toks.push({k:'v',v:ch}); i++; continue; }
    if(ch==='|'){ var pv=toks[toks.length-1]; var opn=(absDepth===0)||!pv||('+-*/^(['.indexOf(pv.k)>=0); if(opn){ absDepth++; toks.push({k:'['}); } else { absDepth--; toks.push({k:']'}); } i++; continue; }
    if('+-*/^()'.indexOf(ch)>=0){ toks.push({k:ch}); i++; continue; }
    return null;
  }
  var out=[];
  for(var t=0;t<toks.length;t++){
    var a=toks[t], b=out[out.length-1];
    if(b && (b.k==='n'||b.k==='v'||b.k===')'||b.k===']') && (a.k==='n'||a.k==='v'||a.k==='('||a.k==='[')) out.push({k:'&'});
    out.push(a);
  }
  var p=0;
  function peek(){ return out[p]; }
  function parseE(){ var n=parseT(); while(peek() && (peek().k==='+'||peek().k==='-')){ var o=out[p++].k, r=parseT(); n=(function(l,r,o){return function(e){ return o==='+'?l(e)+r(e):l(e)-r(e); };})(n,r,o); } return n; }
  function parseI(){ var n=parseU(); while(peek() && peek().k==='&'){ p++; var r=parseP(); n=(function(l,r){return function(e){ return l(e)*r(e); };})(n,r); } return n; }
  function parseT(){ var n=parseI(); while(peek() && (peek().k==='*'||peek().k==='/')){ var o=out[p++].k, r=parseI(); n=(function(l,r,o){return function(e){ return o==='*'?l(e)*r(e):l(e)/r(e); };})(n,r,o); } return n; }
  function parseU(){ if(peek() && peek().k==='-'){ p++; var u=parseU(); return function(e){ return -u(e); }; } if(peek() && peek().k==='+'){ p++; return parseU(); } return parseP(); }
  function parseP(){ var b=parseA(); if(peek() && peek().k==='^'){ p++; var x=parseU(); return function(e){ return Math.pow(b(e),x(e)); }; } return b; }
  function parseA(){
    var t=out[p++]; if(!t) throw 0;
    if(t.k==='n') return function(){ return t.v; };
    if(t.k==='v') return t.v==='#' ? function(){ return Math.PI; } : function(e){ return e[t.v]; };
    if(t.k==='('){ var n=parseE(); if(!peek()||peek().k!==')') throw 0; p++; return n; }
    if(t.k==='['){ var m=parseE(); if(!peek()||peek().k!==']') throw 0; p++; return function(e){ return Math.abs(m(e)); }; }
    throw 0;
  }
  try{ var f=parseE(); if(p!==out.length) return null; return f; }catch(e){ return null; }
}
function exprEqual(input,answer){
  var f=exprCompile(input), g=exprCompile(answer); if(!f||!g) return false;
  var hits=0;
  for(var trial=0;trial<8;trial++){
    var env={}; 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(function(c){ env[c]=1.3+Math.random()*4.1; });
    var x=f(env), y=g(env);
    if(!isFinite(x)||!isFinite(y)) continue;
    if(Math.abs(x-y)>1e-7*Math.max(1,Math.abs(x),Math.abs(y))) return false;
    hits++;
  }
  return hits>=3;
}
function wordsNorm(s){ return String(s||'').toLowerCase().replace(/\band\b/g,' ').replace(/[^a-z]/g,''); }
function listNorm(s){ return (String(s||'').replace(/[−–—]/g,'-').replace(/(\d) (?=\d{3}\b)/g,'$1').match(/-?\d+(\.\d+)?/g)||[]).join(','); }
function powNorm(s){ return String(s||'').toLowerCase().replace(/\s+/g,'').replace(/[×∗*·.]/g,'x').replace(/[⁰¹²³⁴⁵⁶⁷⁸⁹]+/g,function(m){ return '^'+m.split('').map(function(c){ return '⁰¹²³⁴⁵⁶⁷⁸⁹'.indexOf(c); }).join(''); }).replace(/\^1(?!\d)/g,''); }
function fr(s){ return String(s).replace(/\{(\d+) (\d+)\/(\d+)\}/g,'<span class="mx">$1<span class="fq"><span>$2</span><span>$3</span></span></span>').replace(/\{(\d+)\/(\d+)\}/g,'<span class="fq"><span>$1</span><span>$2</span></span>'); }
function gcdI(a,b){ a=Math.abs(a); b=Math.abs(b); while(b){ var t=a%b; a=b; b=t; } return a; }
function fracParse(s){ s=String(s===undefined||s===null?'':s).trim().replace(/[\u2044\u2215\u00f7]/g,'/').replace(/\s+/g,' ').replace(/\s*\/\s*/g,'/'); var m;
  if((m=s.match(/^(-?\d+)$/))) return {v:+m[1],form:'int',n:+m[1],d:1};
  if((m=s.match(/^(-?\d+)\/(\d+)$/))){ if(+m[2]===0) return null; return {v:m[1]/m[2],form:'frac',n:+m[1],d:+m[2]}; }
  if((m=s.match(/^(-?)(\d+)(?: |\+)(\d+)\/(\d+)$/))){ if(+m[4]===0) return null; var sg=m[1]?-1:1; return {v:sg*(+m[2]+m[3]/m[4]),form:'mixed',w:sg*m[2],n:+m[3],d:+m[4]}; }
  if((m=s.match(/^-?\d*\.\d+$/))) return {v:parseFloat(s),form:'dec'};
  return null; }
function fracOK(mode,input,answer){
  if(mode==='flist'){ var A=String(input).split(/[,;]/).map(function(x){return x.trim();}).filter(Boolean), K=String(answer).split(/[,;]/).map(function(x){return x.trim();});
    if(A.length!==K.length) return false; return A.every(function(x,i){ var a=fracParse(x), k=fracParse(K[i]); return a&&k&&Math.abs(a.v-k.v)<1e-9; }); }
  var a=fracParse(input), k=fracParse(answer); if(!a||!k) return false;
  var same=Math.abs(a.v-k.v)<1e-9; if(!same) return false;
  if(mode==='fv') return true;
  if(mode==='dec') return a.form==='dec'||a.form==='int';
  if(mode==='fe') return (a.form==='frac'&&k.form==='frac'&&a.n===k.n&&a.d===k.d)||(a.form==='int'&&k.form==='int');
  if(mode==='fi') return a.form==='frac'||(a.form==='int'&&k.form==='int');
  if(mode==='fl') return a.form==='int'||(a.form==='frac'&&gcdI(a.n,a.d)===1)||(a.form==='mixed'&&a.n<a.d&&gcdI(a.n,a.d)===1);
  if(mode==='fm') return a.form==='int'||(a.form==='mixed'&&a.n>0&&a.n<a.d&&gcdI(a.n,a.d)===1);
  return false; }
function answerMatches(input,answer,accept,expr){
  if(expr==='dec'||expr==='fv'||expr==='fe'||expr==='fl'||expr==='fm'||expr==='fi'||expr==='flist'){ if(input===undefined||input===null||String(input).trim()==='') return false; return fracOK(expr,input,answer); }
  if(input===undefined||input===null||String(input).trim()==='') return false;
  if(expr==='words'){ return [answer].concat(accept||[]).some(function(a){ if(/\d/.test(a)) return norm(a)===norm(input); var w=wordsNorm(a); return w!=='' && w===wordsNorm(input); }); }
  if(expr==='list'){ return [answer].concat(accept||[]).some(function(a){ return listNorm(a)===listNorm(input); }); }
  if(expr==='pow'){ return [answer].concat(accept||[]).some(function(a){ return powNorm(a)===powNorm(input); }); }
  if(expr==='time'){ var tn=function(x){ var t=String(x).toLowerCase().replace(/[\s.]/g,'').replace(/[:h]/g,''); if(/^\d{3}(am|pm)?$/.test(t)) t='0'+t; return t; }; return [answer].concat(accept||[]).some(function(a){ return tn(a)===tn(input); }); }
  if(expr==='glist'){ var gn=function(x){ return String(x).toUpperCase().split(/[\s,;]+/).filter(Boolean).sort().join(','); }; return [answer].concat(accept||[]).some(function(a){ return gn(a)===gn(input); }); }
  if(expr==='coord'){ var cn=function(x){ return String(x).replace(/[\u2212\u2013\u2014]/g,'-').replace(/[\s()\[\]]/g,''); }; return [answer].concat(accept||[]).some(function(a){ return cn(a)===cn(input); }); }
  if(expr==='dlist'){ var dn=function(x){ return (String(x).replace(/[−–—]/g,'-').match(/-?\d*\.?\d+/g)||[]).map(Number).join(','); }; return [answer].concat(accept||[]).some(function(a){ return dn(a)===dn(input); }); }
  if(expr==='set'){ var sn=function(x){ return (String(x).match(/-?\d+/g)||[]).map(Number).sort(function(a,b){return a-b;}).join(','); }; return [answer].concat(accept||[]).some(function(a){ return sn(a)===sn(input); }); }
  if(expr==='primes'){ var pn=function(x){ var t=powNorm(x).replace(/[^0-9x^]/g,''); var out=[]; t.split('x').forEach(function(tok){ if(!tok) return; var m=tok.split('^'); var b=+m[0], e=m[1]?+m[1]:1; for(var i=0;i<e;i++) out.push(b); }); return out.sort(function(a,b){return a-b;}).join(','); }; return [answer].concat(accept||[]).some(function(a){ return pn(a)===pn(input); }); }
  if(expr==='angle'){ var an=function(x){ return String(x).toUpperCase().replace(/[^A-Z]/g,''); }; var k=an(answer), v=an(input); return v===k || v===k.split('').reverse().join(''); }
  if(expr==='trans'){ var tv=function(x){ var s=String(x).toLowerCase().replace(/[−–—]/g,'-').replace(/\b(units?|squares?|and|then|steps?|to|the|a)\b/g,' ').replace(/[,;.]/g,' '); var re=/(\d+)\s*(right|left|up|down|r|l|u|d)\b/g, m, dx=0, dy=0, n=0; while((m=re.exec(s))){ var v=+m[1], d=m[2][0]; if(d==='r')dx+=v; else if(d==='l')dx-=v; else if(d==='u')dy+=v; else dy-=v; n++; } if(!n||s.replace(re,'').replace(/\s+/g,'')!=='') return null; return dx+','+dy; }; var ti=tv(input); return ti!==null && [answer].concat(accept||[]).some(function(a){ return tv(a)===ti; }); }
  if(expr==='rot'){ var rv=function(x){ var s=String(x).toLowerCase().replace(/quarter[\s-]*turn/g,'90').replace(/half[\s-]*turn/g,'180').replace(/three[\s-]*quarter[\s-]*turn/g,'270'); var m=s.match(/\b(90|180|270)\b/); if(!m) return null; var a=+m[1]; if(a===180) return '180'; var dir=/anti|counter|acw|ccw/.test(s)?-1:(/clockwise|\bcw\b/.test(s)?1:0); if(!dir) return null; return String(((a*dir)%360+360)%360); }; var ri=rv(input); return ri!==null && ri===rv(answer); }
  if(expr==='expanded'){ var f=function(x){ return String(x).replace(/\s+/g,'').replace(/,/g,''); }; return [answer].concat(accept||[]).some(function(a){ return f(a)===f(input); }); }
  if(expr===true && input!==undefined && input!==null && String(input).trim()!==''){
    if(exprEqual(input,answer)) return true;
    var alt=String(input).replace(/\/\s*(\d+(?:\.\d+)?)\s*([a-zA-Z(])/g,'/$1*$2'); if(alt!==String(input) && exprEqual(alt,answer)) return true;
    return (accept||[]).some(function(a){ return exprEqual(input,a); });
  }
  if(input===undefined||input===null||String(input).trim()==='') return false;
  var n1=parseNum(input), n2=parseNum(answer);
  if(n1!==null && n2!==null){ if(Math.abs(n1-n2)<1e-3) return true; return (accept||[]).some(function(a){ var n3=parseNum(a); return n3!==null && Math.abs(n1-n3)<1e-3; }); }
  var cands=[answer].concat(accept||[]); var ni=norm(input);
  for(var i=0;i<cands.length;i++){ if(norm(cands[i])===ni) return true; }
  return false;
}
function esc(s){ return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;'); }

/* ================= DATA ================= */
var AR_OPTIONS = ["Both A and R are true, and R is the correct explanation of A","Both A and R are true, but R is NOT the correct explanation of A","A is true but R is false","A is false but R is true"];
var THEORY = "<div class=\"hub\"><div class=\"hub-card\"><h3>📖 Theory notes</h3><p>Notes for every lesson in the chapter: rules in tables, common-mistake boxes and worked examples with every line shown.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-jump=\"n21\">2.1 · Adding and subtracting polynomials</button><button class=\"hub-btn\" data-jump=\"n22\">2.2 · Multiplying polynomials</button><button class=\"hub-btn\" data-jump=\"n23\">2.3 · Simplifying and factoring polynomials</button><button class=\"hub-btn\" data-jump=\"n24\">2.4 · Simplifying rational functions</button><button class=\"hub-btn\" data-jump=\"n26\">2.6 · Multiplying and dividing rational expressions</button><button class=\"hub-btn\" data-jump=\"n27\">2.7 · Adding and subtracting rational expressions</button><button class=\"hub-btn\" data-jump=\"nPS\">PS · Problem solving</button></div></div><div class=\"hub-card\"><h3>🎯 Chapter review practice</h3><p>Every Chapter Review question from pages 132–133 (Q1–Q17, all parts), organised by lesson and tagged with its number, plus a few extra questions. Multiple-choice items alternate with step-by-step fill-ins.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-go=\"s1\">2.1 · Adding and subtracting polynomials</button><button class=\"hub-btn\" data-go=\"s2\">2.2 · Multiplying polynomials</button><button class=\"hub-btn\" data-go=\"s3\">2.3 · Simplifying and factoring polynomials</button><button class=\"hub-btn\" data-go=\"s4\">2.4 · Simplifying rational functions</button><button class=\"hub-btn\" data-go=\"s5\">2.6 · Multiplying and dividing rational expressions</button><button class=\"hub-btn\" data-go=\"s6\">2.7 · Adding and subtracting rational expressions</button><button class=\"hub-btn\" data-go=\"s7\">PS · Problem solving</button></div></div><div class=\"hub-card\"><h3>📝 Test</h3><p>Four short assessments with new questions from every lesson, one per skill area. Take them in Quiz mode and open the report to see your results.</p><div class=\"hub-btns\"><button class=\"hub-btn\" data-go=\"s8\">A · Knowing and understanding</button><button class=\"hub-btn\" data-go=\"s9\">B · Investigating patterns</button><button class=\"hub-btn\" data-go=\"s10\">C · Communicating</button><button class=\"hub-btn\" data-go=\"s11\">D · Applying mathematics in real-life contexts</button><button class=\"hub-btn primary\" data-go=\"report\">📊 View my report</button></div></div></div><section class=\"note\" id=\"nintro\"><h2>About this review</h2><p>Two algebraic expressions are <b>equivalent</b> if they give the same value for every value of the variables (where both are defined). This chapter is about turning an expression into a simpler, equivalent one: collecting like terms, expanding, factoring, and simplifying <b>rational expressions</b> (fractions with polynomials on top and bottom) while keeping track of the values the variable may not take.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Tab</th><th>Lesson</th><th>Book questions</th><th>Learning target</th></tr><tr><td>1</td><td>2.1</td><td>Q1, Q2, Q3</td><td>I can add and subtract polynomials by removing brackets and collecting like terms, and I can test whether two polynomials are equivalent.</td></tr><tr><td>2</td><td>2.2</td><td>Q4, Q5</td><td>I can expand and simplify products of polynomials, including powers such as (a + b)² and (a + b)³.</td></tr><tr><td>3</td><td>2.3</td><td>Q6, Q7, Q8</td><td>I can simplify polynomial expressions and factor them fully: common factors, grouping, trinomials, perfect squares and differences of squares.</td></tr><tr><td>4</td><td>2.4</td><td>Q9, Q10, Q11</td><td>I can simplify a rational expression by dividing out common factors, and state its restrictions.</td></tr><tr><td>5</td><td>2.6</td><td>Q12, Q13, Q15(d), (e)</td><td>I can multiply and divide rational expressions, simplify, and state every restriction, including those from the divisor.</td></tr><tr><td>6</td><td>2.7</td><td>Q14, Q15(a), (b), (c), (f)</td><td>I can add and subtract rational expressions using the lowest common denominator, simplify, and state the restrictions.</td></tr><tr><td>7</td><td>Problem solving</td><td>Q16, Q17</td><td>I can model a situation with rational expressions, simplify and solve, and judge whether the answer makes sense.</td></tr></table></div><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Assessment</th><th>Skill area</th><th>What it checks</th></tr><tr><td>A</td><td>Knowing and understanding</td><td>Simplifying, expanding, factoring and stating restrictions correctly.</td></tr><tr><td>B</td><td>Investigating patterns</td><td>Testing equivalence, product patterns, telescoping sums.</td></tr><tr><td>C</td><td>Communicating</td><td>Vocabulary, explaining why, spotting and correcting errors.</td></tr><tr><td>D</td><td>Applying mathematics in real-life contexts</td><td>Volume, travel time, shared cost, work rate and weighted-mark problems.</td></tr></table></div><h4>Typing answers</h4><div class=\"tscroll\"><table class=\"ttab\"><tr><th>You want</th><th>Type</th></tr><tr><td>x², 3y⁴</td><td class=\"mono\">x^2, 3y^4</td></tr><tr><td>a product</td><td class=\"mono\">6m^2n^2(2n+3m)</td></tr><tr><td>a rational expression</td><td class=\"mono\">(2x+1)/(2x+3)</td></tr><tr><td>a denominator that is a product</td><td class=\"mono\">5/((x-2)(x-3)(x+3))</td></tr><tr><td>π</td><td class=\"mono\">pi</td></tr><tr><td>restrictions</td><td class=\"mono\">-2, -1, 1</td></tr></table></div><p>Always put a whole numerator or denominator in brackets: <span class=\"mono\">x+1/x-1</span> means x + {1/x} − 1, not the fraction. In restriction lists type the numbers in increasing order, and type a fraction such as {3/2} as the decimal <span class=\"mono\">1.5</span>. Expression answers are checked by value, so any correct equivalent form is accepted; when a question asks for factors, the separate factor steps are what show that you factored. ✏️ opens a scratchpad for rough work.</p></section><section class=\"note\" id=\"n21\"><h2>2.1 · Adding and subtracting polynomials</h2><p class=\"lt\"><b>Learning target:</b> I can add and subtract polynomials by removing brackets and collecting like terms, and I can test whether two polynomials are equivalent.</p><h4>Vocabulary</h4><ul><li>A <b>polynomial</b> is a sum of terms such as 7x², −2x and 1, where the exponents are whole numbers.</li><li><b>Like terms</b> have exactly the same variable part: 7x² and −4x² are like terms; 7x² and 7x are not; 4ab and −2ba are.</li><li>The <b>degree</b> of a polynomial in one variable is its highest exponent: 12x² − 12x + 13 has degree 2.</li></ul><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Operation</th><th>What to do</th><th>Example</th></tr><tr><td>Adding</td><td>Drop the brackets; signs stay the same. Collect like terms.</td><td class=\"mono\">(3x + 2) + (x − 5) = 4x − 3</td></tr><tr><td>Subtracting</td><td>Change the sign of <b>every</b> term in the bracket being subtracted, then collect.</td><td class=\"mono\">(3x + 2) − (x − 5) = 3x + 2 − x + 5 = 2x + 7</td></tr><tr><td>Collecting</td><td>Add the coefficients of like terms; the variable part does not change.</td><td class=\"mono\">7x² + 9x² − 4x² = 12x²</td></tr></table></div><div class=\"ex\"><div class=\"exh\">Worked example 1 · Adding</div><div class=\"exl\">Simplify (4x² − 3x + 5) + (2x² + 7x − 9).<br>= 4x² + 2x² − 3x + 7x + 5 − 9<br>= <b>6x² + 4x − 4</b></div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Subtracting, two variables</div><div class=\"exl\">Simplify (5a² − 2ab + b²) − (3a² − 4ab − 2b²).<br>= 5a² − 2ab + b² − 3a² + 4ab + 2b²   (every sign in the second bracket changes)<br>= <b>2a² + 2ab + 3b²</b></div></div><h4>Equivalent polynomials</h4><p>Two polynomials are <b>equivalent</b> when they simplify to the same expression; then they agree for every value of x. To show two polynomials are <b>not</b> equivalent, one value of x where they differ is enough. Agreeing at one or two values does <b>not</b> prove equivalence.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>To show …</th><th>Do this</th></tr><tr><td>f and g are equivalent</td><td>Simplify both and get the same polynomial.</td></tr><tr><td>f and g are not equivalent</td><td>Find one x with f(x) ≠ g(x) (a counterexample).</td></tr></table></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Equivalent</div><div class=\"exl\">Are f(x) = (x − 1)² + 2x and g(x) = x² + 1 equivalent?<br>f(x) = x² − 2x + 1 + 2x = x² + 1. Both simplify to x² + 1, so <b>yes</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 4 · Agreeing at two points is not enough</div><div class=\"exl\">f(x) = x² and g(x) = 2x: f(0) = 0 = g(0) and f(2) = 4 = g(2).<br>But f(1) = 1 and g(1) = 2, so f and g are <b>not</b> equivalent.<br>The trick: f(x) − g(x) = x(x − 2), which is zero only at x = 0 and x = 2.</div></div><div class=\"keybox\"><b>Common mistake.</b> −(4x² + 6x − 7) is −4x² − 6x + 7, not −4x² + 6x − 7. The minus sign in front of a bracket multiplies <b>every</b> term inside by −1.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s1\">Practise 2.1 →</button></div></section><section class=\"note\" id=\"n22\"><h2>2.2 · Multiplying polynomials</h2><p class=\"lt\"><b>Learning target:</b> I can expand and simplify products of polynomials, including powers such as (a + b)² and (a + b)³.</p><p>To multiply two polynomials, multiply <b>every term</b> of the first by <b>every term</b> of the second (the distributive property), then collect like terms. A trinomial times a trinomial gives 3 × 3 = 9 products before collecting.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Special product</th><th>Expanded</th></tr><tr><td class=\"mono\">(a + b)²</td><td class=\"mono\">a² + 2ab + b²</td></tr><tr><td class=\"mono\">(a − b)²</td><td class=\"mono\">a² − 2ab + b²</td></tr><tr><td class=\"mono\">(a + b)(a − b)</td><td class=\"mono\">a² − b²</td></tr><tr><td class=\"mono\">(a + b)³</td><td class=\"mono\">a³ + 3a²b + 3ab² + b³</td></tr><tr><td class=\"mono\">(a − b)³</td><td class=\"mono\">a³ − 3a²b + 3ab² − b³</td></tr></table></div><p>With a number in front, such as −2(3x − 4)(x + 5), multiply the brackets first and the number last (or the number into one bracket first). Either way, the number multiplies every term.</p><div class=\"ex\"><div class=\"exh\">Worked example 1 · A constant and two binomials</div><div class=\"exl\">Expand −2(3x − 4)(x + 5).<br>(3x − 4)(x + 5) = 3x² + 15x − 4x − 20 = 3x² + 11x − 20<br>× (−2): <b>−6x² − 22x + 40</b></div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Binomial × trinomial</div><div class=\"exl\">Expand (2y + 1)(y² − 3y + 4).<br>2y(y² − 3y + 4) = 2y³ − 6y² + 8y<br>1(y² − 3y + 4) = y² − 3y + 4<br>Sum: <b>2y³ − 5y² + 5y + 4</b></div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · A cube</div><div class=\"exl\">Expand (x − 2)³.<br>(x − 2)² = x² − 4x + 4<br>(x² − 4x + 4)(x − 2) = x³ − 2x² − 4x² + 8x + 4x − 8 = <b>x³ − 6x² + 12x − 8</b></div></div><div class=\"ex\"><div class=\"exh\">Worked example 4 · A formula with changed dimensions</div><div class=\"exl\">A cylinder has V = πr²h. The radius grows by 1 and the height stays h.<br>V = π(r + 1)²h = π(r² + 2r + 1)h = <b>π(r²h + 2rh + h)</b></div></div><div class=\"keybox\"><b>Common mistake.</b> (a + b)² is <b>not</b> a² + b²: the middle term 2ab is missing. Check with a = 3, b = 4: (3 + 4)² = 49, but 3² + 4² = 25. In the same way (a + b)³ ≠ a³ + b³.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s2\">Practise 2.2 →</button></div></section><section class=\"note\" id=\"n23\"><h2>2.3 · Simplifying and factoring polynomials</h2><p class=\"lt\"><b>Learning target:</b> I can simplify polynomial expressions and factor them fully: common factors, grouping, trinomials, perfect squares and differences of squares.</p><h4>Simplifying</h4><p>Work from the <b>innermost</b> bracket outwards, expand each product, then collect like terms. Write each product on its own line to keep the signs straight.</p><div class=\"ex\"><div class=\"exh\">Worked example 1 · Nested brackets</div><div class=\"exl\">Simplify −3x[2x − (x − 4)].<br>Inner bracket: 2x − (x − 4) = 2x − x + 4 = x + 4<br>−3x(x + 4) = <b>−3x² − 12x</b></div></div><h4>Factoring: the reverse of expanding</h4><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Type</th><th>Pattern</th><th>Example</th></tr><tr><td>Common factor</td><td>take out the GCF of all terms</td><td class=\"mono\">8p³q² − 12p²q⁴ = 4p²q²(2p − 3q²)</td></tr><tr><td>Common binomial factor</td><td>a bracket shared by all terms</td><td class=\"mono\">x(y + 2) − 5(y + 2) = (y + 2)(x − 5)</td></tr><tr><td>Simple trinomial x² + bx + c</td><td>two numbers: product c, sum b</td><td class=\"mono\">x² + 7x + 12 = (x + 3)(x + 4)</td></tr><tr><td>Trinomial ax² + bx + c</td><td>two numbers: product ac, sum b; split the middle term and group</td><td class=\"mono\">6x² + 7x − 3 = (3x − 1)(2x + 3)</td></tr><tr><td>Perfect square</td><td class=\"mono\">a² ± 2ab + b² = (a ± b)²</td><td class=\"mono\">4x² + 12x + 9 = (2x + 3)²</td></tr><tr><td>Difference of squares</td><td class=\"mono\">a² − b² = (a − b)(a + b)</td><td class=\"mono\">x² − 49 = (x − 7)(x + 7)</td></tr></table></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Greatest common factor</div><div class=\"exl\">Factor 8p³q² − 12p²q⁴.<br>GCF of 8 and 12 is 4; lowest power of p is p², of q is q². GCF = 4p²q².<br>8p³q² ÷ 4p²q² = 2p and 12p²q⁴ ÷ 4p²q² = 3q², so <b>4p²q²(2p − 3q²)</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Decomposition</div><div class=\"exl\">Factor 6x² + 7x − 3.<br>ac = 6 × (−3) = −18. Two numbers with product −18 and sum 7: 9 and −2.<br>6x² + 9x − 2x − 3 = 3x(2x + 3) − 1(2x + 3) = <b>(3x − 1)(2x + 3)</b></div></div><div class=\"ex\"><div class=\"exh\">Worked example 4 · Factor fully</div><div class=\"exl\">Factor 3x² − 48 and x⁴ − 81.<br>3x² − 48 = 3(x² − 16) = <b>3(x − 4)(x + 4)</b><br>x⁴ − 81 = (x² − 9)(x² + 9) = <b>(x − 3)(x + 3)(x² + 9)</b>   (x² + 9 does not factor)</div></div><div class=\"keybox\"><b>Common mistakes.</b> Take out the common factor <b>first</b> (3x² + 24x + 45 = 3(x² + 8x + 15) before anything else). Keep going until no factor can be factored again: (a² − 4)(a² + 4) is not finished. Check every answer by expanding it.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s3\">Practise 2.3 →</button></div></section><section class=\"note\" id=\"n24\"><h2>2.4 · Simplifying rational functions</h2><p class=\"lt\"><b>Learning target:</b> I can simplify a rational expression by dividing out common factors, and state its restrictions.</p><p>A <b>rational function</b> is a function that can be written as a quotient of two polynomials, such as <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − x − 6</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 9</span></span>. Its domain is all real numbers except the zeros of the denominator, because division by zero is undefined. Those excluded values are the <b>restrictions</b>.</p><div class=\"keybox\"><b>Simplifying a rational expression</b><br>1. Factor the numerator and the denominator completely.<br>2. State the restrictions: every value that makes the <b>original</b> denominator zero.<br>3. Divide out (cancel) common <b>factors</b>.<br>4. Write the simplified form together with the restrictions.</div><div class=\"ex\"><div class=\"exh\">Worked example 1 · Factor, restrict, cancel</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span>f(x) =</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − x − 6</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 9</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x − 3)(x + 2)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 3)(x + 3)</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 3</span></span></span></div></div><br>Restrictions from (x − 3)(x + 3) = 0: <b>x ≠ −3, 3</b>. The simplified form still has x ≠ 3 even though (x − 3) has been cancelled.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · A monomial denominator</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">12p³q − 8p²q²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4p²q</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4p²q(3p − 2q)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4p²q</span></span></span><span>= 3p − 2q</span></div></div><br>Restrictions: 4p²q ≠ 0, so <b>p ≠ 0, q ≠ 0</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Opposite factors</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6 − 3x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 4</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">−3(x − 2)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 2)(x + 2)</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">−3</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 2</span></span></span></div></div><br>Use 6 − 3x = −3(x − 2): the factors (2 − x) and (x − 2) are opposites. Restrictions: <b>x ≠ −2, 2</b>.</div></div><h4>Factors, not terms</h4><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Expression</th><th>Right</th><th>Wrong</th></tr><tr><td class=\"mono\">(x + 5)/5</td><td>cannot be simplified (5 is a term of the top, not a factor)</td><td class=\"mono\">= x + 1  or  = x</td></tr><tr><td class=\"mono\">(5x + 10)/5</td><td class=\"mono\">= 5(x + 2)/5 = x + 2</td><td class=\"mono\">= x + 10</td></tr><tr><td class=\"mono\">(x² + 4)/(x + 2)</td><td>does not factor: no common factor</td><td class=\"mono\">= x + 2</td></tr></table></div><h4>Equivalent rational functions</h4><p>Two rational functions are equivalent only if they have the <b>same simplified form and the same restrictions</b>. For example, <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − 1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span> and x + 1 agree everywhere except at x = 1, where the first is undefined, so they are not equivalent. Having the same restrictions is not enough on its own either: the formulas must also agree.</p><div class=\"keybox\"><b>Common mistake.</b> State the restrictions <b>before</b> cancelling. After cancelling, a zero of the denominator may have disappeared from the formula, but the original expression is still undefined there.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s4\">Practise 2.4 →</button></div></section><section class=\"note\" id=\"n26\"><h2>2.6 · Multiplying and dividing rational expressions</h2><p class=\"lt\"><b>Learning target:</b> I can multiply and divide rational expressions, simplify, and state every restriction, including those from the divisor.</p><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Operation</th><th>Rule</th><th>Restrictions come from …</th></tr><tr><td>Multiply</td><td><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">A</span><span style=\"padding:2px 4px 0;white-space:nowrap\">B</span></span>×<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">C</span><span style=\"padding:2px 4px 0;white-space:nowrap\">D</span></span>=<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">AC</span><span style=\"padding:2px 4px 0;white-space:nowrap\">BD</span></span></td><td>B = 0 and D = 0</td></tr><tr><td>Divide</td><td><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">A</span><span style=\"padding:2px 4px 0;white-space:nowrap\">B</span></span>÷<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">C</span><span style=\"padding:2px 4px 0;white-space:nowrap\">D</span></span>=<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">A</span><span style=\"padding:2px 4px 0;white-space:nowrap\">B</span></span>×<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">D</span><span style=\"padding:2px 4px 0;white-space:nowrap\">C</span></span></td><td>B = 0, D = 0 <b>and C = 0</b> (you cannot divide by zero, and C becomes a denominator)</td></tr></table></div><div class=\"keybox\"><b>Method</b><br>1. Rewrite each division as multiplication by the reciprocal of the divisor.<br>2. Factor every numerator and denominator.<br>3. List the restrictions from every denominator <b>and</b> every divisor’s numerator.<br>4. Divide out common factors, then multiply what is left.</div><div class=\"ex\"><div class=\"exh\">Worked example 1 · Monomials</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3a</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4b</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">8b²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">9a²</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">24ab²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">36a²b</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2b</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3a</span></span></span></div></div><br>Restrictions: <b>a ≠ 0, b ≠ 0</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Division with trinomials</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − 4</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 3</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x − 2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 6x + 9</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x − 2)(x + 2)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 3</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x + 3)²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 2</span></span></span></div></div><br>= <b>(x + 2)(x + 3)</b>. Restrictions: x + 3 ≠ 0 and the divisor’s numerator x − 2 ≠ 0, so <b>x ≠ −3, 2</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Multiplying</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − 1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 2x + 1</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x − 1)(x + 1) · 4x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x(x + 1)²</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2x(x − 1)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 1</span></span></span></div></div><br>Restrictions: <b>x ≠ −1, 0</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 4 · Mixed operations (from the chapter FAQ idea)</div><div class=\"exl\">Do ÷ and × before + and −, exactly as with numbers. In <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 1)²</span></span>÷<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 1</span></span>+<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">7</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x − 2</span></span> the division is done first: it gives <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x(x + 1)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2(x − 1)</span></span>, and then adding <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">7</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2(x − 1)</span></span> gives <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² + x + 7</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2(x − 1)</span></span>, with x ≠ −1, 0, 1 (the 0 comes from the divisor’s numerator 4x).</div></div><div class=\"keybox\"><b>Common mistake.</b> Forgetting the restrictions from the divisor’s numerator. In <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 4</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span>÷<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 4</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 2</span></span> the answer <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span> needs x ≠ −4, −2, 1, not just x ≠ 1.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s5\">Practise 2.6 →</button></div></section><section class=\"note\" id=\"n27\"><h2>2.7 · Adding and subtracting rational expressions</h2><p class=\"lt\"><b>Learning target:</b> I can add and subtract rational expressions using the lowest common denominator, simplify, and state the restrictions.</p><p>Add and subtract rational expressions the way you add fractions: rewrite them over a <b>common denominator</b>, then add or subtract the numerators. The lowest common denominator (LCD) is the product of every different factor, each to its highest power.</p><div class=\"keybox\"><b>Method</b><br>1. Factor every denominator and state the restrictions.<br>2. Find the LCD.<br>3. Multiply each numerator by the factors its denominator is missing.<br>4. Add or subtract the numerators; put a <b>bracket</b> round a numerator that is being subtracted.<br>5. Simplify and factor the result if possible.</div><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Denominators</th><th>LCD</th></tr><tr><td class=\"mono\">4x and 6x²</td><td class=\"mono\">12x²</td></tr><tr><td class=\"mono\">x − 3 and x + 2</td><td class=\"mono\">(x − 3)(x + 2)</td></tr><tr><td class=\"mono\">(x − 2)(x + 2) and (x + 1)(x + 2)</td><td class=\"mono\">(x − 2)(x + 2)(x + 1)</td></tr></table></div><div class=\"ex\"><div class=\"exh\">Worked example 1 · Monomial denominators</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4x</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">5</span><span style=\"padding:2px 4px 0;white-space:nowrap\">6x²</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">9x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">12x²</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">10</span><span style=\"padding:2px 4px 0;white-space:nowrap\">12x²</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">9x + 10</span><span style=\"padding:2px 4px 0;white-space:nowrap\">12x²</span></span></span></div></div><br>Restriction: <b>x ≠ 0</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Subtracting</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 3</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 2</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2(x + 2) − (x − 3)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 3)(x + 2)</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 7</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 3)(x + 2)</span></span></span></div></div><br>2x + 4 − x + 3 = x + 7. Restrictions: <b>x ≠ −2, 3</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Factor the denominators first</div><div class=\"exl\"><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 4</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 3x + 2</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x(x + 1) + (x − 2)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 2)(x + 2)(x + 1)</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² + 2x − 2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x − 2)(x + 2)(x + 1)</span></span></span></div></div><br>Restrictions: <b>x ≠ −2, −1, 2</b>.</div></div><div class=\"ex\"><div class=\"exh\">Worked example 4 · Order of operations</div><div class=\"exl\">In <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x</span></span>+<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span>×<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x − 1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4</span></span> multiply first: <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span>×<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x − 1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4</span></span>=<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2</span></span>. Then <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x</span></span>+<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2</span></span>=<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + 2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x</span></span>, with x ≠ 0, 1.</div></div><div class=\"keybox\"><b>Common mistakes.</b> Never add tops and bottoms separately: <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x</span></span>+<span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">y</span></span> is <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x + y</span><span style=\"padding:2px 4px 0;white-space:nowrap\">xy</span></span>, not <span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + y</span></span>. When subtracting, the whole second numerator is subtracted: 5(x − 1) − 2(x + 1) = 5x − 5 − 2x − 2 = 3x − 7.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s6\">Practise 2.7 →</button></div></section><section class=\"note\" id=\"nPS\"><h2>PS · Problem solving</h2><p class=\"lt\"><b>Learning target:</b> I can model a situation with rational expressions, simplify and solve, and judge whether the answer makes sense.</p><div class=\"keybox\"><b>Modelling with rational expressions</b><br>1. Name the variable and write each quantity as an expression (a rate, a fraction of full marks, a probability).<br>2. Build the equation or expression, simplify it, and state restrictions.<br>3. Solve, then <b>check the answer in the situation</b>: marks cannot exceed the total, times and lengths are positive, and a probability is always between 0 and 1.</div><div class=\"tscroll\"><table class=\"ttab\"><tr><th>Situation</th><th>Expression</th></tr><tr><td>score s on a test out of x</td><td class=\"mono\">s/x (a fraction of full marks)</td></tr><tr><td>a part worth 25% of the final mark</td><td class=\"mono\">0.25 × (fraction scored)</td></tr><tr><td>time for distance d at speed v</td><td class=\"mono\">d/v</td></tr><tr><td>work rate: a job done in t hours</td><td class=\"mono\">1/t of the job per hour</td></tr></table></div><div class=\"ex\"><div class=\"exh\">Worked example 1 · A weighted mark</div><div class=\"exl\">A quiz is out of x marks and worth 20%; a test is out of 3x marks and worth 80%. Nia scores 15 and 54 and her final mark is 60%.<br>0.2 × 15/x + 0.8 × 54/(3x) = 3/x + 14.4/x = 17.4/x<br>17.4/x = 0.6, so <b>x = 29</b>. Check: 15 ≤ 29 and 54 ≤ 87 ✓</div></div><div class=\"ex\"><div class=\"exh\">Worked example 2 · Travel time</div><div class=\"exl\">A cyclist rides 60 km at s km/h and returns at (s + 10) km/h.<br><div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span>T =</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">60</span><span style=\"padding:2px 4px 0;white-space:nowrap\">s</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">60</span><span style=\"padding:2px 4px 0;white-space:nowrap\">s + 10</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">60(s + 10) + 60s</span><span style=\"padding:2px 4px 0;white-space:nowrap\">s(s + 10)</span></span></span><span>=</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">120(s + 5)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">s(s + 10)</span></span></span></div></div><br>With s = 20: T = 120(25)/(20 × 30) = <b>5 h</b> (3 h out, 2 h back ✓).</div></div><div class=\"ex\"><div class=\"exh\">Worked example 3 · Does the answer make sense?</div><div class=\"exl\">A model claims a probability is p(n) = 5/(n − 1). For n = 3 it gives {5/2}.<br>A probability can never be more than 1, so this value shows the <b>model is wrong</b> for n = 3, however neat the algebra is.</div></div><div class=\"keybox\"><b>Common mistake.</b> Stopping when the algebra is done. Always ask whether the value fits the story: a negative length, a total smaller than a score, or a probability above 1 means a modelling error somewhere.</div><div class=\"hub-btns\" style=\"margin-top:12px\"><button class=\"hub-btn primary\" data-go=\"s7\">Practise PS →</button></div></section><section class=\"note\" id=\"nsum\"><h2>Chapter checklist</h2><ul><li>I can add and subtract polynomials by removing brackets and collecting like terms, and I can test whether two polynomials are equivalent.</li><li>I can expand and simplify products of polynomials, including powers such as (a + b)² and (a + b)³.</li><li>I can simplify polynomial expressions and factor them fully: common factors, grouping, trinomials, perfect squares and differences of squares.</li><li>I can simplify a rational expression by dividing out common factors, and state its restrictions.</li><li>I can multiply and divide rational expressions, simplify, and state every restriction, including those from the divisor.</li><li>I can add and subtract rational expressions using the lowest common denominator, simplify, and state the restrictions.</li><li>I can model a situation with rational expressions, simplify and solve, and judge whether the answer makes sense.</li><li>I state restrictions from the original denominators (and divisors’ numerators) before I cancel.</li><li>I check an expansion or a factorisation by substituting a value such as x = 2 into both forms.</li></ul><div class=\"hub-btns\" style=\"margin-top:10px\"><button class=\"hub-btn\" data-go=\"s8\">Assessment A</button><button class=\"hub-btn\" data-go=\"s9\">Assessment B</button><button class=\"hub-btn\" data-go=\"s10\">Assessment C</button><button class=\"hub-btn\" data-go=\"s11\">Assessment D</button><button class=\"hub-btn primary\" data-go=\"report\">📊 Report</button></div></section>";
var REPORT = [["s8", "A", "Knowing and understanding"], ["s9", "B", "Investigating patterns"], ["s10", "C", "Communicating"], ["s11", "D", "Applying mathematics in real-life contexts"]];
var SECTIONS = [{"id": "s1", "label": "2.1 · Adding and subtracting polynomials", "sub": "I can add and subtract polynomials by removing brackets and collecting like terms, and I can test whether two polynomials are equivalent.", "slides": [{"kind": "blank", "p": "<b>Q1(a)</b> · Simplify (7x² − 2x + 1) + (9x² − 4x + 5) − (4x² + 6x − 7).", "tag": "", "marks": "", "flat": [{"t": "Remove the last bracket (change every sign): −(4x² + 6x − 7) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-4x^2-6x+7"}, "expr": "expanded"}, {"t": "Collect the x² terms: 7x² + 9x² − 4x² = __B1__", "a": {"B1": "12x^2"}, "expr": true}, {"t": "Collect the x terms: −2x − 4x − 6x = __B1__", "a": {"B1": "-12x"}, "expr": true}, {"t": "Collect the constants: 1 + 5 + 7 = __B1__", "a": {"B1": "13"}}, {"t": "Simplified: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "12x^2-12x+13"}, "expr": "expanded"}], "sol": "The minus sign multiplies every term by −1: −4x² − 6x + 7.\n(7 + 9 − 4)x² = 12x².\n(−2 − 4 − 6)x = −12x.\n1 + 5 + 7 = 13 (the −7 became +7).\n= 12x² − 12x + 13. Check with x = 1: 6 + 10 − 3 = 13 and 12 − 12 + 13 = 13 ✓"}, {"kind": "mcq", "text": "<b>Q1(b)</b> · Simplify (7a² − 4ab + 9b²) − (−a² + 2ab + 6b²).", "opts": ["6a² − 6ab + 3b²", "8a² − 2ab + 3b²", "6a² − 2ab + 15b²", "8a² − 6ab + 3b²"], "correct": 3, "tag": "", "sol": "Subtracting a bracket changes every sign inside it: = 7a² − 4ab + 9b² + a² − 2ab − 6b².\nCollect like terms: (7 + 1)a² + (−4 − 2)ab + (9 − 6)b² = 8a² − 6ab + 3b².\n6a² − 6ab + 3b² forgets that −(−a²) = +a²; 8a² − 2ab + 3b² leaves +2ab unchanged; 6a² − 2ab + 15b² adds the brackets instead of subtracting."}, {"kind": "mcq", "text": "<b>Q2</b> · Determine two non-equivalent polynomials f(x) and g(x), such that f(0) = g(0) and f(1) = g(1). Which pair works?", "opts": ["f(x) = 2x² and g(x) = x² + 1", "f(x) = x² and g(x) = x", "f(x) = (x − 1)² and g(x) = x² − 2x + 1", "f(x) = x + 1 and g(x) = 2x + 1"], "correct": 1, "tag": "", "sol": "f(x) = x², g(x) = x: f(0) = 0 = g(0) and f(1) = 1 = g(1), but f(2) = 4 while g(2) = 2, so they are not equivalent ✓\nx + 1 and 2x + 1 give f(1) = 2 but g(1) = 3. 2x² and x² + 1 give f(0) = 0 but g(0) = 1.\n(x − 1)² expands to x² − 2x + 1: that pair is equivalent, which the question does not allow.\nA general recipe: for any f(x), take g(x) = f(x) + x(x − 1). The extra part is 0 at x = 0 and x = 1, but not elsewhere."}, {"kind": "blank", "p": "<b>Q2</b> · Another answer to Q2: test f(x) = x³ and g(x) = x.", "tag": "", "marks": "", "flat": [{"t": "f(0) = __B1__ and g(0) = __B2__", "a": {"B1": "0", "B2": "0"}}, {"t": "f(1) = __B1__ and g(1) = __B2__", "a": {"B1": "1", "B2": "1"}}, {"t": "f(2) = __B1__ and g(2) = __B2__", "a": {"B1": "8", "B2": "2"}}, {"t": "Are f(x) = x³ and g(x) = x equivalent? (yes / no) __B1__", "a": {"B1": "no"}, "expr": "words"}], "sol": "0³ = 0 and g(0) = 0: equal.\n1³ = 1 and g(1) = 1: equal.\n2³ = 8 but g(2) = 2: different.\nNo. They agree at x = 0 and x = 1 (as Q2 asks) but not at x = 2, so they are two non-equivalent polynomials: a correct answer to Q2."}, {"kind": "blank", "p": "<b>Q3</b> · Ms. Flanagan has three daughters: Astrid, Beatrice, and Cassandra. Today, January 1, their ages are, respectively, A(n) = −(n + 30) + (2n + 5), B(n) = (7 − n) − (32 − 2n), C(n) = (n − 26) − (n + 4) + (n − 3). All ages are expressed in years, and n represents Ms. Flanagan’s age. First simplify each expression.", "tag": "", "marks": "", "flat": [{"t": "A(n) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "n-25"}, "expr": "expanded"}, {"t": "B(n) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "n-25"}, "expr": "expanded"}, {"t": "C(n) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "n-33"}, "expr": "expanded"}], "sol": "A(n) = −n − 30 + 2n + 5 = n − 25.\nB(n) = 7 − n − 32 + 2n = n − 25.\nC(n) = n − 26 − n − 4 + n − 3 = n − 33."}, {"kind": "mcq", "text": "<b>Q3(a)</b> · With A(n) = n − 25, B(n) = n − 25 and C(n) = n − 33, are the three daughters triplets?", "opts": ["No: Astrid is 8 years older than Beatrice", "No: Cassandra is 8 years younger than her sisters", "Yes: in every expression n has coefficient 1", "Yes: all three ages are polynomials in n"], "correct": 1, "tag": "", "sol": "Triplets would have equal ages, so all three expressions would be equivalent.\nA(n) = B(n) = n − 25 but C(n) = n − 33, and (n − 25) − (n − 33) = 8.\nSo they are not triplets: Cassandra is 8 years younger than Astrid and Beatrice."}, {"kind": "mcq", "text": "<b>Q3(b)</b> · Are any of the daughters twins?", "opts": ["Yes: Astrid and Beatrice are both n − 25 years old", "No: no two daughters are the same age", "No: the three expressions look different", "Yes: Beatrice and Cassandra are the same age"], "correct": 0, "tag": "", "sol": "A(n) and B(n) look different but both simplify to n − 25, so they are equivalent: Astrid and Beatrice are the same age for every value of n.\nSo Astrid and Beatrice are twins. Cassandra (n − 33) is not."}, {"kind": "blank", "p": "<b>Q3(c)</b> · How old was Ms. Flanagan when Cassandra was born?", "tag": "", "marks": "", "flat": [{"t": "Ms. Flanagan is older than Cassandra by n − C(n) = n − (n − 33) = __B1__ years", "a": {"B1": "33"}}, {"t": "So when Cassandra was born, Ms. Flanagan was __B1__ years old", "a": {"B1": "33"}}, {"t": "Check: if Ms. Flanagan is 45 today, Cassandra is __B1__", "a": {"B1": "12"}}], "sol": "n − (n − 33) = 33: the difference does not depend on n.\nAn age difference never changes, so Ms. Flanagan was 33 when Cassandra was born.\nC(45) = 45 − 33 = 12, and 45 − 12 = 33 ✓"}, {"kind": "mcq", "text": "Simplify (5x² − 3x + 2) − (2x² − 3x − 4).", "opts": ["3x² − 6x + 6", "3x² − 6x − 2", "7x² + 6", "3x² + 6"], "correct": 3, "tag": "", "sol": "= 5x² − 3x + 2 − 2x² + 3x + 4 = 3x² + 0x + 6 = 3x² + 6.\n3x² − 6x − 2 forgets to change the signs; 3x² − 6x + 6 changes only the constant; 7x² + 6 adds the x² terms."}, {"kind": "blank", "p": "A triangle has sides (2x² + 3x − 1) cm, (x² − 4x + 6) cm and (3x² + x − 2) cm.", "tag": "", "marks": "", "flat": [{"t": "Perimeter = __B1__ cm", "a": {"B1": "6x^2+3"}, "expr": true}, {"t": "Perimeter when x = 2: __B1__ cm", "a": {"B1": "27"}}], "sol": "x²: 2 + 1 + 3 = 6; x: 3 − 4 + 1 = 0; constants: −1 + 6 − 2 = 3, so P = 6x² + 3.\n6(4) + 3 = 27 cm (sides 13, 2 and 12 cm ✓)."}, {"kind": "mcq", "text": "Are f(x) = (x + 3)² − (x − 3)² and g(x) = 12x equivalent?", "opts": ["No: f(x) = 0 because the squares cancel", "No: f(x) simplifies to 2x² + 18", "Only when x = 0", "Yes: f(x) simplifies to 12x"], "correct": 3, "tag": "", "sol": "(x + 3)² = x² + 6x + 9 and (x − 3)² = x² − 6x + 9.\nSubtract: x² + 6x + 9 − x² + 6x − 9 = 12x, so f and g are equivalent (equal for every x).\n2x² + 18 adds the squares; “0” cancels terms that are not equal."}]}, {"id": "s2", "label": "2.2 · Multiplying polynomials", "sub": "I can expand and simplify products of polynomials, including powers such as (a + b)² and (a + b)³.", "slides": [{"kind": "blank", "p": "<b>Q4(a)</b> · Expand and simplify −3(7x − 5)(4x − 7).", "tag": "", "marks": "", "flat": [{"t": "Multiply the brackets: (7x − 5)(4x − 7) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "28x^2-69x+35"}, "expr": "expanded"}, {"t": "Multiply by −3: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-84x^2+207x-105"}, "expr": "expanded"}], "sol": "28x² − 49x − 20x + 35 = 28x² − 69x + 35.\n−3 × each term: −84x² + 207x − 105."}, {"kind": "blank", "p": "<b>Q4(b)</b> · Expand and simplify −(y² − 4y + 7)(3y² − 5y − 3).", "tag": "", "marks": "", "flat": [{"t": "y²(3y² − 5y − 3) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3y^4-5y^3-3y^2"}, "expr": "expanded"}, {"t": "−4y(3y² − 5y − 3) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-12y^3+20y^2+12y"}, "expr": "expanded"}, {"t": "7(3y² − 5y − 3) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "21y^2-35y-21"}, "expr": "expanded"}, {"t": "Add: (y² − 4y + 7)(3y² − 5y − 3) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3y^4-17y^3+38y^2-23y-21"}, "expr": "expanded"}, {"t": "Multiply by −1: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-3y^4+17y^3-38y^2+23y+21"}, "expr": "expanded"}], "sol": "3y⁴ − 5y³ − 3y².\n−12y³ + 20y² + 12y.\n21y² − 35y − 21.\ny³: −5 − 12 = −17; y²: −3 + 20 + 21 = 38; y: 12 − 35 = −23; so 3y⁴ − 17y³ + 38y² − 23y − 21.\nChange every sign: −3y⁴ + 17y³ − 38y² + 23y + 21."}, {"kind": "mcq", "text": "<b>Q4(c)</b> · Expand and simplify 2(a + b)³.", "opts": ["2a³ + 2b³", "2a³ + 4a²b + 4ab² + 2b³", "8a³ + 24a²b + 24ab² + 8b³", "2a³ + 6a²b + 6ab² + 2b³"], "correct": 3, "tag": "", "sol": "(a + b)² = a² + 2ab + b², and (a² + 2ab + b²)(a + b) = a³ + 3a²b + 3ab² + b³.\nMultiply by 2: 2a³ + 6a²b + 6ab² + 2b³.\n2a³ + 2b³ cubes each term (missing middle terms); 8a³ + … cubes the 2 as well, as if it were (2a + 2b)³."}, {"kind": "blank", "p": "<b>Q4(d)</b> · Expand and simplify 3(x² − 2)²(2x − 3)².", "tag": "", "marks": "", "flat": [{"t": "(x² − 2)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^4-4x^2+4"}, "expr": "expanded"}, {"t": "(2x − 3)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "4x^2-12x+9"}, "expr": "expanded"}, {"t": "(x⁴ − 4x² + 4)(4x² − 12x + 9) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "4x^6-12x^5-7x^4+48x^3-20x^2-48x+36"}, "expr": "expanded"}, {"t": "Multiply by 3: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "12x^6-36x^5-21x^4+144x^3-60x^2-144x+108"}, "expr": "expanded"}], "sol": "(a − b)² = a² − 2ab + b²: x⁴ − 4x² + 4.\n4x² − 12x + 9.\nx⁴(4x² − 12x + 9) − 4x²(4x² − 12x + 9) + 4(4x² − 12x + 9) = 4x⁶ − 12x⁵ + 9x⁴ − 16x⁴ + 48x³ − 36x² + 16x² − 48x + 36 = 4x⁶ − 12x⁵ − 7x⁴ + 48x³ − 20x² − 48x + 36.\n12x⁶ − 36x⁵ − 21x⁴ + 144x³ − 60x² − 144x + 108. Check with x = 1: 3(1)(1) = 3 and 12 − 36 − 21 + 144 − 60 − 144 + 108 = 3 ✓"}, {"kind": "blank", "p": "<b>Q5</b> · The volume of a cone is given by V = {1/3}πr²h. Determine the volume of the cone in simplified form if the radius is increased by x and the height is increased by 2x.", "tag": "", "marks": "", "flat": [{"t": "New radius = __B1__", "a": {"B1": "r+x"}, "expr": true}, {"t": "New height = __B1__", "a": {"B1": "h+2x"}, "expr": true}, {"t": "(r + x)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "r^2+2rx+x^2"}, "expr": "expanded"}, {"t": "(r² + 2rx + x²)(h + 2x) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "r^2h+2r^2x+2rhx+4rx^2+hx^2+2x^3"}, "expr": "expanded"}, {"t": "V = __B1__  (type π as pi)", "a": {"B1": "pi/3*(r^2h+2r^2x+2rhx+4rx^2+hx^2+2x^3)"}, "expr": true}], "sol": "The radius r becomes r + x.\nThe height h becomes h + 2x.\n(r + x)² = r² + 2rx + x² (do not forget 2rx).\nr²h + 2r²x + 2rhx + 4rx² + hx² + 2x³.\nV = {1/3}π(r + x)²(h + 2x) = (π/3)(r²h + 2r²x + 2rhx + 4rx² + hx² + 2x³)."}, {"kind": "mcq", "text": "<b>Q5</b> · Which is the simplified volume of the enlarged cone (radius r + x, height h + 2x)?", "opts": ["π(r²h + 2r²x + 2rhx + 4rx² + hx² + 2x³)", "(π/3)(rh + 2rx + hx + 2x²)", "(π/3)(r²h + 2r²x + hx² + 2x³)", "(π/3)(r²h + 2r²x + 2rhx + 4rx² + hx² + 2x³)"], "correct": 3, "tag": "", "sol": "V = {1/3}π(r + x)²(h + 2x) and (r + x)² = r² + 2rx + x².\n(r² + 2rx + x²)(h + 2x) = r²h + 2r²x + 2rhx + 4rx² + hx² + 2x³, so V = (π/3)(r²h + 2r²x + 2rhx + 4rx² + hx² + 2x³).\nThe second option used (r + x)² = r² + x² (missing 2rx); the third forgot to square; the fourth dropped the {1/3}."}, {"kind": "mcq", "text": "Expand (2x − 5)².", "opts": ["4x² − 20x + 25", "4x² − 10x + 25", "4x² − 25", "4x² + 25"], "correct": 0, "tag": "", "sol": "(a − b)² = a² − 2ab + b² with a = 2x, b = 5: 4x² − 2(2x)(5) + 25 = 4x² − 20x + 25.\n4x² + 25 misses the middle term; 4x² − 25 is (2x − 5)(2x + 5); −10x forgets the 2 in 2ab."}, {"kind": "blank", "p": "Expand and simplify (x + 4)(x² − 3x + 2).", "tag": "", "marks": "", "flat": [{"t": "x(x² − 3x + 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^3-3x^2+2x"}, "expr": "expanded"}, {"t": "4(x² − 3x + 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "4x^2-12x+8"}, "expr": "expanded"}, {"t": "Sum: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^3+x^2-10x+8"}, "expr": "expanded"}], "sol": "x³ − 3x² + 2x.\n4x² − 12x + 8.\nx³ + (−3 + 4)x² + (2 − 12)x + 8 = x³ + x² − 10x + 8."}, {"kind": "mcq", "text": "A box measures (x + 1) cm by (x + 2) cm by (x + 3) cm. Which expression is its volume in cm³?", "opts": ["x³ + 6", "x³ + 6x² + 11x + 6", "3x + 6", "x³ + 6x² + 6"], "correct": 1, "tag": "", "sol": "(x + 1)(x + 2) = x² + 3x + 2, and (x² + 3x + 2)(x + 3) = x³ + 3x² + 3x² + 9x + 2x + 6 = x³ + 6x² + 11x + 6.\n3x + 6 is the sum of the three edges, not their product."}]}, {"id": "s3", "label": "2.3 · Simplifying and factoring polynomials", "sub": "I can simplify polynomial expressions and factor them fully: common factors, grouping, trinomials, perfect squares and differences of squares.", "slides": [{"kind": "mcq", "text": "<b>Q6(a)</b> · Simplify (2x⁴ − 3x² − 6) + (6x⁴ − x³ + 4x² + 5).", "opts": ["8x⁴ − x³ + x² − 1", "8x⁴ + x² − 1", "8x⁸ − x³ + x² − 1", "−4x⁴ + x³ − 7x² − 11"], "correct": 0, "tag": "", "sol": "Adding: drop the brackets and collect. x⁴: 2 + 6 = 8; x³: −1; x²: −3 + 4 = 1; constants: −6 + 5 = −1.\nSo 8x⁴ − x³ + x² − 1. (8x⁸ adds the exponents, which only happens when multiplying; −4x⁴ … subtracts instead of adding.)"}, {"kind": "blank", "p": "<b>Q6(b)</b> · Simplify (x² − 4)(2x² + 5x − 2).", "tag": "", "marks": "", "flat": [{"t": "x²(2x² + 5x − 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x^4+5x^3-2x^2"}, "expr": "expanded"}, {"t": "−4(2x² + 5x − 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-8x^2-20x+8"}, "expr": "expanded"}, {"t": "Sum: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x^4+5x^3-10x^2-20x+8"}, "expr": "expanded"}], "sol": "2x⁴ + 5x³ − 2x².\n−8x² − 20x + 8.\nx²: −2 − 8 = −10, so 2x⁴ + 5x³ − 10x² − 20x + 8."}, {"kind": "blank", "p": "<b>Q6(c)</b> · Simplify −7x(x² + x − 1) − 3x(2x² − 5x + 6).", "tag": "", "marks": "", "flat": [{"t": "−7x(x² + x − 1) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-7x^3-7x^2+7x"}, "expr": "expanded"}, {"t": "−3x(2x² − 5x + 6) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-6x^3+15x^2-18x"}, "expr": "expanded"}, {"t": "Simplified: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-13x^3+8x^2-11x"}, "expr": "expanded"}], "sol": "−7x³ − 7x² + 7x.\n−6x³ + 15x² − 18x (−3x × −5x = +15x²).\nx³: −7 − 6 = −13; x²: −7 + 15 = 8; x: 7 − 18 = −11, so −13x³ + 8x² − 11x."}, {"kind": "mcq", "text": "<b>Q6(d)</b> · Simplify −2x²(3x³ − 7x + 2) − x³(5x³ + 2x − 8).", "opts": ["−5x⁶ − 6x⁵ + 2x⁴ + 22x³ − 4x²", "−5x⁶ − 6x⁵ − 2x⁴ + 6x³ − 4x²", "−5x⁶ − 6x⁵ − 2x⁴ + 22x³ − 4x²", "−5x⁶ − 6x⁵ − 2x⁴ + 22x³ + 4x²"], "correct": 2, "tag": "", "sol": "−2x²(3x³ − 7x + 2) = −6x⁵ + 14x³ − 4x².\n−x³(5x³ + 2x − 8) = −5x⁶ − 2x⁴ + 8x³ (−x³ × −8 = +8x³).\nTotal, highest power first: −5x⁶ − 6x⁵ − 2x⁴ + 22x³ − 4x². Each wrong option has one sign error."}, {"kind": "blank", "p": "<b>Q6(e)</b> · Simplify −2x[5x − (2x − 7)] + 6x[3x − (1 + 2x)].", "tag": "", "marks": "", "flat": [{"t": "Inner bracket: 5x − (2x − 7) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3x+7"}, "expr": "expanded"}, {"t": "Inner bracket: 3x − (1 + 2x) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x-1"}, "expr": "expanded"}, {"t": "−2x(3x + 7) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-6x^2-14x"}, "expr": "expanded"}, {"t": "6x(x − 1) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "6x^2-6x"}, "expr": "expanded"}, {"t": "Simplified: __B1__", "a": {"B1": "-20x"}, "expr": true}], "sol": "5x − 2x + 7 = 3x + 7.\n3x − 1 − 2x = x − 1.\n−6x² − 14x.\n6x² − 6x.\n−6x² + 6x² − 14x − 6x = −20x. The x² terms cancel."}, {"kind": "blank", "p": "<b>Q6(f)</b> · Simplify (x + 2)²(x − 1)² − (x − 4)²(x + 4)².", "tag": "", "marks": "", "flat": [{"t": "(x + 2)(x − 1) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^2+x-2"}, "expr": "expanded"}, {"t": "So (x + 2)²(x − 1)² = (x² + x − 2)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^4+2x^3-3x^2-4x+4"}, "expr": "expanded"}, {"t": "(x − 4)(x + 4) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^2-16"}, "expr": "expanded"}, {"t": "So (x − 4)²(x + 4)² = (x² − 16)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^4-32x^2+256"}, "expr": "expanded"}, {"t": "Difference: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x^3+29x^2-4x-252"}, "expr": "expanded"}], "sol": "Use a²b² = (ab)²: (x + 2)(x − 1) = x² + x − 2.\n(x² + x − 2)² = x⁴ + x² + 4 + 2x³ − 4x² − 4x = x⁴ + 2x³ − 3x² − 4x + 4.\nDifference of squares: x² − 16.\nx⁴ − 32x² + 256.\nx⁴ − x⁴ + 2x³ + (−3 + 32)x² − 4x + 4 − 256 = 2x³ + 29x² − 4x − 252."}, {"kind": "mcq", "text": "<b>Q6(g)</b> · Simplify (x² + 5x − 3)².", "opts": ["x⁴ + 10x³ + 31x² − 30x + 9", "x⁴ + 10x³ + 19x² − 30x + 9", "x⁴ + 10x³ + 19x² + 30x + 9", "x⁴ + 25x² + 9"], "correct": 1, "tag": "", "sol": "(x² + 5x − 3)(x² + 5x − 3): squares x⁴ + 25x² + 9, cross terms 2(x²)(5x) = 10x³, 2(x²)(−3) = −6x², 2(5x)(−3) = −30x.\nx²: 25 − 6 = 19, so x⁴ + 10x³ + 19x² − 30x + 9.\nx⁴ + 25x² + 9 squares each term and misses every cross term."}, {"kind": "blank", "p": "<b>Q7(a)</b> · Factor 12m²n³ + 18m³n².", "tag": "", "marks": "", "flat": [{"t": "GCF of 12 and 18 = __B1__", "a": {"B1": "6"}}, {"t": "GCF of the two terms = __B1__", "a": {"B1": "6m^2n^2"}, "expr": true}, {"t": "12m²n³ ÷ 6m²n² = __B1__", "a": {"B1": "2n"}, "expr": true}, {"t": "18m³n² ÷ 6m²n² = __B1__", "a": {"B1": "3m"}, "expr": true}, {"t": "Factored: 12m²n³ + 18m³n² = 6m²n²(__B1__)", "a": {"B1": "2n+3m"}, "expr": true}], "sol": "6 divides both 12 and 18.\nLowest powers: m² and n², so 6m²n².\n2n.\n3m.\n6m²n²(2n + 3m). Check: 12m²n³ + 18m³n² ✓"}, {"kind": "mcq", "text": "<b>Q7(b)</b> · Factor x² − 9x + 20.", "opts": ["(x + 4)(x + 5)", "(x − 2)(x − 10)", "(x + 4)(x − 5)", "(x − 4)(x − 5)"], "correct": 3, "tag": "", "sol": "Find two numbers with product 20 and sum −9: −4 and −5.\nx² − 9x + 20 = (x − 4)(x − 5). (x + 4)(x + 5) gives +9x; (x − 2)(x − 10) gives −12x; (x + 4)(x − 5) gives −x − 20."}, {"kind": "blank", "p": "<b>Q7(c)</b> · Factor 3x² + 24x + 45 fully.", "tag": "", "marks": "", "flat": [{"t": "Common factor of every term = __B1__", "a": {"B1": "3"}}, {"t": "x² + 8x + 15: two integers with product 15 and sum 8 are __B1__ (separate with a comma)", "a": {"B1": "3, 5"}, "expr": "set"}, {"t": "Factored fully: 3x² + 24x + 45 = 3(__B1__)(__B2__)  (one bracket in each box, smaller constant first)", "a": {"B1": "x+3", "B2": "x+5"}, "expr": true}], "sol": "3x² + 24x + 45 = 3(x² + 8x + 15).\n3 × 5 = 15 and 3 + 5 = 8.\n3(x + 3)(x + 5)."}, {"kind": "mcq", "text": "<b>Q7(d)</b> · Factor 50x² − 72 fully.", "opts": ["(5x − 6)(5x + 6)", "2(5x − 6)(5x + 6)", "2(x − 6)(x + 6)", "2(5x − 6)²"], "correct": 1, "tag": "", "sol": "Common factor first: 50x² − 72 = 2(25x² − 36).\n25x² − 36 = (5x)² − 6² is a difference of squares: (5x − 6)(5x + 6). So 2(5x − 6)(5x + 6).\n(5x − 6)(5x + 6) loses the 2; 2(5x − 6)² would have a middle term; 2(x − 6)(x + 6) = 2x² − 72."}, {"kind": "blank", "p": "<b>Q7(e)</b> · Factor 9x² − 6x + 1.", "tag": "", "marks": "", "flat": [{"t": "9x² = (__B1__)²", "a": {"B1": "3x"}, "expr": true}, {"t": "1 = (__B1__)²", "a": {"B1": "1"}}, {"t": "Middle term check: 2 × 3x × 1 = __B1__", "a": {"B1": "6x"}, "expr": true}, {"t": "So 9x² − 6x + 1 = (__B1__)²", "a": {"B1": "3x-1"}, "expr": true, "accept": ["1-3x"]}], "sol": "9x² = (3x)².\n1 = 1².\n2(3x)(1) = 6x, and the middle term is −6x: a perfect square trinomial.\n(3x − 1)². Check: 9x² − 6x + 1 ✓ ((1 − 3x)² is the same.)"}, {"kind": "blank", "p": "<b>Q7(f)</b> · Factor 10a² + a − 3.", "tag": "", "marks": "", "flat": [{"t": "ac = 10 × (−3) = __B1__", "a": {"B1": "-30"}}, {"t": "Two integers with product −30 and sum 1: __B1__", "a": {"B1": "6, -5"}, "expr": "set"}, {"t": "10a² + 6a − 5a − 3 = 2a(5a + 3) − 1(__B1__)", "a": {"B1": "5a+3"}, "expr": true}, {"t": "Factored: 10a² + a − 3 = (__B1__)(5a + 3)", "a": {"B1": "2a-1"}, "expr": true}], "sol": "ac = −30.\n6 × (−5) = −30 and 6 + (−5) = 1.\nGroup in pairs: 2a(5a + 3) − 1(5a + 3).\n(2a − 1)(5a + 3). Check: 10a² + 6a − 5a − 3 ✓"}, {"kind": "mcq", "text": "<b>Q8(a)</b> · Factor 2x²y⁴ − 6x⁵y³ + 8x³y.", "opts": ["2x²y(y³ − 3x³y² + 4xy)", "2x²y(y³ − 3x³y² + 4x)", "2x²y³(y − 3x³ + 4x)", "2x²y(y⁴ − 3x³y³ + 4x)"], "correct": 1, "tag": "", "sol": "GCF: 2 (of 2, 6, 8), x² (lowest power of x), y (lowest power of y): 2x²y.\n2x²y⁴ ÷ 2x²y = y³; 6x⁵y³ ÷ 2x²y = 3x³y²; 8x³y ÷ 2x²y = 4x. So 2x²y(y³ − 3x³y² + 4x).\n2x²y³ is not a factor of 8x³y (only one y)."}, {"kind": "blank", "p": "<b>Q8(b)</b> · Factor 2x(x + 4) + 3(x + 4).", "tag": "", "marks": "", "flat": [{"t": "The common factor is the bracket __B1__", "a": {"B1": "x+4"}, "expr": true}, {"t": "Factored: (x + 4)(__B1__)", "a": {"B1": "2x+3"}, "expr": true}], "sol": "Both terms contain the factor (x + 4).\n(x + 4)(2x + 3). Check: 2x(x + 4) + 3(x + 4) ✓"}, {"kind": "mcq", "text": "<b>Q8(c)</b> · Factor x² − 3x − 10.", "opts": ["(x − 5)(x − 2)", "(x + 5)(x − 2)", "(x − 10)(x + 1)", "(x − 5)(x + 2)"], "correct": 3, "tag": "", "sol": "Two numbers with product −10 and sum −3: −5 and 2. So (x − 5)(x + 2).\n(x + 5)(x − 2) gives +3x; (x − 5)(x − 2) gives +10; (x − 10)(x + 1) gives −9x."}, {"kind": "blank", "p": "<b>Q8(d)</b> · Factor 15x² − 53x + 42.", "tag": "", "marks": "", "flat": [{"t": "ac = 15 × 42 = __B1__", "a": {"B1": "630"}}, {"t": "Two integers with product 630 and sum −53: __B1__", "a": {"B1": "-18, -35"}, "expr": "set"}, {"t": "15x² − 18x − 35x + 42 = 3x(5x − 6) − 7(__B1__)", "a": {"B1": "5x-6"}, "expr": true}, {"t": "Factored: 15x² − 53x + 42 = (__B1__)(5x − 6)", "a": {"B1": "3x-7"}, "expr": true}], "sol": "630.\n(−18)(−35) = 630 and −18 − 35 = −53.\n3x(5x − 6) − 7(5x − 6).\n(3x − 7)(5x − 6). Check: 15x² − 18x − 35x + 42 ✓"}, {"kind": "mcq", "text": "<b>Q8(e)</b> · Factor a⁴ − 16 fully.", "opts": ["(a − 2)²(a + 2)²", "(a² + 4)(a − 2)(a + 2)", "(a² + 4)(a² − 4)", "(a − 2)⁴"], "correct": 1, "tag": "", "sol": "a⁴ − 16 = (a²)² − 4² = (a² − 4)(a² + 4).\na² − 4 is again a difference of squares: (a − 2)(a + 2). So (a² + 4)(a − 2)(a + 2).\n(a² + 4)(a² − 4) is correct but not finished; (a − 2)²(a + 2)² = (a² − 4)², which has a −8a² term."}, {"kind": "blank", "p": "<b>Q8(f)</b> · Factor (m − n)² − (2m + 3n)².", "tag": "", "marks": "", "flat": [{"t": "It is A² − B² with A = m − n and B = __B1__", "a": {"B1": "2m+3n"}, "expr": true}, {"t": "A − B = (m − n) − (2m + 3n) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "-m-4n"}, "expr": "expanded"}, {"t": "A + B = (m − n) + (2m + 3n) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3m+2n"}, "expr": "expanded"}, {"t": "Factored: (m − n)² − (2m + 3n)² = (A − B)(A + B) = −(__B1__)(3m + 2n)", "a": {"B1": "m+4n"}, "expr": true}], "sol": "B = 2m + 3n.\nm − n − 2m − 3n = −m − 4n.\n3m + 2n.\n(−m − 4n)(3m + 2n) = −(m + 4n)(3m + 2n)."}]}, {"id": "s4", "label": "2.4 · Simplifying rational functions", "sub": "I can simplify a rational expression by dividing out common factors, and state its restrictions.", "slides": [{"kind": "blank", "p": "<b>Q9(a)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "10a²b ÷ (−5b) = __B1__", "a": {"B1": "-2a^2"}, "expr": true}, {"t": "15bc² ÷ (−5b) = __B1__", "a": {"B1": "-3c^2"}, "expr": true}, {"t": "Simplified: __B1__", "a": {"B1": "-2a^2-3c^2"}, "expr": true}, {"t": "Restriction: b ≠ __B1__", "a": {"B1": "0"}}], "sol": "Divide each term of the numerator by −5b: −2a².\n−3c².\n−2a² − 3c².\nThe denominator −5b is 0 when b = 0, so b ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">10a²b + 15bc²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">−5b</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q9(b)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "30x²y³ ÷ 10x² = __B1__", "a": {"B1": "3y^3"}, "expr": true}, {"t": "−20x²z² ÷ 10x² = __B1__", "a": {"B1": "-2z^2"}, "expr": true}, {"t": "50x² ÷ 10x² = __B1__", "a": {"B1": "5"}}, {"t": "Simplified: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3y^3-2z^2+5"}, "expr": "expanded"}, {"t": "Restriction: x ≠ __B1__", "a": {"B1": "0"}}], "sol": "3y³.\n−2z².\n5.\n3y³ − 2z² + 5.\n10x² = 0 when x = 0, so x ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">30x²y³ − 20x²z² + 50x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">10x²</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q9(c)</b> · Simplify. State any restrictions on the variables.", "opts": ["1 − z; x ≠ 0, y ≠ 0, z ≠ 0", "−z; x ≠ 0, y ≠ 0", "1 − z; no restrictions", "1 − z; x ≠ 0, y ≠ 0"], "correct": 3, "tag": "", "sol": "Factor: xy − xyz = xy(1 − z). So xy(1 − z)/(xy) = 1 − z.\nThe denominator xy is 0 when x = 0 or y = 0, so x ≠ 0, y ≠ 0. z may be any value: it is not in the denominator.\n“−z” cancels xy with xy and leaves nothing (it should leave 1).", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">xy − xyz</span><span style=\"padding:2px 4px 0;white-space:nowrap\">xy</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q9(d)</b> · Simplify. State any restrictions on the variables.", "opts": ["2r − 24mnp + 40kmn; m ≠ 0, n ≠ 0", "2r − 3p + 5kmn; m ≠ 0, n ≠ 0", "2r − 3p + 5k; m ≠ 0, n ≠ 0", "2r − 3p + 5k; m ≠ 0, n ≠ 0, k ≠ 0"], "correct": 2, "tag": "", "sol": "Divide every term by 8mn: 16mnr/(8mn) = 2r, 24mnp/(8mn) = 3p, 40kmn/(8mn) = 5k.\nSo 2r − 3p + 5k, with m ≠ 0 and n ≠ 0 (from 8mn).\nThe second option divides only the first term.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">16mnr − 24mnp + 40kmn</span><span style=\"padding:2px 4px 0;white-space:nowrap\">8mn</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q10(a)</b> · Simplify. State any restrictions on the variables. (As printed in the book, the fraction bar is under 6x³ only.)", "tag": "", "marks": "", "flat": [{"t": "6x³/(2xy) = __B1__", "a": {"B1": "3x^2/y"}, "expr": true}, {"t": "Simplified: __B1__", "a": {"B1": "8xy^2+12x^2y-3x^2/y"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ and y ≠ __B2__", "a": {"B1": "0", "B2": "0"}}], "sol": "6x³/(2xy) = 3x²/y (divide by 2 and by x).\n8xy² + 12x²y − 3x²/y. The first two terms have no denominator and stay as they are.\n2xy ≠ 0, so x ≠ 0 and y ≠ 0. (If the whole numerator 8xy² + 12x²y − 6x³ were over 2xy, the answer would be 4y + 6x − 3x²/y, with the same restrictions.)", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span>8xy² + 12x²y −</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6x³</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2xy</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q10(b)</b> · Simplify. State any restrictions on the variables.", "opts": ["{7/2}; a ≠ 0, b ≠ 0", "{7/2}; a ≠ 2b", "7; a ≠ 2b", "{7/2}; no restrictions"], "correct": 1, "tag": "", "sol": "Factor the numerator: 7a − 14b = 7(a − 2b). So 7(a − 2b)/(2(a − 2b)) = 7/2.\nThe denominator 2(a − 2b) is 0 when a = 2b, so a ≠ 2b (this restriction stays even though the factor cancels).\n“7” forgets the 2 in the denominator.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">7a − 14b</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2(a − 2b)</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q10(c)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "m² + 10m + 21 = (m + 3)(m + __B1__)", "a": {"B1": "7"}}, {"t": "Simplified: __B1__", "a": {"B1": "1/(m+7)"}, "expr": true}, {"t": "Restrictions: m ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-7, -3"}, "expr": "dlist"}], "sol": "3 × 7 = 21 and 3 + 7 = 10.\n(m + 3)/((m + 3)(m + 7)) = 1/(m + 7): the numerator becomes 1, not 0.\n(m + 3)(m + 7) = 0 at m = −3 and m = −7, so m ≠ −7, −3.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">m + 3</span><span style=\"padding:2px 4px 0;white-space:nowrap\">m² + 10m + 21</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q10(d)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "Numerator: 4x² − 4x − 3 = (2x − 3)(2x + __B1__)", "a": {"B1": "1"}}, {"t": "Denominator: 4x² − 9 = (2x − 3)(2x + __B1__)", "a": {"B1": "3"}}, {"t": "Simplified: __B1__", "a": {"B1": "(2x+1)/(2x+3)"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (type fractions as decimals, increasing, separated by commas)", "a": {"B1": "-1.5, 1.5"}, "expr": "dlist", "accept": ["-1.5, 3/2", "-3/2, 1.5", "-3/2, 3/2"]}], "sol": "ac = −12: −6 and 2 give 4x² − 6x + 2x − 3 = 2x(2x − 3) + 1(2x − 3) = (2x − 3)(2x + 1).\nDifference of squares: (2x − 3)(2x + 3).\n(2x + 1)/(2x + 3).\n2x − 3 = 0 gives x = {3/2}; 2x + 3 = 0 gives x = −{3/2}. So x ≠ −1.5, 1.5.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4x² − 4x − 3</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4x² − 9</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q10(e)</b> · Simplify. State any restrictions on the variables.", "opts": ["{3/7}; x ≠ 1, 3", "3x(x − 7)/(7(x − 1)(x − 3)); x ≠ 1, 3", "3x/(7(x − 1)); x ≠ 1", "3x(x − 7)/(7(x − 1)(x − 3)); x ≠ 0, 1, 3, 7"], "correct": 1, "tag": "", "sol": "Numerator: 3x² − 21x = 3x(x − 7). Denominator: 7x² − 28x + 21 = 7(x² − 4x + 3) = 7(x − 1)(x − 3).\nThere is no common factor, so the simplest form is 3x(x − 7)/(7(x − 1)(x − 3)), with x ≠ 1, 3.\nZeros of the numerator are not restrictions; {3/7} cancels terms (3x² with 7x²), not factors; x − 7 and x − 3 are different factors and do not cancel.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3x² − 21x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">7x² − 28x + 21</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q10(f)</b> · Simplify. State any restrictions on the variables.", "opts": ["(x − 2y)/(x + 4y); x ≠ −4y", "(x − y)/(x + y); x ≠ −y", "(x − y)/(x + y); x ≠ 0, y ≠ 0", "(x − y)/(x + y); x ≠ −y, x ≠ −y/3"], "correct": 3, "tag": "", "sol": "3x² − 2xy − y² = (3x + y)(x − y) and 3x² + 4xy + y² = (3x + y)(x + y).\nCancel (3x + y): (x − y)/(x + y).\nRestrictions from (3x + y)(x + y) ≠ 0: x ≠ −y and 3x ≠ −y, that is x ≠ −y/3. Cancelling “3x²” and “y²” (the third option) cancels terms, not factors.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3x² − 2xy − y²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3x² + 4xy + y²</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q11</b> · If two rational functions have the same restrictions, are they equivalent? Explain and illustrate with an example. Test the example f(x) = (x + 1)/(x − 2) and g(x) = 5/(x − 2).", "tag": "", "marks": "", "flat": [{"t": "Restriction of f: x ≠ __B1__", "a": {"B1": "2"}}, {"t": "Restriction of g: x ≠ __B1__", "a": {"B1": "2"}}, {"t": "f(3) = __B1__", "a": {"B1": "4"}}, {"t": "g(3) = __B1__", "a": {"B1": "5"}}, {"t": "So, are f and g equivalent? (yes / no) __B1__", "a": {"B1": "no"}, "expr": "words"}], "sol": "x − 2 = 0 at x = 2.\nThe same denominator, so the same restriction x ≠ 2.\n(3 + 1)/1 = 4.\n5/1 = 5.\nNo: they have the same restrictions but f(3) ≠ g(3), so they are not equivalent."}, {"kind": "mcq", "text": "<b>Q11</b> · If two rational functions have the same restrictions, are they equivalent? Which explanation and example are correct?", "opts": ["Yes, as long as the denominators are equal", "Not necessarily: 1/(x − 2) and 3/(x − 2) both need x ≠ 2, but at x = 3 they give 1 and 3", "Yes: the restrictions decide the whole function", "No: two rational functions can never have the same restrictions"], "correct": 1, "tag": "", "sol": "Restrictions only tell you where a function is undefined; they say nothing about its values elsewhere.\nf(x) = 1/(x − 2) and g(x) = 3/(x − 2) share the restriction x ≠ 2 (and even the same denominator), but f(3) = 1 ≠ 3 = g(3).\nTo be equivalent, two rational functions need the same simplified form <b>and</b> the same restrictions."}]}, {"id": "s5", "label": "2.6 · Multiplying and dividing rationals", "sub": "I can multiply and divide rational expressions, simplify, and state every restriction, including those from the divisor.", "slides": [{"kind": "blank", "p": "<b>Q12(a)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "Numerator: 6x · 2y² = __B1__", "a": {"B1": "12xy^2"}, "expr": true}, {"t": "Denominator: 8y · 3x = __B1__", "a": {"B1": "24xy"}, "expr": true}, {"t": "Simplified: __B1__", "a": {"B1": "y/2"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ and y ≠ __B2__", "a": {"B1": "0", "B2": "0"}}], "sol": "12xy².\n24xy.\n12xy²/(24xy) = y/2 (divide top and bottom by 12xy).\n8y ≠ 0 and 3x ≠ 0, so x ≠ 0 and y ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">8y</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2y²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3x</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q12(b)</b> · Simplify. State any restrictions on the variables.", "opts": ["m; m ≠ 0, n ≠ 0", "m; n ≠ 0", "1/m; m ≠ 0, n ≠ 0", "m²/n; n ≠ 0"], "correct": 0, "tag": "", "sol": "10m² × 6mn = 60m³n and 3n × 20m² = 60m²n.\n60m³n/(60m²n) = m.\nRestrictions from both denominators: 3n ≠ 0 and 20m² ≠ 0, so m ≠ 0 and n ≠ 0 (the m² factor cancelled, but m = 0 is still not allowed).", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">10m²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3n</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6mn</span><span style=\"padding:2px 4px 0;white-space:nowrap\">20m²</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q12(c)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "Multiply by the reciprocal: (2ab)/(5bc) × __B1__", "a": {"B1": "10b/(6ac)"}, "expr": true}, {"t": "Simplified: __B1__", "a": {"B1": "2b/(3c^2)"}, "expr": true}, {"t": "Restrictions: a ≠ __B1__, b ≠ __B2__, c ≠ __B3__", "a": {"B1": "0", "B2": "0", "B3": "0"}}], "sol": "The reciprocal of (6ac)/(10b) is (10b)/(6ac).\n20ab²/(30abc²) = 2b/(3c²).\n5bc ≠ 0 gives b ≠ 0, c ≠ 0; 10b ≠ 0; and the divisor’s numerator 6ac ≠ 0 gives a ≠ 0. So a ≠ 0, b ≠ 0, c ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2ab</span><span style=\"padding:2px 4px 0;white-space:nowrap\">5bc</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6ac</span><span style=\"padding:2px 4px 0;white-space:nowrap\">10b</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q12(d)</b> · Simplify. State any restrictions on the variables.", "opts": ["5p/(32q²); p ≠ 0, q ≠ 0", "{5/2}; p ≠ 0, q ≠ 0", "5/(2p); q ≠ 0", "5/(2p); p ≠ 0, q ≠ 0"], "correct": 3, "tag": "", "sol": "Multiply by the reciprocal: (5p)/(8pq) × (12q)/(3p) = 60pq/(24p²q) = 5/(2p).\nRestrictions: 8pq ≠ 0, 12q ≠ 0 and the divisor’s numerator 3p ≠ 0, so p ≠ 0, q ≠ 0.\n5p/(32q²) multiplies by the divisor instead of its reciprocal; {5/2} cancels p once too often.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">5p</span><span style=\"padding:2px 4px 0;white-space:nowrap\">8pq</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3p</span><span style=\"padding:2px 4px 0;white-space:nowrap\">12q</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q13(a)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "(3x)² = __B1__", "a": {"B1": "9x^2"}, "expr": true}, {"t": "Multiply by the reciprocal: x²/(2xy) × x/(2y²) × __B1__", "a": {"B1": "xy^2/(9x^2)"}, "expr": true}, {"t": "Numerator: x² · x · xy² = __B1__", "a": {"B1": "x^4y^2"}, "expr": true}, {"t": "Denominator: 2xy · 2y² · 9x² = __B1__", "a": {"B1": "36x^3y^3"}, "expr": true}, {"t": "Simplified: __B1__", "a": {"B1": "x/(36y)"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ and y ≠ __B2__", "a": {"B1": "0", "B2": "0"}}], "sol": "(3x)² = 9x², so the divisor is 9x²/(xy²).\nThe reciprocal of 9x²/(xy²) is xy²/(9x²).\nx⁴y².\n36x³y³.\nx⁴y²/(36x³y³) = x/(36y).\n2xy, 2y², xy² and the divisor’s numerator 9x² must not be 0: x ≠ 0, y ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2xy</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2y²</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(3x)²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">xy²</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q13(b)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "x² − 5x + 6 = (x − a)(x − b), where a and b are __B1__", "a": {"B1": "2, 3"}, "expr": "set"}, {"t": "x² − 4x − 5 = (x − 5)(x + __B1__)", "a": {"B1": "1"}}, {"t": "x² + 3x + 2 = (x + 1)(x + __B1__)", "a": {"B1": "2"}}, {"t": "After multiplying by the reciprocal and dividing out common factors: __B1__", "a": {"B1": "(x-3)(x+1)/(x-1)"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-2, -1, 1, 2, 5"}, "expr": "dlist"}], "sol": "(x − 2)(x − 3).\n(x − 5)(x + 1). Also x² − 1 = (x − 1)(x + 1) and x² − 4 = (x − 2)(x + 2).\n(x + 1)(x + 2).\n(x − 2)(x − 3)/((x − 1)(x + 1)) × (x − 5)(x + 1)/((x − 2)(x + 2)) × (x + 1)(x + 2)/(x − 5) = (x − 3)(x + 1)/(x − 1).\nDenominators: x ≠ ±1, ±2; the divisor’s numerator x − 5 ≠ 0: x ≠ 5. So x ≠ −2, −1, 1, 2, 5.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − 5x + 6</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 1</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − 4x − 5</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 4</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x − 5</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 3x + 2</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q13(c)</b> · Simplify. State any restrictions on the variables.", "opts": ["(1 − x)(1 − y)/(y(y + 1)); x ≠ −1, 0; y ≠ −1, 0, 1", "x(x − 1)/(y(y + 1)); x ≠ −1, 0; y ≠ −1", "x(1 − x)/(y(y + 1)); x ≠ −1, 0; y ≠ −1, 0, 1", "x(x − 1)/(y(y + 1)); x ≠ −1, 0; y ≠ −1, 0, 1"], "correct": 3, "tag": "", "sol": "Factor: 1 − x² = (1 − x)(1 + x), 1 − y² = (1 − y)(1 + y), x + x² = x(1 + x), y³ − y = y(y − 1)(y + 1).\nMultiply by the reciprocal x²/(y(y − 1)(y + 1)) and cancel (1 + x), (1 + y) and x: (1 − x)(1 − y)x/(y(y − 1)(y + 1)).\n(1 − y)/(y − 1) = −1, so the result is −x(1 − x)/(y(y + 1)) = x(x − 1)/(y(y + 1)).\nRestrictions: 1 + y ≠ 0, x + x² ≠ 0, x² ≠ 0 and the divisor’s numerator y³ − y ≠ 0: x ≠ −1, 0 and y ≠ −1, 0, 1.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1 − x²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">1 + y</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1 − y²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + x²</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">y³ − y</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x²</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q13(d)</b> · Simplify. State any restrictions on the variables.", "opts": ["(x − y)(2x + 3y)²/(2x − y)²; x ≠ −y, 2x ≠ ±y", "x − y; x ≠ −y, 2x ≠ ±y, 2x ≠ −3y", "x − y; x ≠ −y, 2x ≠ ±y", "y − x; x ≠ −y, 2x ≠ ±y, 2x ≠ −3y"], "correct": 1, "tag": "", "sol": "Factor: x² − y² = (x − y)(x + y), 4x² − y² = (2x − y)(2x + y), 4x² + 8xy + 3y² = (2x + y)(2x + 3y).\nMultiply by the reciprocal (2x − y)/(2x + 3y): everything cancels except x − y.\nRestrictions: 2x − y ≠ 0, 2x + y ≠ 0, x + y ≠ 0 and the divisor’s numerator 2x + 3y ≠ 0 (that is, x ≠ y/2, x ≠ −y/2, x ≠ −y, x ≠ −3y/2).\nThe second option forgets the divisor’s numerator; the third multiplies by the divisor instead of its reciprocal.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">x² − y²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">4x² − y²</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4x² + 8xy + 3y²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + y</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2x + 3y</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x − y</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q15(d)</b> · Simplify and state any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "x² + 6x + 5 = (x + 1)(x + __B1__)", "a": {"B1": "5"}}, {"t": "3x + 15 = 3(x + __B1__)", "a": {"B1": "5"}}, {"t": "(2 − x)² = (x − 2)², so the product simplifies to __B1__", "a": {"B1": "6/(x+1)"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-5, -1, 2"}, "expr": "dlist"}], "sol": "1 × 5 = 5 and 1 + 5 = 6.\nCommon factor 3.\n2(x − 2)² × 3(x + 5)/((x + 1)(x + 5)(x − 2)²) = 6/(x + 1).\nx² + 6x + 5 = 0 at x = −5, −1, and (2 − x)² = 0 at x = 2, so x ≠ −5, −1, 2.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2(x − 2)²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 6x + 5</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3x + 15</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(2 − x)²</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q15(e)</b> · Simplify and state any restrictions on the variables.", "opts": ["(x − 2y)/((x − y)(x + 3y)); x ≠ ±y, x ≠ 2y, x ≠ −3y", "(x − 2y)³(x + 3y)/((x − y)(x + y)³); x ≠ ±y", "(x − 2y)(x + y)/((x − y)(x + 3y)); x ≠ ±y", "(x − 2y)(x + y)/((x − y)(x + 3y)); x ≠ ±y, x ≠ 2y, x ≠ −3y"], "correct": 3, "tag": "", "sol": "Multiply by the reciprocal: (x − 2y)²/((x − y)(x + y)) × (x + y)²/((x − 2y)(x + 3y)).\nCancel one (x − 2y) and one (x + y): (x − 2y)(x + y)/((x − y)(x + 3y)).\nRestrictions: x² − y² ≠ 0 (x ≠ ±y), (x + y)² ≠ 0 (x ≠ −y) and the divisor’s numerator (x − 2y)(x + 3y) ≠ 0 (x ≠ 2y, x ≠ −3y).\nThe second option forgets the divisor’s numerator; the last cancels (x + y)² completely against a single (x + y).", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x − 2y)²</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − y²</span></span></span><span>÷</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">(x − 2y)(x + 3y)</span><span style=\"padding:2px 4px 0;white-space:nowrap\">(x + y)²</span></span></span></div></div>"}]}, {"id": "s6", "label": "2.7 · Adding and subtracting rationals", "sub": "I can add and subtract rational expressions using the lowest common denominator, simplify, and state the restrictions.", "slides": [{"kind": "blank", "p": "<b>Q14(a)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "The LCD is 15x, and 4/(5x) = __B1__/(15x)", "a": {"B1": "12"}}, {"t": "2/(3x) = __B1__/(15x)", "a": {"B1": "10"}}, {"t": "Difference: __B1__", "a": {"B1": "2/(15x)"}, "expr": true}, {"t": "Restriction: x ≠ __B1__", "a": {"B1": "0"}}], "sol": "Multiply top and bottom by 3: 12/(15x).\nMultiply top and bottom by 5: 10/(15x).\n(12 − 10)/(15x) = 2/(15x).\n5x ≠ 0 and 3x ≠ 0: x ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4</span><span style=\"padding:2px 4px 0;white-space:nowrap\">5x</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3x</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q14(b)</b> · Simplify. State any restrictions on the variables.", "opts": ["(3x − 7)/((x + 1)(x − 1)); x ≠ −1, 1", "{3/2}; x ≠ −1, 1", "3/(x + 1); x ≠ −1, 1", "(3x − 7)/(x² + 1); x ≠ −1, 1"], "correct": 0, "tag": "", "sol": "LCD (x + 1)(x − 1): numerator 5(x − 1) − 2(x + 1) = 5x − 5 − 2x − 2 = 3x − 7.\nSo (3x − 7)/((x + 1)(x − 1)), x ≠ −1, 1.\n3/(x + 1) comes from 5x − 5 − 2x + 2 = 3x − 3 (the −2 was not multiplied by every term); {3/2} subtracts tops and bottoms; (x + 1)(x − 1) is x² − 1, not x² + 1.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">5</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 1</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 1</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q14(c)</b> · Simplify. State any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "x² + 3x − 4 = (x + 4)(__B1__)", "a": {"B1": "x-1"}, "expr": true}, {"t": "x² + x − 12 = (x + 4)(__B1__)", "a": {"B1": "x-3"}, "expr": true}, {"t": "Numerator over the LCD (x + 4)(x − 1)(x − 3): (x − 3) + (x − 1) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x-4"}, "expr": "expanded"}, {"t": "Simplified: __B1__", "a": {"B1": "2(x-2)/((x+4)(x-1)(x-3))"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-4, 1, 3"}, "expr": "dlist"}], "sol": "4 × (−1) = −4 and 4 − 1 = 3.\n4 × (−3) = −12 and 4 − 3 = 1.\nEach fraction is missing one factor: 1·(x − 3) + 1·(x − 1) = 2x − 4.\n(2x − 4)/((x + 4)(x − 1)(x − 3)) = 2(x − 2)/((x + 4)(x − 1)(x − 3)).\nx ≠ −4, 1, 3.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + 3x − 4</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + x − 12</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q14(d)</b> · Simplify. State any restrictions on the variables.", "opts": ["5/((x − 2)(x − 3)(x + 3)); x ≠ −3, 2, 3", "5/((x − 2)(x + 3)); x ≠ −3, 2", "1/((x − 2)(x − 3)(x + 3)); x ≠ −3, 2, 3", "5/((x − 2)(x − 3)(x + 3)); x ≠ 2, 3"], "correct": 0, "tag": "", "sol": "x² − 5x + 6 = (x − 2)(x − 3) and x² − 9 = (x − 3)(x + 3). LCD: (x − 2)(x − 3)(x + 3).\nNumerator: (x + 3) − (x − 2) = x + 3 − x + 2 = 5.\nSo 5/((x − 2)(x − 3)(x + 3)), x ≠ −3, 2, 3. Writing x + 3 − x − 2 = 1 forgets the bracket round (x − 2).", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 5x + 6</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 9</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q15(a)</b> · Simplify and state any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "LCD = __B1__", "a": {"B1": "6x^3"}, "expr": true}, {"t": "Over 6x³ the numerators are 3x², −14x and __B1__", "a": {"B1": "24"}}, {"t": "Simplified: __B1__", "a": {"B1": "(3x^2-14x+24)/(6x^3)"}, "expr": true}, {"t": "Restriction: x ≠ __B1__", "a": {"B1": "0"}}], "sol": "The LCD of 2x, 3x² and x³ is 6x³.\n1/(2x) = 3x²/(6x³), 7/(3x²) = 14x/(6x³), 4/x³ = 24/(6x³).\n(3x² − 14x + 24)/(6x³). (3x² − 14x + 24 does not factor.)\nx ≠ 0.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">1</span><span style=\"padding:2px 4px 0;white-space:nowrap\">2x</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">7</span><span style=\"padding:2px 4px 0;white-space:nowrap\">3x²</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x³</span></span></span></div></div>"}, {"kind": "mcq", "text": "<b>Q15(b)</b> · Simplify and state any restrictions on the variables.", "opts": ["x(7x − 10)/((x + 2)(x − 6)); x ≠ 0, −2, 6", "(7x² − 26x)/((x + 2)(x − 6)); x ≠ −2, 6", "7x/(2x − 4); x ≠ 2", "x(7x − 10)/((x + 2)(x − 6)); x ≠ −2, 6"], "correct": 3, "tag": "", "sol": "LCD (x + 2)(x − 6): numerator 3x(x − 6) + 4x(x + 2) = 3x² − 18x + 4x² + 8x = 7x² − 10x = x(7x − 10).\nSo x(7x − 10)/((x + 2)(x − 6)), with x ≠ −2, 6.\n7x/(2x − 4) adds tops and bottoms; x = 0 makes the numerator 0, which is allowed.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x + 2</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">4x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x − 6</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q15(c)</b> · Simplify and state any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "x² − 5x + 6 = (x − 2)(__B1__)", "a": {"B1": "x-3"}, "expr": true}, {"t": "x² + x − 12 = (x − 3)(__B1__)", "a": {"B1": "x+4"}, "expr": true}, {"t": "Numerator over the LCD (x − 2)(x − 3)(x + 4): 6x(x + 4) − 3x(x − 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3x^2+30x"}, "expr": "expanded"}, {"t": "Simplified: __B1__", "a": {"B1": "3x(x+10)/((x-2)(x-3)(x+4))"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-4, 2, 3"}, "expr": "dlist"}], "sol": "(x − 2)(x − 3).\n(x − 3)(x + 4).\n6x² + 24x − 3x² + 6x = 3x² + 30x.\n3x(x + 10)/((x − 2)(x − 3)(x + 4)).\nx ≠ −4, 2, 3.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">6x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² − 5x + 6</span></span></span><span>−</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3x</span><span style=\"padding:2px 4px 0;white-space:nowrap\">x² + x − 12</span></span></span></div></div>"}, {"kind": "blank", "p": "<b>Q15(f)</b> · Simplify and state any restrictions on the variables.", "tag": "", "marks": "", "flat": [{"t": "Multiply first: 3b/(b² + b − 30) × (b² + 8b + 12)/(b + 3) = __B1__", "a": {"B1": "3b(b+2)/((b-5)(b+3))"}, "expr": true}, {"t": "b² − 2b − 15 = (b − 5)(__B1__)", "a": {"B1": "b+3"}, "expr": true}, {"t": "Add over (b − 5)(b + 3): numerator (2b − 5) + 3b(b + 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3b^2+8b-5"}, "expr": "expanded"}, {"t": "Simplified: __B1__", "a": {"B1": "(3b^2+8b-5)/((b-5)(b+3))"}, "expr": true}, {"t": "Restrictions: b ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-6, -3, 5"}, "expr": "dlist"}], "sol": "Multiplication comes before addition. (b + 6)(b + 2) × 3b/((b + 6)(b − 5)(b + 3)) = 3b(b + 2)/((b − 5)(b + 3)).\n(b − 5)(b + 3).\n2b − 5 + 3b² + 6b = 3b² + 8b − 5.\n(3b² + 8b − 5)/((b − 5)(b + 3)); 3b² + 8b − 5 does not factor over the integers.\nb² − 2b − 15 = 0 at b = 5, −3; b² + b − 30 = 0 at b = −6, 5; b + 3 = 0 at b = −3. So b ≠ −6, −3, 5.", "fig": "<div style=\"max-width:100%;min-width:0;overflow-x:auto;-webkit-overflow-scrolling:touch\"><div style=\"display:inline-flex;align-items:center;gap:4px;padding:6px 4px;white-space:nowrap;font-size:17px;color:var(--ink)\"><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">2b − 5</span><span style=\"padding:2px 4px 0;white-space:nowrap\">b² − 2b − 15</span></span></span><span>+</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">3b</span><span style=\"padding:2px 4px 0;white-space:nowrap\">b² + b − 30</span></span></span><span>×</span><span><span style=\"display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 3px;line-height:1.35\"><span style=\"padding:0 4px 2px;border-bottom:1.5px solid currentColor;white-space:nowrap\">b² + 8b + 12</span><span style=\"padding:2px 4px 0;white-space:nowrap\">b + 3</span></span></span></div></div>"}]}, {"id": "s7", "label": "Problem solving", "sub": "I can model a situation with rational expressions, simplify and solve, and judge whether the answer makes sense.", "slides": [{"kind": "blank", "p": "<b>Q16</b> · Fred’s final mark in an online course was determined entirely by two exams. The mid-term exam was out of x marks and was worth 25% of his final mark. The final exam was out of 2x marks and was worth 75% of his final mark. Fred scored 40 marks on the first exam and 60 marks on the second exam. Determine the value of x if Fred earned a final mark of 50% in the course.", "tag": "", "marks": "", "flat": [{"t": "Mid-term as a fraction of full marks: __B1__", "a": {"B1": "40/x"}, "expr": true}, {"t": "Final exam as a fraction: 60/(2x) = __B1__", "a": {"B1": "30/x"}, "expr": true}, {"t": "Weighted final mark: 0.25 × 40/x + 0.75 × 30/x = __B1__", "a": {"B1": "32.5/x"}, "expr": true}, {"t": "Solve 32.5/x = 0.5: x = __B1__", "a": {"B1": "65"}}], "sol": "40 out of x is 40/x.\n60/(2x) = 30/x.\n10/x + 22.5/x = 32.5/x.\n32.5 = 0.5x, so x = 65. Check: 0.25(40/65) + 0.75(60/130) = 10/65 + 22.5/65 = 32.5/65 = 0.5 ✓ and 40 ≤ 65, 60 ≤ 130 ✓"}, {"kind": "blank", "p": "<b>Q17(a)</b> · Sam plays a game in which he selects three different numbers from 1 to n (n > 3). After he selects his numbers, four different winning numbers from 1 to n are chosen, one at a time. Sam wins if all three of his numbers are among the four winning numbers. The first number chosen is one of Sam’s! His probability of winning is now given by P(n) = 24/(n³ − 3n² + 2n) ÷ 3/n. Simplify P(n) and state the restrictions on n.", "tag": "", "marks": "", "flat": [{"t": "n³ − 3n² + 2n = n(n − a)(n − b), where a and b are __B1__", "a": {"B1": "1, 2"}, "expr": "set"}, {"t": "Dividing by 3/n is the same as multiplying by __B1__", "a": {"B1": "n/3"}, "expr": true}, {"t": "P(n) = __B1__", "a": {"B1": "8/((n-1)(n-2))"}, "expr": true}, {"t": "Restrictions: n ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "0, 1, 2"}, "expr": "dlist"}], "sol": "n(n² − 3n + 2) = n(n − 1)(n − 2).\nThe reciprocal of 3/n is n/3.\n24/(n(n − 1)(n − 2)) × n/3 = 8/((n − 1)(n − 2)).\nn(n − 1)(n − 2) ≠ 0 and 3/n needs n ≠ 0: n ≠ 0, 1, 2. In the game n is also a whole number greater than 3."}, {"kind": "mcq", "text": "<b>Q17(b)(i)</b> · What would Sam’s probability of winning be if n = 5? (Use the simplified formula P(n) = 8/((n − 1)(n − 2)).)", "opts": ["{1/3}", "{8/15}", "{2/3}", "{2/5}"], "correct": 2, "tag": "", "sol": "P(5) = 8/((5 − 1)(5 − 2)) = 8/12 = {2/3}.\n{2/5} is 24/(125 − 75 + 10) = 24/60, the value before dividing by 3/n; {8/15} uses 5 × 3 in the denominator.\nCaution: see Q17(b)(ii). The book’s formula is too large by a factor of {4/3}; the true probability for n = 5 is 6/(4 × 3) = {1/2}."}, {"kind": "blank", "p": "<b>Q17(b)(ii)</b> · What would Sam’s probability of winning be if n = 4? Use the formula first.", "tag": "", "marks": "", "flat": [{"t": "P(4) = 8/((4 − 1)(4 − 2)) = __B1__", "a": {"B1": "4/3"}}, {"t": "Can a probability be greater than 1? (yes / no) __B1__", "a": {"B1": "no"}, "expr": "words"}], "sol": "8/(3 × 2) = 8/6 = {4/3}.\nNo. Every probability is between 0 and 1, so {4/3} cannot be right: the formula itself must be wrong (see the next question)."}, {"kind": "mcq", "text": "<b>Q17(b)(ii)</b> · The formula gives P(4) = {4/3}. What is going on?", "opts": ["{4/3} > 1 is impossible: with n = 4 all four numbers are winners, so P(4) = 1; the given formula overstates P(n)", "Sam’s probability really is {4/3}, because he has 3 numbers out of 4", "Nothing: a probability can be larger than 1 when n is small", "n = 4 is a restriction, so P(4) is undefined"], "correct": 0, "tag": "", "sol": "If n = 4, the four winning numbers are all of 1, 2, 3, 4, so Sam is certain to win: the probability is 1.\nThe book’s P(n) divides P(win) = 24/(n(n − 1)(n − 2)) by P(first number is Sam’s) = 3/n. That would be right only if every win started with one of Sam’s numbers; in fact, when Sam wins, the first number drawn is his with probability {3/4}.\nCorrect model: given the first number is Sam’s, the other 3 winning numbers come from the remaining n − 1 and must include Sam’s other two, so P = (n − 3) ÷ [(n − 1)(n − 2)(n − 3)/6] = 6/((n − 1)(n − 2)) = {3/4} × 8/((n − 1)(n − 2)).\nThis gives P(4) = 1 ✓ and P(5) = {1/2}. The algebra in Q17(a) is correct; the formula given in the question is not."}, {"kind": "mcq", "text": "Riya cycles 24 km to a lake at x km/h and returns at (x − 4) km/h. Which expression is her total travel time in hours?", "opts": ["24/(x(x − 4))", "48(x − 2)/(x(x − 4))", "48/(2x − 4)", "48(x − 2)/(x − 4)"], "correct": 1, "tag": "", "sol": "Time = distance ÷ speed: 24/x + 24/(x − 4).\nLCD x(x − 4): (24(x − 4) + 24x)/(x(x − 4)) = (48x − 96)/(x(x − 4)) = 48(x − 2)/(x(x − 4)), x ≠ 0, 4 (and x > 4 in context).\n48/(2x − 4) adds tops and bottoms."}, {"kind": "blank", "p": "Use Riya’s trip time T(x) = 24/x + 24/(x − 4).", "tag": "", "marks": "", "flat": [{"t": "Simplified T(x) = __B1__", "a": {"B1": "48(x-2)/(x(x-4))"}, "expr": true}, {"t": "T(12) = __B1__ hours", "a": {"B1": "5"}}], "sol": "(24(x − 4) + 24x)/(x(x − 4)) = 48(x − 2)/(x(x − 4)).\n48(10)/(12 × 8) = 480/96 = 5 h. Check: 24/12 + 24/8 = 2 + 3 = 5 ✓"}, {"kind": "mcq", "text": "A rectangle has area (x² + 7x + 12) cm² and width (x + 3) cm. What is its length?", "opts": ["(x + 4) cm", "(x + 9) cm", "(x − 4) cm", "(x² + 4) cm"], "correct": 0, "tag": "", "sol": "Length = area ÷ width = (x² + 7x + 12)/(x + 3) = (x + 3)(x + 4)/(x + 3) = x + 4, x ≠ −3.\nx + 9 comes from cancelling terms (7x + 12 − 3x …), not factors."}, {"kind": "blank", "p": "A quiz is out of x marks and worth 40% of a final mark; a project is out of 3x marks and worth 60%. Lena scores 18 on the quiz and 45 on the project, and her final mark is 60%. Find x.", "tag": "", "marks": "", "flat": [{"t": "Weighted mark: 0.4 × 18/x + 0.6 × 45/(3x) = __B1__", "a": {"B1": "16.2/x"}, "expr": true}, {"t": "Solve 16.2/x = 0.6: x = __B1__", "a": {"B1": "27"}}], "sol": "7.2/x + 0.6 × 15/x = 7.2/x + 9/x = 16.2/x.\n16.2 = 0.6x, so x = 27. Check: 18 ≤ 27 and 45 ≤ 81 ✓"}]}, {"id": "s8", "label": "Assessment A", "sub": "Knowing and understanding", "slides": [{"kind": "mcq", "text": "Simplify (3x² − 5x + 2) − (x² − 2x + 7).", "opts": ["2x² − 7x − 5", "4x² − 7x + 9", "2x² − 3x + 9", "2x² − 3x − 5"], "correct": 3, "tag": "", "sol": "= 3x² − 5x + 2 − x² + 2x − 7 = 2x² − 3x − 5.\n2x² − 7x − 5 leaves −2x unchanged; 2x² − 3x + 9 leaves +7 unchanged; 4x² − 7x + 9 adds."}, {"kind": "blank", "p": "Expand and simplify (2x + 3)(x² − x + 4).", "tag": "", "marks": "", "flat": [{"t": "2x(x² − x + 4) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x^3-2x^2+8x"}, "expr": "expanded"}, {"t": "3(x² − x + 4) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "3x^2-3x+12"}, "expr": "expanded"}, {"t": "Sum: __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "2x^3+x^2+5x+12"}, "expr": "expanded"}], "sol": "2x³ − 2x² + 8x.\n3x² − 3x + 12.\n2x³ + x² + 5x + 12."}, {"kind": "mcq", "text": "Factor 6x² − x − 2.", "opts": ["(6x + 1)(x − 2)", "(2x − 1)(3x + 2)", "(3x + 1)(2x − 2)", "(2x + 1)(3x − 2)"], "correct": 3, "tag": "", "sol": "ac = −12; two numbers with product −12 and sum −1: −4 and 3.\n6x² − 4x + 3x − 2 = 2x(3x − 2) + 1(3x − 2) = (2x + 1)(3x − 2).\n(2x − 1)(3x + 2) = 6x² + x − 2 (wrong middle sign)."}, {"kind": "blank", "p": "Simplify (x² − 9)/(x² + 5x + 6) and state the restrictions.", "tag": "", "marks": "", "flat": [{"t": "x² − 9 = (x − 3)(x + __B1__)", "a": {"B1": "3"}}, {"t": "x² + 5x + 6 = (x + 2)(x + __B1__)", "a": {"B1": "3"}}, {"t": "Simplified: __B1__", "a": {"B1": "(x-3)/(x+2)"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-3, -2"}, "expr": "dlist"}], "sol": "Difference of squares.\n2 × 3 = 6, 2 + 3 = 5.\n(x − 3)(x + 3)/((x + 2)(x + 3)) = (x − 3)/(x + 2).\nx ≠ −3, −2 (x = −3 stays excluded after cancelling)."}, {"kind": "mcq", "text": "Simplify (4x²)/(3y) × (9y²)/(8x) and state the restrictions.", "opts": ["3xy/2; x ≠ 0, y ≠ 0", "3x²y²/2; x ≠ 0, y ≠ 0", "2/(3xy); x ≠ 0, y ≠ 0", "3xy/2; y ≠ 0"], "correct": 0, "tag": "", "sol": "36x²y²/(24xy) = 3xy/2.\nBoth denominators must be non-zero: 3y ≠ 0 and 8x ≠ 0, so x ≠ 0, y ≠ 0."}, {"kind": "blank", "p": "Simplify 3/(x − 2) + 2/(x + 1) and state the restrictions.", "tag": "", "marks": "", "flat": [{"t": "LCD = __B1__", "a": {"B1": "(x-2)(x+1)"}, "expr": true}, {"t": "Numerator: 3(x + 1) + 2(x − 2) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "5x-1"}, "expr": "expanded"}, {"t": "Simplified: __B1__", "a": {"B1": "(5x-1)/((x-2)(x+1))"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-1, 2"}, "expr": "dlist"}], "sol": "(x − 2)(x + 1).\n3x + 3 + 2x − 4 = 5x − 1.\n(5x − 1)/((x − 2)(x + 1)).\nx ≠ −1, 2."}, {"kind": "mcq", "text": "What are all the restrictions on (x + 4)/(x − 1) ÷ (x + 4)/(x + 2)?", "opts": ["x ≠ −2, 1", "x ≠ −4, −2, 1", "x ≠ −4, 1", "x ≠ 1"], "correct": 1, "tag": "", "sol": "Denominators: x − 1 ≠ 0 and x + 2 ≠ 0. The divisor’s numerator x + 4 ≠ 0 too, because it becomes a denominator.\nSo x ≠ −4, −2, 1. (The quotient simplifies to (x + 2)/(x − 1).)"}, {"kind": "blank", "p": "Expand (x − 3)³.", "tag": "", "marks": "", "flat": [{"t": "(x − 3)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^2-6x+9"}, "expr": "expanded"}, {"t": "(x² − 6x + 9)(x − 3) = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^3-9x^2+27x-27"}, "expr": "expanded"}], "sol": "x² − 6x + 9.\nx³ − 3x² − 6x² + 18x + 9x − 27 = x³ − 9x² + 27x − 27."}]}, {"id": "s9", "label": "Assessment B", "sub": "Investigating patterns", "slides": [{"kind": "mcq", "text": "(x − 1)(x + 1) = x² − 1 and (x − 1)(x² + x + 1) = x³ − 1. Following the pattern, what is (x − 1)(x³ + x² + x + 1)?", "opts": ["x⁴ + 1", "x⁴ − 2x + 1", "x⁴ − x − 1", "x⁴ − 1"], "correct": 3, "tag": "", "sol": "Multiply: x⁴ + x³ + x² + x − x³ − x² − x − 1 = x⁴ − 1. All the middle terms cancel in pairs, just as in the first two products."}, {"kind": "blank", "p": "Test whether f(x) = (x + 2)² and g(x) = x² + 4 are equivalent.", "tag": "", "marks": "", "flat": [{"t": "f(0) = __B1__ and g(0) = __B2__", "a": {"B1": "4", "B2": "4"}}, {"t": "f(1) = __B1__ and g(1) = __B2__", "a": {"B1": "9", "B2": "5"}}, {"t": "Equivalent? (yes / no) __B1__", "a": {"B1": "no"}, "expr": "words"}], "sol": "(0 + 2)² = 4 and 0 + 4 = 4.\n(1 + 2)² = 9 but 1 + 4 = 5.\nNo: one counterexample (x = 1) is enough. (x + 2)² = x² + 4x + 4."}, {"kind": "mcq", "text": "f(x) = (x² − 4)/(x − 2) and g(x) = x + 2. Which statement is true?", "opts": ["They are equal for every x except x = 2, where f is undefined", "They are equal only for x > 2", "They are never equal", "They are equivalent for all real x"], "correct": 0, "tag": "", "sol": "f(x) = (x − 2)(x + 2)/(x − 2) = x + 2 for x ≠ 2. At x = 2, f is undefined but g(2) = 4, so the functions are not equivalent: they differ by one missing point."}, {"kind": "blank", "p": "Explore the pattern 1/n − 1/(n + 1).", "tag": "", "marks": "", "flat": [{"t": "1/n − 1/(n + 1) = __B1__", "a": {"B1": "1/(n(n+1))"}, "expr": true}, {"t": "So 1/(1·2) + 1/(2·3) + … + 1/(9·10) = (1 − {1/2}) + ({1/2} − {1/3}) + … + ({1/9} − {1/10}) = __B1__", "a": {"B1": "9/10"}}], "sol": "(n + 1 − n)/(n(n + 1)) = 1/(n(n + 1)).\nEvery middle term cancels, leaving 1 − {1/10} = {9/10}."}, {"kind": "mcq", "text": "Which expression is equal to (n + 1)² − n² for every n?", "opts": ["2n² + 2n + 1", "2n", "1", "2n + 1"], "correct": 3, "tag": "", "sol": "(n + 1)² − n² = n² + 2n + 1 − n² = 2n + 1. So consecutive squares differ by consecutive odd numbers: 1, 4, 9, 16 differ by 3, 5, 7."}, {"kind": "blank", "p": "Powers of (x + 1).", "tag": "", "marks": "", "flat": [{"t": "(x + 1)³ = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^3+3x^2+3x+1"}, "expr": "expanded"}, {"t": "(x + 1)⁴ = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "x^4+4x^3+6x^2+4x+1"}, "expr": "expanded"}, {"t": "The coefficients of (x + 1)⁴ add up to __B1__", "a": {"B1": "16"}}], "sol": "Coefficients 1, 3, 3, 1.\n(x³ + 3x² + 3x + 1)(x + 1): coefficients 1, 4, 6, 4, 1 (Pascal’s triangle).\n1 + 4 + 6 + 4 + 1 = 16 = 2⁴ (put x = 1)."}, {"kind": "mcq", "text": "As x gets very large, what value does (2x + 1)/(x − 3) get close to?", "opts": ["2", "0", "−{1/3}", "It keeps growing"], "correct": 0, "tag": "", "sol": "Divide top and bottom by x: (2 + 1/x)/(1 − 3/x). As x grows, 1/x and 3/x shrink to 0, so the value approaches 2/1 = 2. For example, x = 1000 gives 2001/997 ≈ 2.007."}, {"kind": "blank", "p": "Prove the identity (a + b)² − (a − b)² = 4ab and use it.", "tag": "", "marks": "", "flat": [{"t": "(a + b)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "a^2+2ab+b^2"}, "expr": "expanded"}, {"t": "(a − b)² = __B1__ <i>(expanded form, no brackets)</i>", "a": {"B1": "a^2-2ab+b^2"}, "expr": "expanded"}, {"t": "Difference: __B1__", "a": {"B1": "4ab"}, "expr": true}, {"t": "Use a = 50, b = 1: 51² − 49² = __B1__", "a": {"B1": "200"}}], "sol": "a² + 2ab + b².\na² − 2ab + b².\nThe a² and b² cancel: 4ab.\n4 × 50 × 1 = 200 (2601 − 2401 = 200 ✓)."}]}, {"id": "s10", "label": "Assessment C", "sub": "Communicating", "slides": [{"kind": "mcq", "text": "Which of these is a rational function?", "opts": ["f(x) = 1/√(x + 2)", "f(x) = (x² + 1)/(x − 3)", "f(x) = 2ˣ − 1", "f(x) = √x + 1"], "correct": 1, "tag": "", "sol": "A rational function is a quotient of two polynomials. (x² + 1)/(x − 3) is one. √x and 2ˣ are not polynomials, so the others are not rational functions."}, {"kind": "blank", "p": "Complete the sentences.", "tag": "", "marks": "", "flat": [{"t": "Values of a variable that make a denominator zero are called __B1__.", "a": {"B1": "restrictions"}, "expr": "words", "accept": ["restriction", "excluded values", "non-permissible values", "nonpermissible values"]}, {"t": "Two expressions that give the same value for every value of the variable are __B1__.", "a": {"B1": "equivalent"}, "expr": "words"}], "sol": "They are the restrictions (excluded values).\nThey are equivalent expressions."}, {"kind": "mcq", "text": "<b>Error analysis.</b> Jai writes (x + 6)/(x + 3) = 2, “because the x’s cancel and 6 ÷ 3 = 2”. Which comment is correct?", "opts": ["Wrong: only common factors cancel, and (x + 6)/(x + 3) has none, so it cannot be simplified", "Wrong: the answer is 3, not 2", "Right, but only when x > 0", "Right: cancel x, then divide 6 by 3"], "correct": 0, "tag": "", "sol": "x is a term of x + 6, not a factor, so it cannot be cancelled. Test x = 1: 7/4 ≠ 2. (x + 6)/(x + 3) is already in simplest form, with x ≠ −3."}, {"kind": "blank", "p": "<b>Spot the error.</b> (5x + 2) − (3x − 4)   Line 1: = 5x + 2 − 3x − 4   Line 2: = 2x − 2", "tag": "", "marks": "", "flat": [{"t": "The first wrong line is Line __B1__", "a": {"B1": "1"}}, {"t": "The correct answer is __B1__", "a": {"B1": "2x+6"}, "expr": true}], "sol": "Line 1 changed the sign of 3x but not of −4: −(3x − 4) = −3x + 4.\n5x + 2 − 3x + 4 = 2x + 6."}, {"kind": "mcq", "text": "Why must restrictions be found from the original expression, before cancelling?", "opts": ["Because cancelling changes the value of the expression everywhere", "Cancelling can remove a factor that makes the denominator zero, but the original expression is still undefined there", "It does not matter: the simplified form always has the same restrictions", "Because restrictions only come from the numerator"], "correct": 1, "tag": "", "sol": "Example: (x − 1)(x + 2)/(x − 1) simplifies to x + 2, which has no restriction, but the original is undefined at x = 1. So write x ≠ 1 with the simplified form."}, {"kind": "blank", "p": "Explain how to divide 2x/(x + 5) ÷ 4x/(x + 5).", "tag": "", "marks": "", "flat": [{"t": "To divide, multiply by the __B1__ of the divisor.", "a": {"B1": "reciprocal"}, "expr": "words", "accept": ["reciprocal of the divisor", "flip"]}, {"t": "Simplified result: __B1__", "a": {"B1": "1/2"}, "expr": true}, {"t": "Restrictions: x ≠ __B1__ (in increasing order, separated by commas)", "a": {"B1": "-5, 0"}, "expr": "dlist"}], "sol": "Multiply by the reciprocal (x + 5)/(4x).\n2x(x + 5)/((x + 5)(4x)) = {1/2}.\nx + 5 ≠ 0 and the divisor’s numerator 4x ≠ 0: x ≠ −5, 0."}, {"kind": "mcq", "text": "<b>Error analysis.</b> Mia says (x + 3)² = x² + 9. Which reply is correct?", "opts": ["Wrong: (x + 3)² = x² + 3x + 9", "Wrong: (x + 3)² = x² + 6x + 9; for x = 1, (1 + 3)² = 16 but 1 + 9 = 10", "Right when x is positive", "Right: square each term"], "correct": 1, "tag": "", "sol": "(x + 3)(x + 3) = x² + 3x + 3x + 9 = x² + 6x + 9. One value (x = 1) shows that x² + 9 is not equivalent."}, {"kind": "blank", "p": "<b>Spot the error.</b> 3/x − (x − 2)/x   Line 1: = (3 − x − 2)/x   Line 2: = (1 − x)/x", "tag": "", "marks": "", "flat": [{"t": "The first wrong line is Line __B1__", "a": {"B1": "1"}}, {"t": "The correct simplified form is __B1__", "a": {"B1": "(5-x)/x"}, "expr": true}], "sol": "The whole numerator x − 2 is subtracted: 3 − (x − 2) = 3 − x + 2.\n(5 − x)/x, with x ≠ 0."}]}, {"id": "s11", "label": "Assessment D", "sub": "Applying mathematics in real-life contexts", "slides": [{"kind": "mcq", "text": "A 20 cm by 30 cm card has a square of side x cm cut from each corner and is folded into an open box. Which is its volume in cm³?", "opts": ["600x − 4x³", "4x³ + 100x² + 600x", "4x³ − 100x² + 600", "4x³ − 100x² + 600x"], "correct": 3, "tag": "", "sol": "The base is (20 − 2x) by (30 − 2x) and the height is x.\n(20 − 2x)(30 − 2x) = 600 − 100x + 4x², so V = x(600 − 100x + 4x²) = 4x³ − 100x² + 600x (0 < x < 10)."}, {"kind": "blank", "p": "A driver goes 120 km at x km/h and returns at (x + 20) km/h.", "tag": "", "marks": "", "flat": [{"t": "Total time T = __B1__ (one fraction)", "a": {"B1": "240(x+10)/(x(x+20))"}, "expr": true}, {"t": "T when x = 60: __B1__ hours", "a": {"B1": "7/2"}}], "sol": "(120(x + 20) + 120x)/(x(x + 20)) = (240x + 2400)/(x(x + 20)) = 240(x + 10)/(x(x + 20)).\n240(70)/(60 × 80) = 3.5 h (2 h + 1.5 h ✓)."}, {"kind": "mcq", "text": "A ₹1500 bus hire is shared equally by n students. If 5 more students join, by how much does each student’s share go down?", "opts": ["₹1500/(n(n + 5))", "₹7500/(n(n + 5))", "−₹7500/(n(n + 5))", "₹300"], "correct": 1, "tag": "", "sol": "Decrease = 1500/n − 1500/(n + 5) = (1500(n + 5) − 1500n)/(n(n + 5)) = 7500/(n(n + 5)).\nFor n = 25: 60 − 50 = ₹10, and 7500/(25 × 30) = 10 ✓. ₹300 is 1500 ÷ 5."}, {"kind": "blank", "p": "A rectangular garden is (3x + 2) m long and (2x − 1) m wide.", "tag": "", "marks": "", "flat": [{"t": "Area = __B1__ m² <i>(expanded form, no brackets)</i>", "a": {"B1": "6x^2+x-2"}, "expr": "expanded"}, {"t": "Area when x = 4: __B1__ m²", "a": {"B1": "98"}}], "sol": "6x² − 3x + 4x − 2 = 6x² + x − 2.\n6(16) + 4 − 2 = 98 m² (14 m × 7 m ✓)."}, {"kind": "mcq", "text": "Pipe A fills a tank in x hours and pipe B in (x + 2) hours. What fraction of the tank do they fill together in one hour?", "opts": ["2/(2x + 2)", "(2x + 2)/(x + 2)", "(2x + 2)/(x(x + 2))", "1/(2x + 2)"], "correct": 2, "tag": "", "sol": "In one hour A fills 1/x and B fills 1/(x + 2). Together: 1/x + 1/(x + 2) = (x + 2 + x)/(x(x + 2)) = (2x + 2)/(x(x + 2)).\n2/(2x + 2) adds tops and bottoms."}, {"kind": "blank", "p": "An assignment is out of x marks and worth 30%; an exam is out of 4x marks and worth 70%. Kabir scores 24 and 80 and finishes with 53%. Find x.", "tag": "", "marks": "", "flat": [{"t": "Weighted mark: 0.3 × 24/x + 0.7 × 80/(4x) = __B1__", "a": {"B1": "21.2/x"}, "expr": true}, {"t": "Solve 21.2/x = 0.53: x = __B1__", "a": {"B1": "40"}}], "sol": "7.2/x + 14/x = 21.2/x.\nx = 21.2 ÷ 0.53 = 40. Check: 24 ≤ 40 and 80 ≤ 160 ✓"}, {"kind": "mcq", "text": "Making n posters costs ₹(500 + 20n). What is the average cost per poster when 50 are made?", "opts": ["₹1500", "₹520", "₹30", "₹20"], "correct": 2, "tag": "", "sol": "Average cost = (500 + 20n)/n = 500/n + 20. For n = 50: 10 + 20 = ₹30.\n₹1500 is the total cost; ₹20 ignores the fixed ₹500."}, {"kind": "blank", "p": "A triangular sail has base (2x + 6) m and height (x − 1) m.", "tag": "", "marks": "", "flat": [{"t": "Area = __B1__ m² <i>(expanded form, no brackets)</i>", "a": {"B1": "x^2+2x-3"}, "expr": "expanded"}, {"t": "Area when x = 5: __B1__ m²", "a": {"B1": "32"}}], "sol": "{1/2}(2x + 6)(x − 1) = (x + 3)(x − 1) = x² + 2x − 3.\n25 + 10 − 3 = 32 m² ({1/2} × 16 × 4 ✓)."}]}];
/* ================= build slide lists ================= */
var SLIDES = {}; SECTIONS.forEach(function(sec){ SLIDES[sec.id]=sec.slides; });
var TAB_DEFS = SECTIONS.map(function(sec){ return {id:sec.id, label:sec.label, sub:sec.sub}; });

/* ================= state ================= */
function blankItem(slide){
  if(slide.kind==='mcq'||slide.kind==='ar'){
    return {status:'unanswered', attempts:0, choice:undefined};
  }
  return {status:'unanswered', curStep:0, stepStates: slide.flat.map(function(){ return {status:'unanswered', attempts:0, inputs:{}}; })};
}
function defaultState(){
  var s={tabs:{}};
  TAB_DEFS.forEach(function(td){
    s.tabs[td.id] = { idx:0, maxReached:0, items: SLIDES[td.id].map(function(sl){ return blankItem(sl); }) };
  });
  return s;
}
var appState = {mode:null, learning:null, quiz:null};
var state = null;      // alias for appState[appState.mode]
var MODE = null;
var activeTab=TAB_DEFS[0].id;

function setMode(m){
  appState.mode = m;
  if(!appState[m]) appState[m] = defaultState();
  state = appState[m];
  MODE = m;
}
/* ================= student accounts (saved on this device) ================= */
var SHEET_KEY='sopaan-f11ch2';
var ACC_KEY='sopaan-students-v1';
var storageOK=true;
var MEM={};
function lsGet(k){ var r=null; try{ r=localStorage.getItem(k); }catch(e){ storageOK=false; }
  if(r===null||r===undefined) r=MEM[k]||null; try{ return r?JSON.parse(r):null; }catch(e){ return null; } }
function lsSet(k,v){ var j=JSON.stringify(v); MEM[k]=j; try{ localStorage.setItem(k,j); return true; }catch(e){ storageOK=false; return false; } }
try{ localStorage.setItem('sopaan-probe','1'); localStorage.removeItem('sopaan-probe'); }catch(e){ storageOK=false; }
function hashPin(pin,salt){ var h=2166136261, str=salt+'|'+pin; for(var i=0;i<str.length;i++){ h^=str.charCodeAt(i); h=Math.imul(h,16777619)>>>0; } return h.toString(36); }
function accKey(name,roll){ return (name.trim().toLowerCase().replace(/\s+/g,' ')+'#'+roll.trim().toLowerCase()); }
function accounts(){ return lsGet(ACC_KEY)||{students:{}}; }
var student=null; // {key,name,roll}
var records=[];   // finished-tab history for this student on this sheet
function progKey(){ return SHEET_KEY+'::'+student.key; }

function loadState(){
  appState = {mode:null, learning:null, quiz:null}; records=[]; activeTab=TAB_DEFS[0].id;
  var saved=lsGet(progKey());
  if(!saved) return;
  try{
    ['learning','quiz'].forEach(function(m){
      if(saved[m] && saved[m].tabs){
        var fresh = defaultState();
        TAB_DEFS.forEach(function(td){
          if(saved[m].tabs[td.id] && saved[m].tabs[td.id].items && saved[m].tabs[td.id].items.length===SLIDES[td.id].length){
            fresh.tabs[td.id] = saved[m].tabs[td.id];
          }
        });
        appState[m] = fresh;
      }
    });
    if(saved.mode==='learning' || saved.mode==='quiz') appState.mode = saved.mode;
    if(saved.activeTab && TAB_DEFS.some(function(t){ return t.id===saved.activeTab; })) activeTab = saved.activeTab;
    if(Array.isArray(saved.records)) records = saved.records;
  }catch(e){}
}
function saveState(){
  if(!student) return;
  lsSet(progKey(), {mode:appState.mode, learning:appState.learning, quiz:appState.quiz, activeTab:activeTab, records:records, updated:Date.now()});
  var acc=accounts(); if(acc.students[student.key]){ acc.students[student.key].last=Date.now(); lsSet(ACC_KEY,acc); }
}
function addRecord(mode, tabId, correct, revealed, skipped, total){
  records.unshift({at:Date.now(), mode:mode, tab:tabId, correct:correct, revealed:revealed, skipped:skipped, total:total});
  if(records.length>60) records.length=60;
  saveState();
}
function fmtDate(ms){ try{ return new Date(ms).toLocaleString(undefined,{day:'numeric',month:'short',hour:'2-digit',minute:'2-digit'}); }catch(e){ return ''; } }

function renderWho(){
  var el=document.getElementById('whoBar');
  if(!student){ el.hidden=true; el.innerHTML=''; return; }
  el.hidden=false;
  el.innerHTML='Signed in as <b>'+esc(student.name)+'</b> · Roll '+esc(student.roll)+
    ' <button id="btnRecord">My record</button> <button id="btnSignOut">Sign out</button>';
  document.getElementById('btnRecord').addEventListener('click', renderRecord);
  document.getElementById('btnSignOut').addEventListener('click', signOut);
}
function signOut(){
  saveState(); student=null; state=null; MODE=null;
  var acc=accounts(); delete acc.current; lsSet(ACC_KEY,acc);
  document.getElementById('modePill').hidden=true;
  renderWho(); renderLogin();
}
function signIn(key){
  var acc=accounts(); var st=acc.students[key]; if(!st) return;
  student={key:key, name:st.name, roll:st.roll};
  acc.current=key; st.last=Date.now(); lsSet(ACC_KEY,acc);
  loadState(); renderWho();
  if(appState.mode==='learning' || appState.mode==='quiz'){
    setMode(appState.mode); document.getElementById('modePill').hidden=false; updateModePill();
    showChrome(true); buildTabbar(); renderSlide();
    showToast('Welcome back, '+st.name.split(' ')[0]+'. Picking up where you left off.');
  } else {
    renderModePicker();
  }
}
function renderLogin(msg){
  showChrome(false);
  var acc=accounts(); var keys=Object.keys(acc.students).sort(function(a,b){ return (acc.students[b].last||0)-(acc.students[a].last||0); });
  var h='<div class="login-card"><h2>Student sign-in</h2>'+
    '<p class="lead">Sign in to save your answers, see your record and continue where you left off next time.</p>';
  if(!storageOK) h+='<div class="login-err">This browser is blocking saved data (for example, a private window). You can still practise, but progress will not be kept after you close the page.</div>';
  if(msg) h+='<div class="login-err">'+esc(msg)+'</div>';
  if(keys.length){
    h+='<div class="known"><span class="known-label">Continue as</span>';
    keys.slice(0,6).forEach(function(k){ var st=acc.students[k];
      h+='<button class="known-btn" data-k="'+esc(k)+'"><span>'+esc(st.name)+' <small>· Roll '+esc(st.roll)+'</small></span><small>'+(st.last?'Last active '+fmtDate(st.last):'')+'</small></button>'; });
    h+='</div>';
  }
  h+='<form id="loginForm" novalidate>'+
    '<div class="fld"><label for="lgName">Full name</label><input id="lgName" autocomplete="name" required></div>'+
    '<div class="fld-row"><div class="fld"><label for="lgRoll">Roll no.</label><input id="lgRoll" required></div>'+
    '<div class="fld"><label for="lgPin">4-digit PIN</label><input id="lgPin" type="password" inputmode="numeric" maxlength="4" autocomplete="off" required></div></div>'+
    '<button class="btn btn-primary" type="submit" style="width:100%;">Sign in</button>'+
    '<p class="login-note">New here? Enter your name, roll no. and a PIN you will remember, and your profile is created. Progress is saved on this device, so use the same device and browser to continue.</p>'+
    '</form></div>';
  var wrap=document.getElementById('wrap'); wrap.innerHTML=h;
  wrap.querySelectorAll('.known-btn').forEach(function(b){
    b.addEventListener('click', function(){
      var st=accounts().students[b.dataset.k];
      document.getElementById('lgName').value=st.name; document.getElementById('lgRoll').value=st.roll;
      document.getElementById('lgPin').focus();
    });
  });
  document.getElementById('loginForm').addEventListener('submit', function(e){
    e.preventDefault();
    var name=document.getElementById('lgName').value.trim(), roll=document.getElementById('lgRoll').value.trim(), pin=document.getElementById('lgPin').value.trim();
    if(!name||!roll){ renderLoginErr('Enter your name and roll no.'); return; }
    if(!/^\d{4}$/.test(pin)){ renderLoginErr('Your PIN must be exactly 4 digits.'); return; }
    var k=accKey(name,roll); var acc=accounts();
    if(acc.students[k]){
      if(acc.students[k].pin!==hashPin(pin,k)){ renderLoginErr('That PIN does not match this name and roll no. Try again.'); return; }
    } else {
      acc.students[k]={name:name.replace(/\s+/g,' '), roll:roll, pin:hashPin(pin,k), created:Date.now()};
      lsSet(ACC_KEY,acc);
    }
    signIn(k);
  });
}
function renderLoginErr(m){
  var n=document.getElementById('lgName').value, r=document.getElementById('lgRoll').value;
  renderLogin(m); document.getElementById('lgName').value=n; document.getElementById('lgRoll').value=r; document.getElementById('lgPin').focus();
}
function tabSummary(m){
  var st=appState[m]; if(!st) return null;
  return TAB_DEFS.map(function(td){
    var items=st.tabs[td.id].items, n=items.length;
    var c=items.filter(function(i){return i.status==='correct';}).length;
    var done=items.filter(function(i){return i.status!=='unanswered';}).length;
    return {label:td.label, n:n, done:done, correct:c};
  });
}
function renderRecord(){
  showChrome(false);
  var tabLabel=function(id){ var t=TAB_DEFS.find(function(x){return x.id===id;}); return t?t.label:id; };
  var h='<div class="rec-card"><h2>'+esc(student.name)+'’s record</h2><p class="rec-empty" style="margin:0 0 12px;">Roll '+esc(student.roll)+' · Equivalent Algebraic Expressions</p>';
  ['learning','quiz'].forEach(function(m){
    var sum=tabSummary(m);
    h+='<h3>'+(m==='learning'?'📘 Learning Sheet':'📝 Quiz Mode')+'</h3>';
    if(!sum){ h+='<p class="rec-empty">Not started yet.</p>'; return; }
    h+='<div class="rec-table-wrap"><table class="rec-table"><thead><tr><th>Section</th><th>Progress</th><th>Correct first time</th></tr></thead><tbody>';
    sum.forEach(function(r){ var pct=Math.round(r.done/r.n*100);
      h+='<tr><td>'+r.label+'</td><td><span class="rec-bar"><i style="width:'+pct+'%"></i></span>'+r.done+' / '+r.n+'</td><td>'+(m==='quiz'?'—':r.correct+' / '+r.n)+'</td></tr>'; });
    h+='</tbody></table></div>';
  });
  h+='</div><div class="rec-card"><h3>Finished sections</h3>';
  if(!records.length){ h+='<p class="rec-empty">No sections finished yet. Each time you finish a tab, your score is recorded here.</p>'; }
  else {
    h+='<div class="rec-table-wrap"><table class="rec-table"><thead><tr><th>When</th><th>Mode</th><th>Section</th><th>Score</th></tr></thead><tbody>';
    records.forEach(function(r){ h+='<tr><td>'+fmtDate(r.at)+'</td><td>'+(r.mode==='quiz'?'Quiz':'Learning')+'</td><td>'+tabLabel(r.tab)+'</td><td>'+r.correct+' / '+r.total+(r.mode==='learning'?' <span class="rec-empty">('+r.revealed+' revealed, '+r.skipped+' skipped)</span>':'')+'</td></tr>'; });
    h+='</tbody></table></div>';
  }
  h+='</div><button class="btn btn-primary" id="btnBack">'+(MODE?'Back to practice':'Choose a mode')+'</button>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('btnBack').addEventListener('click', function(){
    if(MODE){ showChrome(true); buildTabbar(); renderSlide(); } else renderModePicker();
  });
  window.scrollTo({top:0});
}

/* ================= tab bar ================= */
function buildTabbar(){
  var el=document.getElementById('tabbar');
  el.innerHTML = '<button class="tab-btn'+(activeTab==='theory'?' active':'')+'" data-tab="theory">Theory<span class="tab-count">notes</span></button>' + TAB_DEFS.map(function(t){
    return '<button class="tab-btn'+(t.id===activeTab?' active':'')+'" data-tab="'+t.id+'">'+t.label+'<span class="tab-count">'+SLIDES[t.id].length+'</span></button>';
  }).join('') + '<button class="tab-btn'+(activeTab==='report'?' active':'')+'" data-tab="report">📊 Report<span class="tab-count">pie</span></button>';
  el.querySelectorAll('.tab-btn').forEach(function(btn){
    btn.addEventListener('click', function(){ activeTab=btn.dataset.tab; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); });
  });
}

/* ================= rendering ================= */
function canProceed(item){ return item.status==='correct'||item.status==='revealed'||item.status==='skipped'; }

function renderSlide(){
  if(!state.tabs[activeTab]){ activeTab=TAB_DEFS[0].id; }
  var ts = state.tabs[activeTab];
  var slides = SLIDES[activeTab];
  if(ts.idx>=slides.length||ts.idx<0) ts.idx=0;
  var idx = ts.idx;
  var slide = slides[idx];
  var item = ts.items[idx];

  var tdef=TAB_DEFS.find(function(t){return t.id===activeTab;});
  document.getElementById('spLabel').textContent = tdef.label+' · Question '+(idx+1)+' of '+slides.length;
  document.getElementById('secSub').textContent = tdef.label+' — '+tdef.sub;
  document.getElementById('spFill').style.width = Math.round(((idx)/(Math.max(slides.length-1,1)))*100)+'%';

  var h='<div class="qcard">';
  if(slide.kind==='mcq' || slide.kind==='ar'){
    h += renderChoiceBody(slide, item, idx);
  } else {
    h += renderBlankBody(slide, item, idx);
  }
  h += '<div class="feedback" id="feedbackBox"></div>';
  if(MODE==='learning' && (item.status==='correct'||item.status==='revealed')) h += solutionHTML(slide);
  h += '</div>';

  document.getElementById('wrap').innerHTML = h;
  wireSlideEvents(slide, item, idx);
  restoreFeedback(item);
  renderNavbar(item);
  updateFab();
  saveState();
}

function solutionHTML(slide){
  if(!slide.sol) return '';
  return '<div class="solution"><div class="sol-h">Solution</div>'+slide.sol.split('\n').map(function(l){ return '<div class="sol-line">'+fr(esc(l))+'</div>'; }).join('')+'</div>';
}
var LETTERS=['a','b','c','d','e','f'];
function chosenHTML(slide,item){
  var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
  if(item.choice===undefined) return '';
  var ok=item.choice===slide.correct;
  var h='<div class="chosen '+(ok?'ok':'bad')+'"><b>Your answer:</b> ('+LETTERS[item.choice]+') '+fr(esc(opts[item.choice]))+(ok?' ✓':' ✗')+'</div>';
  if(!ok) h+='<div class="chosen ok"><b>Correct answer:</b> ('+LETTERS[slide.correct]+') '+fr(esc(opts[slide.correct]))+'</div>';
  return h;
}
function renderChoiceBody(slide, item, idx){
  var h='<div class="qhead"><div class="qnum">'+(idx+1)+'</div>';
  if(slide.kind==='mcq'){
    h += '<div class="qtext">'+fr(esc(slide.text))+(slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  } else {
    h += '<div class="qtext"><span class="qtag" style="margin-left:0;margin-right:6px;">A / R</span>Assertion (A): '+fr(esc(slide.a))+'<br>Reason (R): '+fr(esc(slide.r))+(slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  }
  h += '</div>';
  if(slide.fig) h += '<div class="fig">'+slide.fig+'</div>';
  var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
  if(MODE==='quiz') h += '<div class="quiz-hint">Quiz mode — pick an option. The correct answer is revealed once you finish this tab.</div>';
  var locked = MODE==='learning' && (item.status==='correct' || item.status==='revealed');
  h += '<div class="options">';
  opts.forEach(function(opt,i){
    var cls='opt';
    if(locked){
      if(i===slide.correct) cls+=' is-correct';
      else if(item.choice===i) cls+=' is-wrong';
      cls+=' locked';
    }
    if(item.choice===i) cls+=' is-chosen';
    h += '<label class="'+cls+'"><input type="radio" name="choice" value="'+i+'" '+(item.choice===i?'checked':'')+' '+(locked?'disabled':'')+'> <span class="opt-l">('+LETTERS[i]+')</span> <span class="opt-t">'+fr(esc(opt))+'</span>'+(item.choice===i?'<span class="opt-tag">'+(locked?(i===slide.correct?'Your answer ✓':'Your answer ✗'):'Selected')+'</span>':'')+'</label>';
  });
  h += '</div>';
  if(locked) h += chosenHTML(slide,item);
  return h;
}

function renderBlankBody(slide, item, idx){
  var h='<div class="qhead"><div class="qnum">'+(idx+1)+'</div><div class="qtext">';
  if(slide.kind==='case'){ h += '<b>'+esc(slide.title)+'.</b> '+esc(slide.body); }
  else { var pp=fr(esc(slide.p)).split('\n'); h += pp[0]+pp.slice(1).map(function(x){return '<span class="datline">'+x+'</span>';}).join(''); }
  h += (slide.tag?'<span class="qtag">'+esc(slide.tag)+'</span>':'')+'</div>';
  if(slide.marks) h += '<div class="marks-pill">'+slide.marks+'</div>';
  h += '</div>';
  if(slide.fig) h += '<div class="fig">'+slide.fig+'</div>';

  var total = slide.flat.length;
  var hasExpr = slide.flat.some(function(s){ return s.expr===true; });
  var hasFrac = slide.flat.some(function(s){ return ['fv','fe','fl','fm','fi','flist'].indexOf(s.expr)>=0; });
  var blankCount=0; slide.flat.forEach(function(s){ blankCount+=Object.keys(s.a).length; });

  if(MODE==='quiz'){
    h += '<div class="step-badge">'+blankCount+' blank'+(blankCount===1?'':'s')+' in this question</div>';
    h += '<div class="quiz-hint">Quiz mode — fill in what you can. Correct answers are revealed once you finish this tab.</div>';
    if(hasFrac) h += '<div class="quiz-hint">Type fractions like <b>3/4</b> and mixed numbers like <b>2 3/4</b> (whole number, space, fraction).</div>';
    if(hasExpr) h += '<div class="quiz-hint">Type answers like <b>2x-5</b>, <b>x^2-4</b> or <b>3+2i</b>. Use ^ for powers, | | for absolute value and pi for π. Any equivalent form is accepted.</div>';
    h += '<div class="steps">';
    for(var qi=0; qi<total; qi++){
      var qstep = slide.flat[qi];
      var qss = item.stepStates[qi];
      if(qstep.partLabel) h += '<div class="subpart-label">'+esc(qstep.partLabel)+'</div>';
      if(qstep.orDivider) h += '<div class="or-divider">OR</div>';
      var qline = fr(qstep.t);
      Object.keys(qstep.a).forEach(function(bkey){
        var val = qss.inputs[bkey]||'';
        var inp='<input class="blank-input'+(['fv','fe','fl','fm','fi','dec'].indexOf(qstep.expr)>=0?' fr':(qstep.expr==='flist'||qstep.expr==='dlist'||qstep.expr==='glist')?' wide':qstep.expr===true?' expr':(qstep.expr==='words'||qstep.expr==='list'||qstep.expr==='expanded'||qstep.expr==='set'||qstep.expr==='primes'||qstep.expr==='trans'||qstep.expr==='rot'?' wide':''))+'" data-step="'+qi+'" data-bkey="'+bkey+'" value="'+esc(val)+'">';
        qline = qline.replace('__'+bkey+'__', inp);
      });
      if(qstep.fig) h += '<div class="fig">'+qstep.fig+'</div>';
      h += '<div class="step-line">'+qline+'</div>';
    }
    h += '</div>';
    return h;
  }

  if(hasFrac) h += '<div class="quiz-hint">Type fractions like <b>3/4</b> and mixed numbers like <b>2 3/4</b> (whole number, space, fraction).</div>';
  if(hasExpr) h += '<div class="quiz-hint">Type answers like <b>2x-5</b>, <b>x^2-4</b> or <b>3+2i</b>. Use ^ for powers, | | for absolute value and pi for π. Any equivalent form is accepted.</div>';
  var locked = item.status==='correct' || item.status==='revealed';
  var upto = locked ? total-1 : item.curStep;
  h += '<div class="step-badge">Step '+(Math.min(item.curStep,total-1)+1)+' of '+total+'</div>';
  h += '<div class="steps">';
  for(var i=0;i<=upto;i++){
    var step = slide.flat[i];
    var ss = item.stepStates[i];
    if(step.partLabel) h += '<div class="subpart-label">'+esc(step.partLabel)+'</div>';
    if(step.orDivider) h += '<div class="or-divider">OR</div>';
    var resolved = ss.status==='correct' || ss.status==='revealed';
    var line = fr(step.t);
    Object.keys(step.a).forEach(function(bkey){
      var fs = ss.inputs['fs_'+bkey];
      var cls = fs==='correct'?'is-correct':(fs==='wrong'?'is-wrong':'');
      var val = ss.inputs[bkey]||'';
      var dis = resolved ? 'disabled':'';
      var inp='<input class="blank-input '+cls+(['fv','fe','fl','fm','fi','dec'].indexOf(step.expr)>=0?' fr':(step.expr==='flist'||step.expr==='dlist'||step.expr==='glist')?' wide':step.expr===true?' expr':(step.expr==='words'||step.expr==='list'||step.expr==='expanded'||step.expr==='set'||step.expr==='primes'||step.expr==='trans'||step.expr==='rot'?' wide':''))+'" data-step="'+i+'" data-bkey="'+bkey+'" value="'+esc(val)+'" '+dis+'>';
      line = line.replace('__'+bkey+'__', inp);
    });
    if(step.fig) h += '<div class="fig">'+step.fig+'</div>';
    h += '<div class="step-line'+(resolved?' resolved':'')+'">'+line+'</div>';
    if(ss.status==='revealed'){
      var reveals=[];
      Object.keys(step.a).forEach(function(bkey){ reveals.push(bkey+' = '+esc(step.a[bkey])); });
      h += '<div class="reveal-note">correct: '+reveals.join(', ')+'</div>';
    }
  }
  h += '</div>';
  return h;
}

var __flash=null;
function restoreFeedback(item){
  var fb=document.getElementById('feedbackBox'); if(!fb) return;
  if(__flash){ fb.className='feedback show '+__flash.c; fb.innerHTML=__flash.h; __flash=null; return; }
  if(MODE==='quiz'){ fb.className='feedback'; fb.innerHTML=''; return; }
  if(item.status==='correct'){ fb.className='feedback show ok'; fb.innerHTML='<b>All done — correct!</b>'; }
  else if(item.status==='revealed'){ fb.className='feedback show reveal'; fb.innerHTML='<b>Answer revealed above.</b> Move on whenever you’re ready.'; }
  else if(item.status==='skipped'){ fb.className='feedback show retry'; fb.innerHTML='Skipped — you can answer it now and press <b>Check</b>, or come back later from the Question Palette.'; }
  else { fb.className='feedback'; fb.innerHTML=''; }
}

function slideIsAnswered(slide,item){
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice!==undefined;
  return item.stepStates.some(function(ss){ return Object.keys(ss.inputs).some(function(k){ return k.indexOf('fs_')!==0 && ss.inputs[k] && String(ss.inputs[k]).trim()!==''; }); });
}
function renderNavbar(item){
  var ts = state.tabs[activeTab];
  var slides = SLIDES[activeTab];
  var slide = slides[ts.idx];
  var isLast = ts.idx === slides.length-1;
  var h='';
  h += '<button class="btn" id="btnPrev" '+(ts.idx===0?'disabled':'')+'>&larr; Previous</button>';

  if(MODE==='quiz'){
    h += '<button class="btn" id="btnSkip">Skip</button>';
    h += '<span class="spacer"></span>';
    h += '<button class="btn btn-primary" id="btnNext">'+(isLast?'Finish':'Next →')+'</button>';
  } else {
    h += '<button class="btn" id="btnSkip" '+(item.status!=='unanswered'?'disabled':'')+'>Skip</button>';
    h += '<span class="spacer"></span>';
    h += '<button class="btn btn-primary" id="btnCheck" '+((item.status!=='unanswered'&&item.status!=='skipped')?'disabled':'')+'>Check</button>';
    h += '<button class="btn btn-primary" id="btnNext" '+(canProceed(item)?'':'disabled')+'>'+(isLast?'Finish':'Next →')+'</button>';
  }
  document.getElementById('navbarInner').innerHTML = h;

  document.getElementById('btnPrev').addEventListener('click', function(){ if(ts.idx>0){ ts.idx--; renderSlide(); } });

  if(MODE==='quiz'){
    document.getElementById('btnSkip').addEventListener('click', function(){
      item.status='skipped';
      advanceQuiz(ts, slides);
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      item.status = slideIsAnswered(slide,item) ? 'answered' : 'unanswered';
      advanceQuiz(ts, slides);
    });
  } else {
    document.getElementById('btnSkip').addEventListener('click', function(){
      if(item.status==='unanswered'){ item.status='skipped'; renderSlide(); }
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      if(!canProceed(item)) return;
      if(ts.idx < slides.length-1){ ts.idx++; ts.maxReached=Math.max(ts.maxReached, ts.idx); renderSlide(); }
      else { renderFinished(); }
    });
    document.getElementById('btnCheck').addEventListener('click', function(){ handleCheck(); });
  }
}
function advanceQuiz(ts, slides){
  if(ts.idx < slides.length-1){ ts.idx++; ts.maxReached=Math.max(ts.maxReached, ts.idx); renderSlide(); }
  else { renderFinished(); }
}

function wireSlideEvents(slide, item, idx){
  document.querySelectorAll('input[type="radio"][name="choice"]').forEach(function(r){
    r.addEventListener('change', function(){ item.choice=parseInt(r.value,10); saveState();
      document.querySelectorAll('.opt').forEach(function(l){ l.classList.remove('is-chosen'); var t=l.querySelector('.opt-tag'); if(t) t.remove(); });
      var lab=r.closest('.opt'); lab.classList.add('is-chosen'); var tg=document.createElement('span'); tg.className='opt-tag'; tg.textContent='Selected'; lab.appendChild(tg); });
  });
  document.querySelectorAll('.blank-input').forEach(function(inp){
    inp.addEventListener('input', function(){
      var si=parseInt(inp.dataset.step,10), bk=inp.dataset.bkey;
      item.stepStates[si].inputs[bk]=inp.value;
      saveState();
    });
  });
}

function handleCheck(){
  var ts = state.tabs[activeTab];
  var slide = SLIDES[activeTab][ts.idx];
  var item = ts.items[ts.idx];
  if(item.status==='skipped') item.status='unanswered';
  var fb = document.getElementById('feedbackBox');

  if(slide.kind==='mcq' || slide.kind==='ar'){
    if(item.choice===undefined){ fb.className='feedback show err'; fb.innerHTML='Please choose an option first.'; return; }
    var ok = item.choice===slide.correct;
    if(ok){
      item.status='correct'; playSuccess();
      fb.className='feedback show ok'; fb.innerHTML='<b>Correct!</b>';
    } else {
      item.attempts=(item.attempts||0)+1;
      if(item.attempts>=2){ item.status='revealed'; playReveal(); }
      else { playWrong(); fb.className='feedback show retry'; fb.innerHTML='<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'; __flash={c:'retry',h:'<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'}; }
    }
    renderSlide();
    return;
  }

  // blank / case
  var step = slide.flat[item.curStep];
  var ss = item.stepStates[item.curStep];
  var blanks = Object.keys(step.a);
  var missing = blanks.some(function(k){ return !ss.inputs[k] || String(ss.inputs[k]).trim()===''; });
  if(missing){ fb.className='feedback show err'; fb.innerHTML='Fill in every blank in this step before checking.'; return; }

  var allGood=true;
  blanks.forEach(function(k){
    var good=answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr);
    ss.inputs['fs_'+k]=good?'correct':'wrong';
    if(!good) allGood=false;
  });

  if(allGood){
    ss.status='correct'; playSuccess();
    advanceStepOrFinish(item, slide);
  } else {
    ss.attempts=(ss.attempts||0)+1;
    if(ss.attempts>=2){
      ss.status='revealed'; playReveal();
      advanceStepOrFinish(item, slide);
    } else {
      playWrong();
      fb.className='feedback show retry';
      fb.innerHTML='<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'; __flash={c:'retry',h:'<b>Not quite — try again</b> (attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'};
      renderSlide();
      return;
    }
  }
  renderSlide();
}

function advanceStepOrFinish(item, slide){
  var total = slide.flat.length;
  var hasExpr = slide.flat.some(function(s){ return s.expr===true; });
  var hasFrac = slide.flat.some(function(s){ return ['fv','fe','fl','fm','fi','flist'].indexOf(s.expr)>=0; });
  if(item.curStep < total-1){
    item.curStep++;
  } else {
    var anyRevealed = item.stepStates.some(function(ss){ return ss.status==='revealed'; });
    item.status = anyRevealed ? 'revealed' : 'correct';
  }
}

/* ================= palette ================= */
var overlay=document.getElementById('overlay');
function statusOf(tabId,i){
  var ts=state.tabs[tabId];
  if(i>ts.maxReached) return 'locked';
  if(i===ts.idx) return 'current';
  return ts.items[i].status==='unanswered' ? 'locked' : ts.items[i].status;
}
function buildPalette(){
  var slides=SLIDES[activeTab];
  document.getElementById('paletteTitle').textContent = TAB_DEFS.find(function(t){return t.id===activeTab;}).label+' · Question palette';
  var body=document.getElementById('paletteBody');
  var html='';
  for(var i=0;i<slides.length;i++){
    html += '<div class="chip" data-status="'+statusOf(activeTab,i)+'" data-idx="'+i+'">'+(i+1)+'</div>';
  }
  body.innerHTML = html;
  body.querySelectorAll('.chip').forEach(function(chip){
    chip.addEventListener('click', function(){
      var i=parseInt(chip.dataset.idx,10);
      var ts=state.tabs[activeTab];
      if(i>ts.maxReached){ showToast('Finish the earlier questions to unlock this one.'); return; }
      ts.idx=i; closePalette(); renderSlide();
    });
  });
}
function openPalette(){ buildPalette(); overlay.classList.add('show'); }
function closePalette(){ overlay.classList.remove('show'); }
var toastTimer;
function showToast(msg){
  var t=document.getElementById('toast'); t.textContent=msg; t.classList.add('show');
  clearTimeout(toastTimer); toastTimer=setTimeout(function(){ t.classList.remove('show'); },2200);
}
document.getElementById('paletteFab').addEventListener('click', openPalette);
document.getElementById('paletteClose').addEventListener('click', closePalette);
overlay.addEventListener('click', function(e){ if(e.target===overlay) closePalette(); });

function updateFab(){
  var slides=SLIDES[activeTab];
  var done=state.tabs[activeTab].items.filter(function(it){ return it.status==='correct'||it.status==='revealed'||it.status==='skipped'; }).length;
  document.getElementById('fabBadge').textContent = done+'/'+slides.length;
}

/* ================= overall progress + finish ================= */
function updateChapterProgress(){
  var total=0, done=0;
  TAB_DEFS.forEach(function(td){
    state.tabs[td.id].items.forEach(function(it){
      total++;
      if(it.status==='correct'||it.status==='revealed'||it.status==='skipped') done++;
    });
  });
  var pct = total>0 ? Math.round((done/total)*100) : 0;
  document.getElementById('cpFill').style.width=pct+'%';
  document.getElementById('cpLabel').textContent=pct+'% complete';
}
function isSlideCorrect(tabId,i){
  var slide=SLIDES[tabId][i], item=state.tabs[tabId].items[i];
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice===slide.correct;
  return slide.flat.every(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).every(function(k){ return answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr); });
  });
}
function isSlideAttempted(tabId,i){
  var slide=SLIDES[tabId][i], item=state.tabs[tabId].items[i];
  if(slide.kind==='mcq'||slide.kind==='ar') return item.choice!==undefined;
  return slide.flat.some(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).some(function(k){ return ss.inputs[k] && String(ss.inputs[k]).trim()!==''; });
  });
}
function slideLabel(slide){
  var t = slide.kind==='case' ? slide.title : (slide.kind==='ar' ? slide.a : (slide.p||slide.text||''));
  t = String(t);
  return t.length>90 ? t.slice(0,90)+'…' : t;
}
function slideAnswerText(slide, item, correctSide){
  if(slide.kind==='mcq'||slide.kind==='ar'){
    var opts = slide.kind==='mcq' ? slide.opts : AR_OPTIONS;
    if(correctSide) return '('+LETTERS[slide.correct]+') '+opts[slide.correct];
    return item.choice!==undefined ? '('+LETTERS[item.choice]+') '+opts[item.choice] : '— not attempted —';
  }
  return slide.flat.map(function(step,si){
    var ss=item.stepStates[si];
    return Object.keys(step.a).map(function(k){
      return correctSide ? step.a[k] : (ss.inputs[k] || '—');
    }).join(', ');
  }).join('  |  ');
}

function renderFinished(){
  if(MODE==='quiz'){ renderQuizResults(); return; }
  var ts=state.tabs[activeTab];
  var correct=ts.items.filter(function(i){return i.status==='correct';}).length;
  var revealed=ts.items.filter(function(i){return i.status==='revealed';}).length;
  var skipped=ts.items.filter(function(i){return i.status==='skipped';}).length;
  var h='<div class="qcard done-card"><div class="big">✨</div><h2>Tab complete</h2>';
  h+='<p style="color:var(--ink-soft);font-size:14px;">You worked through all '+ts.items.length+' questions in this tab.</p>';
  if(!ts.recorded){ ts.recorded=true; addRecord('learning', activeTab, correct, revealed, skipped, ts.items.length); }
  h+='<div class="score-pills">'+
     '<span class="score-pill" style="background:var(--success-soft);color:var(--success);">'+correct+' correct</span>'+
     '<span class="score-pill" style="background:var(--danger-soft);color:var(--danger);">'+revealed+' revealed</span>'+
     '<span class="score-pill" style="background:var(--gold-soft);color:var(--retry-text);">'+skipped+' skipped</span></div>'+
     '<button class="btn btn-primary" id="btnReview">Review from question 1</button></div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  document.getElementById('btnReview').addEventListener('click', function(){ ts.idx=0; ts.recorded=false; renderSlide(); });
  updateChapterProgress(); saveState();
}

function renderQuizResults(){
  var ts=state.tabs[activeTab];
  var slides=SLIDES[activeTab];
  var correctCount=0, attemptedCount=0;
  var rowsHtml = slides.map(function(slide,i){
    var item=ts.items[i];
    var ok=isSlideCorrect(activeTab,i);
    var att=isSlideAttempted(activeTab,i);
    if(ok) correctCount++;
    if(att) attemptedCount++;
    var tagCls = ok?'ok':(att?'bad':'na');
    var tagText = ok?'Correct':(att?'Incorrect':'Not attempted');
    var row='<div class="review-row">';
    row+='<span class="review-tag '+tagCls+'">Q'+(i+1)+' · '+tagText+'</span>';
    row+='<div class="review-q">'+fr(esc(slideLabel(slide)))+'</div>';
    row+='<div class="review-ans"><b>Your answer:</b> '+fr(esc(slideAnswerText(slide,item,false)))+'</div>';
    if(!ok) row+='<div class="review-ans" style="color:var(--success);"><b>Correct answer:</b> '+fr(esc(slideAnswerText(slide,item,true)))+'</div>';
    if(slide.sol) row+='<details class="rev-sol"><summary>Show solution</summary>'+solutionHTML(slide)+'</details>';
    row+='</div>';
    return row;
  }).join('');

  addRecord('quiz', activeTab, correctCount, 0, 0, slides.length);
  var h='<div class="qcard done-card" style="text-align:left;">';
  h+='<div style="text-align:center;"><div class="big">🏁</div><h2>Quiz complete</h2>';
  h+='<p style="color:var(--ink-soft);font-size:14px;">'+correctCount+' / '+slides.length+' correct · '+attemptedCount+' attempted</p></div>';
  h+='<div style="margin-top:16px;">'+rowsHtml+'</div>';
  h+='<div style="text-align:center;margin-top:6px;"><button class="btn btn-primary" id="btnReview">Review from question 1</button></div>';
  h+='</div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  document.getElementById('btnReview').addEventListener('click', function(){ ts.idx=0; renderSlide(); });
  playSuccess();
  updateChapterProgress(); saveState();
}

/* ================= mode picker ================= */
function updateModePill(){
  var btn=document.getElementById('modePill');
  if(!btn) return;
  btn.textContent = MODE==='quiz' ? '📝 Quiz Mode · switch' : '📘 Learning Sheet · switch';
}
function showChrome(show){
  document.querySelector('.tabbar').style.display = show?'':'none';
  document.querySelector('.slide-progress').style.display = show?'':'none';
  document.querySelector('.navbar').style.display = show?'':'none';
  document.getElementById('paletteFab').style.display = show?'':'none';
}
function renderModePicker(){
  showChrome(false);
  var wrap=document.getElementById('wrap');
  wrap.innerHTML =
    '<div class="mode-pick">'+
      '<div class="mode-card" data-pick="learning"><div class="mode-icon">📘</div><h3>Learning Sheet</h3>'+
      '<p>Work through each question step by step with instant feedback — two tries, then the correct value is revealed right there so you can keep moving.</p></div>'+
      '<div class="mode-card" data-pick="quiz"><div class="mode-icon">📝</div><h3>Quiz Mode</h3>'+
      '<p>Attempt every question with no hints along the way. Your score and the full answer key are shown together once you finish the tab — just like the real exam.</p></div>'+
    '</div>';
  wrap.querySelectorAll('[data-pick]').forEach(function(card){
    card.addEventListener('click', function(){
      setMode(card.dataset.pick); activeTab='theory';
      document.getElementById('modePill').hidden=false;
      updateModePill();
      showChrome(true);
      buildTabbar();
      renderSlide();
    });
  });
}
document.getElementById('modePill').addEventListener('click', function(){
  if(!appState.mode){ return; }
  setMode(appState.mode==='quiz' ? 'learning' : 'quiz');
  updateModePill();
  showChrome(true);
  buildTabbar();
  renderSlide();
});

/* ================= boot ================= */
var _origRenderSlide = renderSlide;
renderSlide = function(){ _origRenderSlide(); updateChapterProgress(); updateModePill(); };


/* ================= theory tab ================= */
function renderTheory(){
  var wrap=document.getElementById('wrap');
  wrap.innerHTML='<div class="theory">'+fr(THEORY)+'</div>';
  document.querySelector('.slide-progress').style.display='none';
  document.querySelector('.navbar').style.display='none';
  document.getElementById('paletteFab').style.display='none';
  document.getElementById('secSub').textContent='Theory — notes, key ideas and worked examples';
  wrap.querySelectorAll('[data-go]').forEach(function(b){ b.addEventListener('click',function(){ activeTab=b.dataset.go; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); });
  wrap.querySelectorAll('[data-jump]').forEach(function(b){ b.addEventListener('click',function(){ var t=document.getElementById(b.dataset.jump); if(t) t.scrollIntoView({behavior:'smooth',block:'start'}); }); });
}
var _rsTheory = renderSlide;
renderSlide = function(){
  if(activeTab==='theory'){ renderTheory(); buildTabbar(); updateChapterProgress(); updateModePill(); saveState(); return; }
  document.querySelector('.slide-progress').style.display='';
  document.querySelector('.navbar').style.display='';
  document.getElementById('paletteFab').style.display='';
  _rsTheory();
};


/* ================= MYP criterion report ================= */
var CRIT_COL={A:'var(--accent-text)',B:'var(--gold)',C:'#8A6FC4',D:'#2F9AA0'};
function critStats(){
  return REPORT.map(function(r){
    var tabId=r[0], slides=SLIDES[tabId], ts=state&&state.tabs[tabId];
    var c=0,w=0,n=0;
    slides.forEach(function(sl,i){
      if(!ts||!ts.items[i]){ n++; return; }
      var it=ts.items[i];
      if(MODE==='learning'){
        if(it.status==='correct') c++; else if(it.status==='revealed') w++; else n++;
      } else {
        if(isSlideCorrect(tabId,i)) c++; else if(isSlideAttempted(tabId,i)) w++; else n++;
      }
    });
    var tot=slides.length, pct=tot?Math.round(c/tot*100):0;
    var lvl=Math.round(c/Math.max(tot,1)*8);
    return {tab:tabId,letter:r[1],name:r[2],c:c,w:w,n:n,tot:tot,pct:pct,lvl:lvl};
  });
}
function arcPath(cx,cy,r,a0,a1){
  if(a1-a0>=Math.PI*2-1e-6){ return 'M'+(cx-r)+','+cy+' a'+r+','+r+' 0 1,0 '+(2*r)+',0 a'+r+','+r+' 0 1,0 '+(-2*r)+',0 Z'; }
  var x0=cx+r*Math.sin(a0), y0=cy-r*Math.cos(a0), x1=cx+r*Math.sin(a1), y1=cy-r*Math.cos(a1);
  return 'M'+cx+','+cy+' L'+x0.toFixed(2)+','+y0.toFixed(2)+' A'+r+','+r+' 0 '+((a1-a0)>Math.PI?1:0)+',1 '+x1.toFixed(2)+','+y1.toFixed(2)+' Z';
}
function pieSVG(parts,size,hole,center,sub){
  var tot=parts.reduce(function(s,p){return s+p.v;},0), cx=size/2, cy=size/2, r=size/2-4, a=0, h='';
  if(!tot){ h+='<circle cx="'+cx+'" cy="'+cy+'" r="'+r+'" style="fill:var(--paper-2);stroke:var(--rule)"/>'; }
  parts.forEach(function(p){ if(!p.v) return; var b=a+p.v/tot*Math.PI*2; h+='<path d="'+arcPath(cx,cy,r,a,b)+'" style="fill:'+p.col+';stroke:var(--card);stroke-width:2"><title>'+esc(p.label)+': '+p.v+'</title></path>'; a=b; });
  if(hole) h+='<circle cx="'+cx+'" cy="'+cy+'" r="'+(r*hole)+'" style="fill:var(--card)"/>';
  if(center) h+='<text x="'+cx+'" y="'+(cy-(sub?4:0))+'" text-anchor="middle" dominant-baseline="middle" style="fill:var(--ink);font:700 '+(size>150?22:15)+'px Fraunces,serif">'+center+'</text>';
  if(sub) h+='<text x="'+cx+'" y="'+(cy+16)+'" text-anchor="middle" style="fill:var(--ink-soft);font:600 11px \'Source Sans 3\',sans-serif">'+sub+'</text>';
  return '<svg viewBox="0 0 '+size+' '+size+'" width="'+size+'" height="'+size+'" role="img">'+h+'</svg>';
}
function band(l){ return l===0?'0':(l<=2?'1–2':(l<=4?'3–4':(l<=6?'5–6':'7–8'))); }
function renderReport(){
  var st=critStats(), totC=0, totQ=0;
  st.forEach(function(s){ totC+=s.c; totQ+=s.tot; });
  var h='<div class="theory">';
  h+='<section class="note"><h2>Chapter test report</h2><p class="lt">'+(MODE==='quiz'?'<b>Quiz mode</b> results: answers are marked when you finish each test tab.':'<b>Learning mode</b> results: a question counts as correct only if you got it without the answer being revealed. Switch to Quiz mode for an exam-style score.')+'</p>';
  h+='<div class="rep-top"><div class="rep-pie">'+pieSVG(st.map(function(s){return {v:s.c,col:CRIT_COL[s.letter],label:'Criterion '+s.letter};}),200,0.55,totC+'/'+totQ,'correct')+'</div>';
  h+='<div class="rep-legend"><div class="rep-cap">Marks earned, by criterion</div>'+st.map(function(s){ return '<div class="rep-li"><span class="sw" style="background:'+CRIT_COL[s.letter]+'"></span><b>'+s.letter+'</b>&nbsp;'+esc(s.name)+'<span class="rep-n">'+s.c+' / '+s.tot+'</span></div>'; }).join('')+'</div></div></section>';
  h+='<div class="rep-grid">'+st.map(function(s){
    return '<div class="rep-card"><div class="rep-h"><span class="crit" style="background:'+CRIT_COL[s.letter]+'">'+s.letter+'</span>'+esc(s.name)+'</div>'+
      '<div class="rep-row">'+pieSVG([{v:s.c,col:'var(--success)',label:'Correct'},{v:s.w,col:'var(--danger)',label:'Incorrect'},{v:s.n,col:'var(--locked)',label:'Not attempted'}],120,0.5,s.pct+'%')+
      '<div class="rep-stats"><div><span class="sw" style="background:var(--success)"></span>Correct <b>'+s.c+'</b></div><div><span class="sw" style="background:var(--danger)"></span>Incorrect <b>'+s.w+'</b></div><div><span class="sw" style="background:var(--locked)"></span>Not attempted <b>'+s.n+'</b></div>'+
      '<div class="rep-lvl">Indicative level <b>'+s.lvl+'</b> / 8 <span>(band '+band(s.lvl)+')</span></div></div></div>'+
      '<button class="hub-btn" data-go="'+s.tab+'">Open Test '+s.letter+' →</button></div>';
  }).join('')+'</div>';
  h+='<p class="rep-note">Indicative level = fraction of questions correct × 8, rounded. It is a practice guide only; your teacher awards the real MYP criterion levels.</p></div>';
  var wrap=document.getElementById('wrap'); wrap.innerHTML=h;
  document.querySelector('.slide-progress').style.display='none';
  document.querySelector('.navbar').style.display='none';
  document.getElementById('paletteFab').style.display='none';
  document.getElementById('secSub').textContent='Report — chapter test results by MYP criterion';
  wrap.querySelectorAll('[data-go]').forEach(function(b){ b.addEventListener('click',function(){ activeTab=b.dataset.go; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); });
}
var _rsReport = renderSlide;
renderSlide = function(){
  if(activeTab==='report'){ renderReport(); buildTabbar(); updateChapterProgress(); updateModePill(); saveState(); return; }
  _rsReport();
};


/* ================= skipped-question return ================= */
function firstSkippedIdx(ts){
  for(var i=0;i<ts.items.length;i++){
    var it=ts.items[i];
    if(MODE==='quiz'){ if(!isSlideAttempted(activeTab,i)) return i; }
    else if(it.status==='skipped'||it.status==='unanswered') return i;
  }
  return -1;
}
function skippedList(ts){
  var out=[]; for(var i=0;i<ts.items.length;i++){ var it=ts.items[i];
    if(MODE==='quiz' ? !isSlideAttempted(activeTab,i) : (it.status==='skipped'||it.status==='unanswered')) out.push(i); }
  return out;
}
function renderSkipGate(ts){
  var list=skippedList(ts);
  var h='<div class="qcard done-card"><div class="big">⏭️</div><h2>You skipped '+list.length+' question'+(list.length>1?'s':'')+'</h2>'+
    '<p style="color:var(--ink-soft);font-size:14px;">Answer them now, or submit the tab as it is. Answers are marked only when you submit.</p>'+
    '<div class="skip-chips">'+list.map(function(i){ return '<button class="chip skip-go" data-i="'+i+'">Q'+(i+1)+'</button>'; }).join('')+'</div>'+
    '<div class="skip-btns"><button class="btn btn-primary" id="btnGoSkipped">Answer skipped questions</button><button class="btn" id="btnSubmitAnyway">Submit anyway</button></div></div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  var go=function(i){ ts.idx=i; ts.maxReached=Math.max(ts.maxReached,i); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); };
  document.getElementById('btnGoSkipped').addEventListener('click',function(){ go(list[0]); });
  document.querySelectorAll('.skip-go').forEach(function(b){ b.addEventListener('click',function(){ go(parseInt(b.dataset.i,10)); }); });
  document.getElementById('btnSubmitAnyway').addEventListener('click',function(){ ts.submitOK=true; renderFinished(); ts.submitOK=false; });
  saveState();
}
var _rfSkip = renderFinished;
renderFinished = function(){
  var ts=state.tabs[activeTab];
  if(MODE==='quiz' && !ts.submitOK && skippedList(ts).length){ renderSkipGate(ts); return; }
  _rfSkip();
  if(MODE==='learning'){
    var list=skippedList(ts);
    if(list.length){
      var card=document.querySelector('.done-card');
      if(card){ var d=document.createElement('div'); d.className='skip-btns';
        d.innerHTML='<button class="btn btn-primary" id="btnGoSkipped">Attempt skipped questions ('+list.length+')</button>';
        card.appendChild(d);
        document.getElementById('btnGoSkipped').addEventListener('click',function(){ ts.idx=list[0]; ts.recorded=false; renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); }); }
    }
  }
};


/* ================= approx answers (physics: within 1%) ================= */
var _amTools = answerMatches;
answerMatches = function(input,answer,accept,expr){
  if(expr==='approx'){
    var n1=parseNum(input); if(n1===null) return false;
    return [answer].concat(accept||[]).some(function(a){ var n2=parseNum(a); if(n2===null) return false; return Math.abs(n1-n2) <= Math.max(0.011*Math.abs(n2), 1e-9); });
  }
  return _amTools(input,answer,accept,expr);
};

/* ================= palette: every question already reached can be opened ================= */
statusOf = function(tabId,i){
  var ts=state.tabs[tabId];
  if(i>ts.maxReached) return 'locked';
  if(i===ts.idx) return 'current';
  var s=ts.items[i].status;
  if(s==='unanswered') return 'skipped';
  return s;
};

/* ================= on-screen keyboard ================= */
var KB={on:true, page:'num', target:null};
try{ var kbp=localStorage.getItem('sopaan-kb-pref'); if(kbp==='off') KB.on=false; }catch(e){}
function kbSave(){ try{ localStorage.setItem('sopaan-kb-pref', KB.on?'on':'off'); }catch(e){} }
var KEYS_NUM=[['7','8','9','(',')'],['4','5','6','−','/'],['1','2','3','.',','],['0',':','%','°','⌫'],['abc','←','→','Clear','Done']];
var KEYS_FRAC=[['7','8','9','/'],['4','5','6','−'],['1','2','3','space'],['0',',','⌫','Clear'],['abc','←','→','Done']];
var KEYS_ALG=[['7','8','9','x','y','n'],['4','5','6','+','−','a'],['1','2','3','×','÷','b'],['0','.','(',')','^','²'],['/','π','|','t','⌫','Clear'],['abc','←','→','Done']];
function kbLayoutFor(inp){ try{ var ts=state.tabs[activeTab], sl=SLIDES[activeTab][ts.idx], stp=sl.flat[parseInt(inp.dataset.step,10)]; var m=stp.expr, key=String(stp.a[inp.dataset.bkey]||'');
  if(m==='words'||m==='glist'||m==='angle') return 'abc'; if(m===true||m==='pow'||m==='primes') return 'alg';
  if(['fv','fe','fl','fm','fi','flist'].indexOf(m)>=0) return 'frac'; if(m==='dec'||m==='approx'||m==='dlist'||m==='set'||m==='coord'||m==='list'||m==='time') return 'num';
  if(/^[\-−]?\d+ \d+\/\d+$/.test(key)||/^[\-−]?\d+\/\d+$/.test(key)) return 'frac'; if(/[a-df-z]/i.test(key.replace(/pi/gi,''))) return /\d/.test(key)?'alg':'abc'; return 'num'; }catch(e){ return 'num'; } }
var KEYS_CALC=[['7','8','9','x','(',')'],['4','5','6','+','−','^'],['1','2','3','×','/','²'],['0','.','e','eˣ','√','ln'],['sin','cos','tan','t','⌫','Clear'],['abc','←','→','Done']];
var KEYS_ABC=[['q','w','e','r','t','y','u','i','o','p'],['a','s','d','f','g','h','j','k','l','-'],['z','x','c','v','b','n','m',',',':','/'],['123','space','←','→','⌫','Done']];
function kbBuild(){
  var el=document.getElementById('vkb'); if(!el){ el=document.createElement('div'); el.id='vkb'; el.className='vkb'; document.body.appendChild(el);
    el.addEventListener('pointerdown',function(e){ var b=e.target.closest('button[data-k]'); e.preventDefault(); if(b) kbPress(b.dataset.k); });
    el.addEventListener('mousedown',function(e){ e.preventDefault(); }); }
  var rows={num:KEYS_NUM,frac:KEYS_FRAC,alg:KEYS_ALG,abc:KEYS_ABC,calc:KEYS_CALC}[KB.page]||KEYS_NUM;
  el.innerHTML='<div class="vkb-top"><span>⌨️ Keyboard</span><button data-k="device" class="vkb-link">Use device keyboard</button></div>'+
    rows.map(function(r){ return '<div class="vkb-row">'+r.map(function(k){
      var cls='vkb-k'+(/^(abc|123|Done|Clear|⌫|←|→|space)$/.test(k)?' fn':'')+(k==='Done'?' done':'');
      return '<button type="button" class="'+cls+'" data-k="'+k+'">'+(k==='space'?'space':k)+'</button>'; }).join('')+'</div>'; }).join('');
  return el;
}
function kbShow(inp){ KB.target=inp; KB.home=kbLayoutFor(inp); KB.page=KB.home; if(!KB.on) return; var cp=document.getElementById('calcPanel'); if(cp&&cp.classList.contains('show')) return; var el=kbBuild(); var nb=document.querySelector('.navbar'); el.style.bottom=(nb?nb.getBoundingClientRect().height:0)+'px'; el.classList.add('show'); document.body.classList.add('kb-open'); setTimeout(function(){ var r=inp.getBoundingClientRect(), top=el.getBoundingClientRect().top; if(r.bottom>top-12) window.scrollBy({top:r.bottom-top+60,behavior:'smooth'}); else if(r.top<60) window.scrollBy({top:r.top-80,behavior:'smooth'}); },30); }
function kbHide(){ var el=document.getElementById('vkb'); if(el) el.classList.remove('show'); document.body.classList.remove('kb-open'); }
function kbInsert(s){
  var t=KB.target; if(!t||t.disabled) return;
  var a=t.selectionStart==null?t.value.length:t.selectionStart, b=t.selectionEnd==null?a:t.selectionEnd;
  t.value=t.value.slice(0,a)+s+t.value.slice(b); var p=a+s.length; try{ t.setSelectionRange(p,p); }catch(e){}
  t.dispatchEvent(new Event('input',{bubbles:true}));
}
function kbPress(k){
  var t=KB.target; if(k==='device'){ KB.on=false; kbSave(); kbHide(); document.querySelectorAll('.blank-input').forEach(function(i){ i.removeAttribute('inputmode'); }); if(t){ t.blur(); setTimeout(function(){ t.focus(); },50); } showToast('Device keyboard on. Tap ⌨️ on any blank to bring the on-screen keyboard back.'); return; }
  if(k==='Done'){ kbHide(); if(t) t.blur(); return; }
  if(k==='abc'||k==='123'){ KB.page=(k==='abc')?'abc':(KB.home&&KB.home!=='abc'?KB.home:'num'); kbBuild(); return; }
  if(!t) return;
  if(k==='⌫'){ var a=t.selectionStart, b=t.selectionEnd; if(a===b&&a>0){ t.value=t.value.slice(0,a-1)+t.value.slice(b); try{t.setSelectionRange(a-1,a-1);}catch(e){} } else { t.value=t.value.slice(0,a)+t.value.slice(b); try{t.setSelectionRange(a,a);}catch(e){} } t.dispatchEvent(new Event('input',{bubbles:true})); return; }
  if(k==='Clear'){ t.value=''; t.dispatchEvent(new Event('input',{bubbles:true})); return; }
  if(k==='←'||k==='→'){ var p=(t.selectionStart||0)+(k==='←'?-1:1); p=Math.max(0,Math.min(t.value.length,p)); try{t.setSelectionRange(p,p);}catch(e){} return; }
  var map={'−':'-','space':' '}; kbInsert(map[k]!==undefined?map[k]:k);
}
function kbWire(){
  document.querySelectorAll('.blank-input').forEach(function(inp){
    if(inp.dataset.kb) return; inp.dataset.kb='1';
    if(KB.on) inp.setAttribute('inputmode','none');
    inp.addEventListener('focus',function(){ kbShow(inp); });
    var btn=document.createElement('button'); btn.type='button'; btn.className='kb-toggle'; btn.title='On-screen keyboard'; btn.textContent='⌨️'; btn.tabIndex=-1;
    btn.addEventListener('mousedown',function(e){ e.preventDefault(); });
    btn.addEventListener('click',function(){ KB.on=true; kbSave(); document.querySelectorAll('.blank-input').forEach(function(i){ i.setAttribute('inputmode','none'); }); inp.focus(); kbShow(inp); });
    if(!inp.disabled) inp.insertAdjacentElement('afterend',btn);
  });
}
document.addEventListener('focusout',function(e){ setTimeout(function(){ var a=document.activeElement; if(!a||!a.classList||!a.classList.contains('blank-input')){ if(!document.querySelector('#vkb:hover')) kbHide(); } },120); });

/* ================= calculator ================= */
var CALC={expr:'', ans:0};
function calcEval(src){
  var s=String(src).replace(/×/g,'*').replace(/÷/g,'/').replace(/−/g,'-').replace(/π/g,'(PI)').replace(/Ans/g,'('+CALC.ans+')').replace(/\^/g,'**').replace(/√\(/g,'sqrt(').replace(/²/g,'**2').replace(/E/g,'*10**');
  s=s.replace(/(^|[(*\/+\-,])-/g,'$1(-1)*');
  if(/[^0-9+\-*/().,a-z A-Z]/.test(s)) throw 0;
  var ok=s.replace(/sin|cos|tan|asin|acos|atan|sqrt|log|ln|PI|abs/g,''); if(/[a-zA-Z]/.test(ok)) throw 0;
  var f=new Function('sin','cos','tan','asin','acos','atan','sqrt','log','ln','PI','abs','return ('+s+');');
  var d=Math.PI/180;
  var v=f(function(x){return Math.sin(x*d);},function(x){return Math.cos(x*d);},function(x){return Math.tan(x*d);},
    function(x){return Math.asin(x)/d;},function(x){return Math.acos(x)/d;},function(x){return Math.atan(x)/d;},Math.sqrt,Math.log10,Math.log,Math.PI,Math.abs);
  if(typeof v!=='number'||!isFinite(v)) throw 0; return v;
}
function fmtNum(v){ if(Math.abs(v)>=1e10||(Math.abs(v)<1e-6&&v!==0)) return v.toExponential(6).replace(/\.?0+e/,'e'); return String(parseFloat(v.toPrecision(10))); }
var CKEYS=[['sin(','cos(','tan(','√(','^','²'],['asin(','acos(','atan(','(',')','π'],['7','8','9','÷','⌫','AC'],['4','5','6','×','E','Ans'],['1','2','3','−','(−)','Insert'],['0','.','=','+']];
function openCalc(){
  var p=document.getElementById('calcPanel');
  if(!p){ p=document.createElement('div'); p.id='calcPanel'; p.className='tool-panel calc';
    p.innerHTML='<div class="tp-head"><b>🧮 Calculator</b><span class="tp-note">degrees · tap a blank, then Insert</span><button class="tp-x" data-c="close">✕</button></div>'+
      '<div class="calc-disp"><div class="calc-expr" id="calcExpr"></div><div class="calc-res" id="calcRes">0</div></div>'+
      '<div class="calc-keys">'+CKEYS.map(function(r){ return r.map(function(k){ return '<button type="button" data-c="'+k+'" class="'+(k==='='?'eq':(/^(AC|⌫|Insert)$/.test(k)?'fn':''))+'">'+({'sin(':'sin','cos(':'cos','tan(':'tan','asin(':'sin⁻¹','acos(':'cos⁻¹','atan(':'tan⁻¹','√(':'√'}[k]||k)+'</button>'; }).join(''); }).join('')+'</div>';
    document.body.appendChild(p);
    p.addEventListener('mousedown',function(e){ if(e.target.closest('button')) e.preventDefault(); });
    p.addEventListener('click',function(e){ var b=e.target.closest('button[data-c]'); if(!b) return; calcKey(b.dataset.c); });
  }
  kbHide(); var nb=document.querySelector('.navbar'); p.style.bottom=((nb?nb.getBoundingClientRect().height:0)+8)+'px'; p.classList.add('show'); document.body.classList.add('calc-open'); calcShow();
}
function calcShow(res){ document.getElementById('calcExpr').textContent=CALC.expr||' '; if(res!==undefined) document.getElementById('calcRes').textContent=res; }
function calcKey(k){
  if(k==='close'){ document.getElementById('calcPanel').classList.remove('show'); document.body.classList.remove('calc-open'); return; }
  if(k==='AC'){ CALC.expr=''; calcShow('0'); return; }
  if(k==='⌫'){ CALC.expr=CALC.expr.replace(/(asin\(|acos\(|atan\(|sin\(|cos\(|tan\(|√\(|Ans|.)$/,''); calcShow(); return; }
  if(k==='='){ try{ var v=calcEval(CALC.expr); CALC.ans=v; calcShow(fmtNum(v)); }catch(e){ calcShow('Error'); } return; }
  if(k==='(−)'){ CALC.expr+='−'; calcShow(); return; }
  if(k==='Insert'){ var r=document.getElementById('calcRes').textContent; if(KB.target && !KB.target.disabled && r!=='Error'){ KB.target.value=r; KB.target.dispatchEvent(new Event('input',{bubbles:true})); showToast('Inserted '+r+' into the blank.'); } else showToast('Tap a blank first, then press Insert.'); return; }
  CALC.expr+=k; calcShow();
}

/* ================= Desmos ================= */
var DESMOS_KEY='dcb31709b452b1cf9dc26972add0fda6', desmosCalc=null, desmosLoading=false;
function openDesmos(exprs){
  var p=document.getElementById('desmosPanel');
  if(!p){ p=document.createElement('div'); p.id='desmosPanel'; p.className='tool-panel desmos';
    p.innerHTML='<div class="tp-head"><b>📈 Desmos graphing calculator</b><button class="tp-x" id="desmosReset">Reset graph</button><button class="tp-x" id="desmosClose">✕</button></div><div id="desmosBox"><div class="desmos-msg">Loading Desmos…</div></div>';
    document.body.appendChild(p);
    document.getElementById('desmosClose').addEventListener('click',function(){ p.classList.remove('show'); });
    document.getElementById('desmosReset').addEventListener('click',function(){ if(desmosCalc) desmosSet(p._exprs||[]); });
  }
  p._exprs=exprs||[]; p.classList.add('show');
  if(window.Desmos){ desmosInit(); desmosSet(p._exprs); return; }
  if(desmosLoading) return; desmosLoading=true;
  var sc=document.createElement('script'); sc.src='https://www.desmos.com/api/v1.9/calculator.js?apiKey='+DESMOS_KEY;
  sc.onload=function(){ desmosInit(); desmosSet(p._exprs); };
  sc.onerror=function(){ desmosLoading=false; document.getElementById('desmosBox').innerHTML='<div class="desmos-msg">Desmos needs an internet connection. <a href="https://www.desmos.com/calculator" target="_blank" rel="noopener">Open Desmos in a new tab</a>.</div>'; };
  document.head.appendChild(sc);
}
function desmosInit(){ if(desmosCalc) return; var box=document.getElementById('desmosBox'); box.innerHTML=''; desmosCalc=Desmos.GraphingCalculator(box,{expressionsCollapsed:false,settingsMenu:false,border:false,degreeMode:true}); }
function desmosSet(exprs){ if(!desmosCalc) return; desmosCalc.setBlank(); (exprs||[]).forEach(function(e,i){ if(typeof e==='string') desmosCalc.setExpression({id:'e'+i,latex:e}); else desmosCalc.setExpression(Object.assign({id:'e'+i},e)); }); }

/* ================= toolbar on each question ================= */
var _rsTools = renderSlide;
renderSlide = function(){
  _rsTools();
  kbHide();
  if(activeTab==='theory'||activeTab==='report') return;
  var ts=state.tabs[activeTab]; if(!ts) return;
  var slide=SLIDES[activeTab][ts.idx], card=document.querySelector('#wrap .qcard');
  if(card && slide && slide.tools && slide.tools.length && !card.querySelector('.tool-bar')){
    var bar=document.createElement('div'); bar.className='tool-bar';
    bar.innerHTML=(slide.tools.indexOf('calc')>=0?'<button type="button" class="tool-btn" data-t="calc">🧮 Calculator</button>':'')+
                  (slide.tools.indexOf('desmos')>=0?'<button type="button" class="tool-btn" data-t="desmos">📈 Desmos graph</button>':'');
    card.insertBefore(bar, card.firstChild);
    bar.addEventListener('click',function(e){ var b=e.target.closest('[data-t]'); if(!b) return; if(b.dataset.t==='calc') openCalc(); else openDesmos(slide.desmos||[]); });
  }
  kbWire();
};



/* ================= signed fractions in text: {−3/4}, {3/−4}, {−2 1/3}, {p/q} ================= */
fr = function(s){ return String(s).replace(/&lt;(\/?)(b|sup|sub|i)>/g,'<$1$2>')
  .replace(/\{([−-]?\d+) (\d+)\/(\d+)\}/g,'<span class="mx">$1<span class="fq"><span>$2</span><span>$3</span></span></span>')
  .replace(/\{([−-]?[A-Za-z0-9]+)\/([−-]?[A-Za-z0-9]+)\}/g,'<span class="fq"><span>$1</span><span>$2</span></span>'); };
/* ================= BMA badge → main page of this sheet (theory hub) ================= */
(function(){
  var c=document.querySelector('.brand .crest'); if(!c) return;
  var a=document.createElement('button'); a.type='button'; a.className='crest crest-home'; a.title='Back to the main page (theory notes)'; a.setAttribute('aria-label','Main page');
  a.innerHTML='<img src="data:image/png;base64,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" alt="Brain and Mind"><span class="crest-h">⌂</span>'; c.parentNode.replaceChild(a,c);
  a.addEventListener('click',function(){
    if(!student||!MODE){ window.scrollTo({top:0,behavior:'smooth'}); return; }
    if(typeof kbHide==='function') kbHide(); if(typeof SP!=='undefined'&&SP.on) spToggle(false);
    var cp=document.getElementById('calcPanel'); if(cp) cp.classList.remove('show'); document.body.classList.remove('calc-open');
    activeTab = (typeof THEORY!=='undefined') ? 'theory' : TAB_DEFS[0].id;
    buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'});
  });
})();

/* ================= session clock: starts at sign-in and keeps running ================= */
var CLK={t0:null};
(function(){
  var row=document.querySelector('.brand .brand-row'); if(!row) return;
  var d=document.createElement('div'); d.className='bmasw off'; d.id='swBox'; d.title='Time since you signed in';
  d.innerHTML='<span class="bmasw-ic">⏱</span><span class="bmasw-t" id="swT">00:00</span>';
  row.appendChild(d); setInterval(swTick,1000);
})();
function swFmt(s){ s=Math.floor(s||0); var h=Math.floor(s/3600), m=Math.floor(s%3600/60), x=s%60; return (h?h+':'+String(m).padStart(2,'0'):String(m).padStart(2,'0'))+':'+String(x).padStart(2,'0'); }
function swTick(){
  var box=document.getElementById('swBox'); if(!box) return;
  if(student && !CLK.t0) CLK.t0=Date.now();
  if(!student) CLK.t0=null;
  box.classList.toggle('off',!CLK.t0);
  document.getElementById('swT').textContent = CLK.t0 ? swFmt((Date.now()-CLK.t0)/1000) : '00:00';
}
function swTab(){ try{ if(!state||!state.tabs||activeTab==='theory'||activeTab==='report') return null; return state.tabs[activeTab]||null; }catch(e){ return null; } }
var _rsSW = renderSlide;
renderSlide = function(){ _rsSW(); swTick(); };
var _rfSW = renderFinished;
renderFinished = function(){ _rfSW(); var done=document.querySelector('#wrap .done-card'); if(CLK.t0 && done && !done.querySelector('.bmasw-done')){ var p=document.createElement('p'); p.className='bmasw-done'; p.textContent='⏱ Time since sign-in: '+swFmt((Date.now()-CLK.t0)/1000); var h2=done.querySelector('h2'); if(h2) h2.insertAdjacentElement('afterend',p); else done.appendChild(p); } };

/* ================= scratchpad (Khan-style, 4 pens) ================= */
var SP={on:false, draw:true, color:'ink', size:3, erase:false, store:{}, key:null, cv:null, ctx:null, down:false, last:null};
var SP_COL={ink:null, blue:'#2563EB', red:'#DC2626', green:'#16A34A'};
function spInk(){ return getComputedStyle(document.documentElement).getPropertyValue('--ink').trim()||'#211E1A'; }
function spKey(){ var ts=swTab(); return ts ? (MODE+'|'+activeTab+'|'+ts.idx) : null; }
function spBuild(){
  if(SP.cv) return;
  var cv=document.createElement('canvas'); cv.id='spCanvas'; cv.className='sp-canvas'; document.body.appendChild(cv);
  var bar=document.createElement('div'); bar.id='spBar'; bar.className='sp-bar';
  bar.innerHTML='<span class="sp-lbl">✏️ Scratchpad</span>'+
    ['ink','blue','red','green'].map(function(c){ return '<button type="button" class="sp-pen" data-c="'+c+'" title="'+(c==='ink'?'black':c)+' pen"><i style="background:'+(c==='ink'?'var(--ink)':SP_COL[c])+'"></i></button>'; }).join('')+
    '<button type="button" class="sp-tool" data-t="erase" title="Eraser">🧽</button><button type="button" class="sp-tool" data-t="size" title="Pen size">●</button><button type="button" class="sp-tool" data-t="scroll" title="Pause drawing to scroll or answer">✋</button>'+
    '<button type="button" class="sp-tool" data-t="clear" title="Clear page">🗑</button><button type="button" class="sp-tool" data-t="close" title="Close scratchpad">✕</button>';
  document.body.appendChild(bar);
  bar.addEventListener('click',function(e){ var b=e.target.closest('button'); if(!b) return;
    if(b.dataset.c){ SP.color=b.dataset.c; SP.erase=false; SP.draw=true; }
    else if(b.dataset.t==='erase'){ SP.erase=true; SP.draw=true; }
    else if(b.dataset.t==='size'){ SP.size = SP.size===3?6:(SP.size===6?1.5:3); b.textContent = SP.size===6?'⬤':(SP.size===1.5?'·':'●'); }
    else if(b.dataset.t==='scroll'){ SP.draw=!SP.draw; }
    else if(b.dataset.t==='clear'){ spClear(); }
    else if(b.dataset.t==='close'){ spToggle(false); return; }
    spUI(); });
  SP.cv=cv; SP.ctx=cv.getContext('2d');
  cv.addEventListener('pointerdown',function(e){ if(!SP.draw) return; e.preventDefault(); cv.setPointerCapture(e.pointerId); SP.down=true; SP.last=spPt(e); spDot(SP.last); });
  cv.addEventListener('pointermove',function(e){ if(!SP.down) return; e.preventDefault(); var p=spPt(e); spLine(SP.last,p); SP.last=p; });
  var up=function(){ if(SP.down){ SP.down=false; spSave(); } };
  cv.addEventListener('pointerup',up); cv.addEventListener('pointercancel',up); cv.addEventListener('pointerleave',up);
  window.addEventListener('resize',function(){ if(SP.on) spFit(true); });
}
function spPt(e){ var r=SP.cv.getBoundingClientRect(); return {x:e.clientX-r.left, y:e.clientY-r.top}; }
function spStyle(){ var c=SP.ctx; c.lineCap='round'; c.lineJoin='round'; c.globalCompositeOperation=SP.erase?'destination-out':'source-over'; c.strokeStyle=c.fillStyle=(SP.color==='ink'?spInk():SP_COL[SP.color]); c.lineWidth=SP.erase?22:SP.size; }
function spDot(p){ spStyle(); var c=SP.ctx; c.beginPath(); c.arc(p.x,p.y,(SP.erase?11:SP.size/2),0,Math.PI*2); c.fill(); }
function spLine(a,b){ spStyle(); var c=SP.ctx; c.beginPath(); c.moveTo(a.x,a.y); c.lineTo(b.x,b.y); c.stroke(); }
function spSave(){ if(SP.key&&SP.cv){ try{ SP.store[SP.key]=SP.cv.toDataURL(); }catch(e){} } }
function spClear(){ if(!SP.ctx) return; SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.clearRect(0,0,SP.cv.width,SP.cv.height); SP.ctx.restore(); if(SP.key) delete SP.store[SP.key]; }
function spFit(keep){
  var wrap=document.getElementById('wrap'); if(!wrap||!SP.cv) return;
  var r=wrap.getBoundingClientRect(), top=r.top+window.scrollY, h=Math.max(wrap.scrollHeight, window.innerHeight-r.top)+40, w=document.documentElement.clientWidth;
  var old=keep&&SP.key?SP.store[SP.key]:null, dpr=window.devicePixelRatio||1;
  SP.cv.style.top=top+'px'; SP.cv.style.left='0px'; SP.cv.style.width=w+'px'; SP.cv.style.height=h+'px';
  SP.cv.width=Math.round(w*dpr); SP.cv.height=Math.round(h*dpr); SP.ctx.setTransform(dpr,0,0,dpr,0,0);
  if(old){ var im=new Image(); im.onload=function(){ SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.drawImage(im,0,0); SP.ctx.restore(); }; im.src=old; }
}
function spLoad(){ spSave(); SP.key=spKey(); spFit(false); var d=SP.key&&SP.store[SP.key]; if(d){ var im=new Image(); im.onload=function(){ SP.ctx.save(); SP.ctx.setTransform(1,0,0,1,0,0); SP.ctx.drawImage(im,0,0); SP.ctx.restore(); }; im.src=d; } }
function spUI(){
  var bar=document.getElementById('spBar'); if(!bar) return;
  bar.querySelectorAll('.sp-pen').forEach(function(b){ b.classList.toggle('on', !SP.erase && SP.draw && b.dataset.c===SP.color); });
  bar.querySelector('[data-t=erase]').classList.toggle('on', SP.erase && SP.draw);
  bar.querySelector('[data-t=scroll]').classList.toggle('on', !SP.draw);
  SP.cv.classList.toggle('passive', !SP.draw);
  var fb=document.getElementById('spFab'); if(fb) fb.classList.toggle('on',SP.on);
}
function spToggle(on){
  spBuild(); SP.on=(on===undefined)?!SP.on:on;
  document.body.classList.toggle('sp-open',SP.on); SP.cv.style.display=SP.on?'block':'none'; document.getElementById('spBar').style.display=SP.on?'flex':'none';
  if(SP.on){ SP.draw=true; SP.erase=false; spLoad(); if(typeof kbHide==='function') kbHide(); } else { spSave(); }
  spUI();
}
(function(){ var f=document.createElement('button'); f.type='button'; f.id='spFab'; f.className='sp-fab'; f.innerHTML='✏️ <span>Scratchpad</span>'; f.title='Open a scratchpad to write your working'; f.addEventListener('click',function(){ spToggle(); }); document.body.appendChild(f); })();
var _rsSP = renderSlide;
renderSlide = function(){ _rsSP(); var fab=document.getElementById('spFab'); var q=!!swTab(); if(fab) fab.style.display=q?'':'none'; if(!q && SP.on) spToggle(false); if(SP.on) setTimeout(spLoad,30); };


/* ================= v4: attempt classification ================= */
function v4Class(item){
  if(!item) return 'un';
  if(item.status==='skipped') return 'sk';
  if(item.status==='unanswered') return 'un';
  if(item.stepStates){ // step question
    if(item.status!=='correct' && item.status!=='revealed') return 'un';
    if(item.status==='revealed' || item.stepStates.some(function(s){return s.status==='revealed';})) return 'w';
    return item.stepStates.some(function(s){return (s.attempts||0)>0;}) ? 'c2' : 'c1';
  }
  if(item.status==='revealed') return 'w';
  if(item.status==='correct') return (item.attempts||0)>0 ? 'c2' : 'c1';
  if(item.status==='wrong'||item.status==='incorrect') return 'w';
  return 'un';
}
function v4Counts(items){ var c={n:items.length,c1:0,c2:0,w:0,sk:0,un:0}; items.forEach(function(it){ c[v4Class(it)]++; }); return c; }

/* ================= v4: My record with attempt columns ================= */
renderRecord = function(){
  showChrome(false);
  var tabLabel=function(id){ var t=TAB_DEFS.find(function(x){return x.id===id;}); return t?t.label:id; };
  var title=(document.querySelector('.chapter-title')||{}).textContent||'';
  var h='<div class="rec-card"><h2>'+esc(student.name)+'’s record</h2><p class="rec-empty" style="margin:0 0 12px;">Roll '+esc(student.roll)+(title?' · '+esc(title):'')+'</p>';
  var st=appState.learning;
  h+='<h3>📘 Learning Sheet — attempts</h3><p class="v4leg"><b>1st ✓</b> correct on the first attempt · <b>2nd ✓</b> correct on the second attempt · <b>Wrong</b> still wrong after two attempts (answer revealed) · <b>Skip</b> skipped<span class="v4left"> · <b>Left</b> not done yet</span></p>';
  if(!st){ h+='<p class="rec-empty">Not started yet.</p>'; }
  else {
    var T={n:0,c1:0,c2:0,w:0,sk:0,un:0};
    h+='<div class="rec-table-wrap"><table class="rec-table v4rec"><thead><tr><th>Sheet</th><th>Qs</th><th>1st ✓</th><th>2nd ✓</th><th>Wrong</th><th>Skip</th><th class="v4left">Left</th></tr></thead><tbody>';
    TAB_DEFS.forEach(function(td){ var tt=st.tabs[td.id]; if(!tt||!tt.items||!tt.items.length) return; var c=v4Counts(tt.items);
      ['n','c1','c2','w','sk','un'].forEach(function(k){ T[k]+=c[k]; });
      h+='<tr><td>'+td.label+'</td><td>'+c.n+'</td><td class="v4g">'+c.c1+'</td><td class="v4o">'+c.c2+'</td><td class="v4r">'+c.w+'</td><td>'+c.sk+'</td><td class="v4left">'+c.un+'</td></tr>'; });
    h+='<tr class="v4tot"><td>Total</td><td>'+T.n+'</td><td class="v4g">'+T.c1+'</td><td class="v4o">'+T.c2+'</td><td class="v4r">'+T.w+'</td><td>'+T.sk+'</td><td class="v4left">'+T.un+'</td></tr>';
    h+='</tbody></table></div>';
    var doneN=T.c1+T.c2+T.w; if(doneN){ h+='<p class="v4sum">Of '+doneN+' questions answered: <b>'+Math.round(T.c1/doneN*100)+'%</b> right first time, <b>'+Math.round(T.c2/doneN*100)+'%</b> right on the second try, <b>'+Math.round(T.w/doneN*100)+'%</b> still wrong after two tries.</p>'; }
  }
  var q=appState.quiz;
  h+='<h3>📝 Quiz Mode</h3>';
  if(!q){ h+='<p class="rec-empty">Not started yet.</p>'; }
  else {
    h+='<div class="rec-table-wrap"><table class="rec-table v4rec"><thead><tr><th>Sheet</th><th>Qs</th><th>Status</th><th>Correct</th><th>Wrong</th></tr></thead><tbody>';
    TAB_DEFS.forEach(function(td){ var tt=q.tabs[td.id]; if(!tt||!tt.items||!tt.items.length) return; var n=tt.items.length, cor=0, att=0;
      tt.items.forEach(function(it){ if(it.status!=='unanswered'||it.choice!==undefined) att++; });
      var rec=records.filter(function(r){ return r.mode==='quiz'&&r.tab===td.id; })[0];
      if(rec){ cor=rec.correct; att=Math.max(att,rec.total); }
      h+='<tr><td>'+td.label+'</td><td>'+n+'</td><td>'+(rec?'Finished':att+' / '+n)+'</td><td class="v4g">'+(rec?cor:'—')+'</td><td class="v4r">'+(rec?(rec.total-cor):'—')+'</td></tr>'; });
    h+='</tbody></table></div>';
  }
  h+='</div><div class="rec-card"><h3>Finished sheets (latest first)</h3>';
  if(!records.length){ h+='<p class="rec-empty">No sheets finished yet. Each time you finish a sheet, your score is recorded here.</p>'; }
  else {
    h+='<div class="rec-table-wrap"><table class="rec-table v4rec"><thead><tr><th>When</th><th>Mode</th><th>Sheet</th><th>Score</th><th>1st ✓</th><th>2nd ✓</th><th>Wrong</th></tr></thead><tbody>';
    records.forEach(function(r){ h+='<tr><td>'+fmtDate(r.at)+'</td><td>'+(r.mode==='quiz'?'Quiz':'Learning')+'</td><td>'+tabLabel(r.tab)+'</td><td>'+r.correct+' / '+r.total+'</td><td>'+(r.c1!=null?r.c1:'—')+'</td><td>'+(r.c2!=null?r.c2:'—')+'</td><td>'+(r.w!=null?r.w:(r.mode==='quiz'?r.total-r.correct:'—'))+'</td></tr>'; });
    h+='</tbody></table></div>';
  }
  h+='</div><button class="btn btn-primary" id="btnBack">'+(MODE?'Back to practice':'Choose a mode')+'</button>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('btnBack').addEventListener('click', function(){ if(MODE){ showChrome(true); buildTabbar(); renderSlide(); } else renderModePicker(); });
  window.scrollTo({top:0});
};
var _v4add = addRecord;
addRecord = function(mode, tabId, correct, revealed, skipped, total){
  _v4add(mode, tabId, correct, revealed, skipped, total);
  try{ if(mode==='learning'&&records[0]){ var c=v4Counts(state.tabs[tabId].items); records[0].c1=c.c1; records[0].c2=c.c2; records[0].w=c.w; saveState(); } }catch(e){}
};

/* ================= v4: celebration ================= */
function v4Cracker(){
  var ctx=ensureAudio(); if(!ctx) return; try{ if(ctx.state==='suspended') ctx.resume(); }catch(e){}
  var now=ctx.currentTime;
  function pop(t, vol, dur, hp){
    var len=Math.floor(ctx.sampleRate*dur), buf=ctx.createBuffer(1,len,ctx.sampleRate), d=buf.getChannelData(0);
    for(var i=0;i<len;i++){ d[i]=(Math.random()*2-1)*Math.pow(1-i/len,3); }
    var src=ctx.createBufferSource(); src.buffer=buf;
    var f=ctx.createBiquadFilter(); f.type='highpass'; f.frequency.value=hp;
    var g=ctx.createGain(); g.gain.setValueAtTime(vol,t); g.gain.exponentialRampToValueAtTime(0.001,t+dur);
    src.connect(f); f.connect(g); g.connect(ctx.destination); src.start(t); src.stop(t+dur+0.02);
  }
  pop(now,0.9,0.35,300);                                   // big bang
  for(var k=0;k<14;k++){ pop(now+0.35+Math.random()*1.3, 0.25+Math.random()*0.35, 0.05+Math.random()*0.08, 1500+Math.random()*2500); } // crackles
  [523.25,659.25,783.99,1046.5].forEach(function(fq,i){ var o=ctx.createOscillator(), g=ctx.createGain(); o.type='triangle'; o.frequency.value=fq;
    var t=now+0.15+i*0.12; g.gain.setValueAtTime(0.0001,t); g.gain.exponentialRampToValueAtTime(0.18,t+0.03); g.gain.exponentialRampToValueAtTime(0.001,t+0.5);
    o.connect(g); g.connect(ctx.destination); o.start(t); o.stop(t+0.55); });
}
function v4Confetti(){
  var cv=document.createElement('canvas'); cv.className='v4conf'; document.body.appendChild(cv);
  var W=cv.width=window.innerWidth*(window.devicePixelRatio||1), H=cv.height=window.innerHeight*(window.devicePixelRatio||1), s=(window.devicePixelRatio||1);
  var ctx=cv.getContext('2d'), cols=['#e8b13a','#d9534f','#2e86de','#27ae60','#9b59b6','#f39c12','#1abc9c','#ff6b9a'], P=[];
  function burst(x,y,n){ for(var i=0;i<n;i++){ var a=Math.random()*Math.PI*2, v=(4+Math.random()*9)*s;
    P.push({x:x,y:y,vx:Math.cos(a)*v,vy:Math.sin(a)*v-6*s,w:(6+Math.random()*7)*s,h:(4+Math.random()*5)*s,r:Math.random()*6,vr:(Math.random()-.5)*.4,c:cols[i%cols.length],life:0,flyer:Math.random()<.25}); } }
  burst(W*0.2,H*0.35,90); burst(W*0.8,H*0.35,90); setTimeout(function(){ burst(W*0.5,H*0.25,120); },380); setTimeout(function(){ burst(W*0.35,H*0.3,70); burst(W*0.65,H*0.3,70); },800);
  var t0=performance.now();
  (function frame(t){
    ctx.clearRect(0,0,W,H);
    P.forEach(function(p){ p.vy+=0.22*s; p.vx*=0.985; p.vy*=0.985; p.x+=p.vx; p.y+=p.vy; p.r+=p.vr; p.life++;
      ctx.save(); ctx.translate(p.x,p.y); ctx.rotate(p.r); ctx.fillStyle=p.c;
      if(p.flyer){ ctx.fillRect(-p.w*1.4,-1.5*s,p.w*2.8,3*s); } else { ctx.fillRect(-p.w/2,-p.h/2,p.w,p.h*Math.abs(Math.cos(p.life/6))); }
      ctx.restore(); });
    if(t-t0<4200) requestAnimationFrame(frame); else cv.remove();
  })(t0);
}
function v4NextTab(){
  var i=TAB_DEFS.findIndex(function(t){return t.id===activeTab;});
  for(var j=i+1;j<TAB_DEFS.length;j++){ var id=TAB_DEFS[j].id; if(id!=='theory' && SLIDES[id] && SLIDES[id].length) return TAB_DEFS[j]; }
  return null;
}
function v4Celebrate(){
  var done=document.querySelector('#wrap .done-card'); if(!done || done.dataset.v4) return; done.dataset.v4='1';
  var ts=state.tabs[activeTab], c=v4Counts(ts.items), n=ts.items.length;
  var first=(student&&student.name)?String(student.name).split(' ')[0]:'';
  var pct=MODE==='quiz'?null:Math.round((c.c1+c.c2)/Math.max(n,1)*100);
  var msg = pct===null ? 'You finished this sheet!' : (pct>=90?'Outstanding work!':pct>=75?'Excellent effort!':pct>=50?'Well done — keep going!':'Great persistence — every try makes you stronger!');
  var banner=document.createElement('div'); banner.className='v4ban';
  banner.innerHTML='<div class="v4trophy">🏆</div><div class="v4h">Congratulations'+(first?', '+esc(first):'')+'!</div><div class="v4m">'+msg+'</div>'+
    (MODE==='quiz'?'':'<div class="v4pills"><span class="v4p g">✅ '+c.c1+' first attempt</span><span class="v4p o">🔁 '+c.c2+' second attempt</span><span class="v4p r">❌ '+c.w+' finally wrong</span>'+(c.sk?'<span class="v4p s">⏭ '+c.sk+' skipped</span>':'')+'</div>');
  done.insertBefore(banner, done.firstChild);
  var nx=v4NextTab(), wrapB=document.createElement('div'); wrapB.className='v4next';
  if(nx){ wrapB.innerHTML='<button class="btn btn-primary v4go" id="v4Next">Next sheet: '+nx.label+' →</button>'; }
  else if(SLIDES.report!==undefined || TAB_DEFS.some(function(t){return t.id==='report';})){ wrapB.innerHTML='<button class="btn btn-primary v4go" id="v4Next">📊 View my report →</button>'; }
  else { wrapB.innerHTML='<button class="btn btn-primary v4go" id="v4Next">⌂ Back to the home page</button>'; }
  banner.appendChild(wrapB);
  document.getElementById('v4Next').addEventListener('click',function(){
    var t=nx?nx.id:(TAB_DEFS.some(function(x){return x.id==='report';})?'report':(TAB_DEFS[0]&&TAB_DEFS[0].id));
    activeTab=t; showChrome(true); buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); });
  setTimeout(function(){ var r=banner.getBoundingClientRect(); window.scrollBy({top:r.top-110,behavior:'smooth'}); },60);
  v4Confetti(); v4Cracker();
}
var _v4rf = renderFinished;
renderFinished = function(){ _v4rf.apply(this,arguments); try{ v4Celebrate(); }catch(e){ console.log('v4',e); } };


/* ================= calculus answer mode ================= */
function calcCompile(src){
  var s=String(src).replace(/\s+/g,'').replace(/[×∗·]/g,'*').replace(/÷/g,'/').replace(/[−–—]/g,'-')
    .replace(/²/g,'^2').replace(/³/g,'^3').replace(/π/g,'#').replace(/eˣ/g,'e^x');
  if(s.indexOf('=')>=0) s=s.slice(s.lastIndexOf('=')+1);
  var FN=['sqrt','cbrt','abs','ln','log','exp','sin','cos','tan','sec','csc','cot','pi'];
  var i=0,toks=[];
  while(i<s.length){
    var ch=s[i];
    if(/[0-9.]/.test(ch)){ var j=i; while(j<s.length&&/[0-9.]/.test(s[j])) j++; toks.push({k:'n',v:parseFloat(s.slice(i,j))}); i=j; continue; }
    if(ch==='√'){ toks.push({k:'f',v:'sqrt'}); i++; continue; }
    if(ch==='∛'){ toks.push({k:'f',v:'cbrt'}); i++; continue; }
    if(/[a-zA-Z#]/.test(ch)){
      var hit=null; for(var q=0;q<FN.length;q++){ if(s.substr(i,FN[q].length).toLowerCase()===FN[q]){ hit=FN[q]; break; } }
      if(hit==='pi'){ toks.push({k:'v',v:'#'}); i+=2; continue; }
      if(hit){ toks.push({k:'f',v:hit}); i+=hit.length; continue; }
      toks.push({k:'v',v:ch}); i++; continue; }
    if('+-*/^()|'.indexOf(ch)>=0){ toks.push({k:ch}); i++; continue; }
    return null;
  }
  // absolute value bars -> abs( )
  var t2=[],open=false; for(var a=0;a<toks.length;a++){ var tk=toks[a]; if(tk.k==='|'){ if(!open){ t2.push({k:'f',v:'abs'}); t2.push({k:'('}); open=true; } else { t2.push({k:')'}); open=false; } } else t2.push(tk); }
  toks=t2;
  var out=[];
  for(var t=0;t<toks.length;t++){ var A=toks[t], B=out[out.length-1];
    if(B&&(B.k==='n'||B.k==='v'||B.k===')')&&(A.k==='n'||A.k==='v'||A.k==='('||A.k==='f')) out.push({k:'&'});
    out.push(A); }
  var p=0; function pk(){ return out[p]; }
  var F={sqrt:Math.sqrt,cbrt:Math.cbrt,ln:Math.log,log:function(x){return Math.log(x)/Math.LN10;},exp:Math.exp,sin:Math.sin,cos:Math.cos,tan:Math.tan,
    sec:function(x){return 1/Math.cos(x);},csc:function(x){return 1/Math.sin(x);},cot:function(x){return 1/Math.tan(x);},abs:Math.abs};
  function E(){ var n=T(); while(pk()&&(pk().k==='+'||pk().k==='-')){ var o=out[p++].k,r=T(); n=(function(l,r,o){return function(e){return o==='+'?l(e)+r(e):l(e)-r(e);};})(n,r,o);} return n; }
  function T(){ var n=I(); while(pk()&&(pk().k==='*'||pk().k==='/')){ var o=out[p++].k,r=I(); n=(function(l,r,o){return function(e){return o==='*'?l(e)*r(e):l(e)/r(e);};})(n,r,o);} return n; }
  function I(){ var n=U(); while(pk()&&pk().k==='&'){ p++; var r=P(); n=(function(l,r){return function(e){return l(e)*r(e);};})(n,r);} return n; }
  function U(){ if(pk()&&pk().k==='-'){ p++; var u=U(); return function(e){return -u(e);}; } if(pk()&&pk().k==='+'){ p++; return U(); } return P(); }
  function P(){ var b=Aa(); if(pk()&&pk().k==='^'){ p++; var x=U(); return function(e){return Math.pow(b(e),x(e));}; } return b; }
  function Aa(){ var t=out[p++]; if(!t) throw 0;
    if(t.k==='n') return function(){return t.v;};
    if(t.k==='v'){ if(t.v==='#') return function(){return Math.PI;}; if(t.v==='e') return function(){return Math.E;}; return function(e){return e[t.v];}; }
    if(t.k==='('){ var n=E(); if(!pk()||pk().k!==')') throw 0; p++; return n; }
    if(t.k==='f'){ var fn=F[t.v]; var ex=null;
      if(pk()&&pk().k==='^'){ p++; ex=Aa(); if(pk()&&pk().k==='&') p++; }            // sin^2(x)
      var arg; if(pk()&&pk().k==='('){ p++; arg=E(); if(!pk()||pk().k!==')') throw 0; p++; } else { arg=P(); while(pk()&&pk().k==='&'&&out[p+1]&&(out[p+1].k==='n'||(out[p+1].k==='v'&&out[p+1].v!=='e'))){ p++; var nx=P(); arg=(function(l,r){return function(e){return l(e)*r(e);};})(arg,nx); } }
      return ex? function(e){ return Math.pow(fn(arg(e)),ex(e)); } : function(e){ return fn(arg(e)); }; }
    throw 0; }
  try{ var f=E(); if(p!==out.length) return null; return f; }catch(e){ return null; }
}
function calcEqual(input,answer){
  var f=calcCompile(input), g=calcCompile(answer); if(!f||!g) return false;
  var hits=0;
  for(var trial=0;trial<14;trial++){
    var env={}; 'abcdfghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(function(c){ env[c]=0.35+Math.random()*2.3; });
    var x=f(env), y=g(env); if(!isFinite(x)||!isFinite(y)) continue;
    if(Math.abs(x-y)>1e-6*Math.max(1,Math.abs(x),Math.abs(y))) return false; hits++;
  }
  return hits>=4;
}
(function(){
  var _am=answerMatches;
  answerMatches=function(input,answer,accept,expr){
    if(expr==='expanded'){ if(input===undefined||input===null||String(input).trim()==='') return false; if(/[()\[\]]/.test(String(input))) return false; return _am.call(this,input,answer,accept,true); }
    if(expr==='calc'){ if(input===undefined||input===null||String(input).trim()==='') return false;
      if(calcEqual(input,answer)) return true; return (accept||[]).some(function(a){ return calcEqual(input,a); }); }
    return _am.apply(this,arguments); };
  var _kl=kbLayoutFor;
  kbLayoutFor=function(inp){ try{ var ts=state.tabs[activeTab], sl=SLIDES[activeTab][ts.idx], stp=sl.flat[parseInt(inp.dataset.step,10)]; if(stp.expr==='calc') return 'calc'; }catch(e){} return _kl(inp); };
  var _kp=kbPress;
  kbPress=function(k){ var m={'eˣ':'e^(','√':'√(','ln':'ln(','sin':'sin(','cos':'cos(','tan':'tan('}; if(KB.page==='calc'&&m[k]){ kbInsert(m[k]); return; } return _kp(k); };
})();

renderLogin();
})();
</script>
</body>
</html>
