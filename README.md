<html lang="th">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Aegean – ระบบจัดตารางกะ</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Thai:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#F4F5F2;--card:#fff;--ink:#1D2A1F;--mute:#737D74;--line:#E4E8E2;--pri:#2B5A3A;--pri-s:#E3EFE6;--red:#C8445A;--red-s:#FBE7EA;--amb:#A87408;--amb-s:#FCF2D8;--grn:#23885A;--grn-s:#DFF3E9;--gray:#EDEFEB;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#121712;--card:#1B221C;--ink:#EEF3EE;--mute:#9BA69C;--line:#2B352C;--pri:#8FC79F;--pri-s:#1F3326;--red-s:#432029;--amb-s:#3B2F12;--grn-s:#17382B;--gray:#252E26;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#121712;--card:#1B221C;--ink:#EEF3EE;--mute:#9BA69C;--line:#2B352C;--pri:#8FC79F;--pri-s:#1F3326;--red-s:#432029;--amb-s:#3B2F12;--grn-s:#17382B;--gray:#252E26;color-scheme:dark}
*{box-sizing:border-box}html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font:400 15px/1.55 'Noto Sans Thai',system-ui,sans-serif}
button,input,select,textarea{font:inherit;color:inherit}button{cursor:pointer;border:0;background:none}
button:focus-visible,input:focus-visible,label:focus-within{outline:2px solid var(--pri);outline-offset:2px}
.wrap{max-width:900px;margin:0 auto;padding:16px 16px 120px}
header{display:flex;align-items:center;gap:12px;margin-bottom:14px}
.lg{position:relative;width:58px;height:58px;flex:none;display:grid;place-items:center;cursor:pointer;-webkit-tap-highlight-color:transparent;transition:transform .3s cubic-bezier(.3,1.6,.5,1)}
.lg:active{transform:scale(.9)}
.lg::before{content:"";position:absolute;inset:0;border-radius:50%;padding:2.5px;background:conic-gradient(#8fe3b8,#c4b5ff,#ffc2b0,#fff0a0,#8fe3b8);-webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);-webkit-mask-composite:xor;mask:linear-gradient(#000 0 0) content-box exclude,linear-gradient(#000 0 0);animation:spin 5s linear infinite reverse}
.lg::after{content:"";position:absolute;top:-3px;left:50%;width:9px;height:9px;margin-left:-4.5px;border-radius:50%;background:#ff8fab;box-shadow:0 0 0 2px var(--bg);transform-origin:4.5px 32px;animation:spin 3s linear infinite}
.logo{width:46px;height:46px;border-radius:50%;background:#fff;animation:spin 12s linear infinite}
.lg.fast .logo{animation-duration:.7s}.lg.fast::before{animation-duration:.9s}.lg.fast::after{animation-duration:.6s}
@keyframes spin{to{transform:rotate(360deg)}}
@media(prefers-reduced-motion:reduce){.lg::before,.lg::after,.logo{animation:none}}
.hd{flex:1;min-width:0}.brand{font-weight:700;font-size:13px;color:var(--pri);line-height:1.2}
h1{font-size:21px;margin:0;font-weight:700;line-height:1.3}.sub{color:var(--mute);font-size:13px}
.circs{display:flex;gap:8px}
.circ{width:42px;height:42px;border-radius:50%;background:var(--card);border:1px solid var(--line);display:grid;place-items:center;position:relative;color:var(--ink)}
.circ svg{width:19px;height:19px;stroke:currentColor;fill:none;stroke-width:1.7;stroke-linecap:round;stroke-linejoin:round}
.circ b{position:absolute;top:-3px;right:-3px;min-width:18px;height:18px;border-radius:9px;background:var(--red);color:#fff;font-size:11px;line-height:18px;padding:0 4px}
.tabs{display:flex;gap:4px;background:var(--card);border:1px solid var(--line);border-radius:16px;padding:4px;margin-bottom:14px;position:sticky;top:env(safe-area-inset-top,0px);z-index:5}
.tab{flex:1;padding:9px 2px;border-radius:12px;font-weight:600;font-size:12.5px;color:var(--mute)}.tab.on{background:var(--pri);color:var(--bg)}
.card{background:var(--card);border:1px solid var(--line);border-radius:22px;padding:16px;margin-bottom:14px}
.ch{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;gap:8px}.ch h2{margin:0;font-size:17px}
.link{color:var(--pri);font-weight:600;font-size:14px}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:14px}
.stat{background:var(--card);border-radius:18px;padding:12px 14px;border:1px solid var(--line)}.stat b{display:block;font-size:22px}.stat span{font-size:12px;color:var(--mute)}
.drow{display:grid;grid-template-columns:44px 1fr 58px;gap:8px;align-items:center;margin-bottom:8px}.drow>b{font-size:15px}.drow .st{text-align:right;font-weight:600;font-size:14px}
.chips{display:flex;gap:6px;flex-wrap:wrap}.chip{flex:1;min-width:64px;text-align:center;padding:12px 6px;border-radius:12px;font-size:14px;background:var(--gray);color:var(--mute)}
.ok{background:var(--grn-s);color:var(--grn)}.warn{background:var(--amb-s);color:var(--amb)}.bad{background:var(--red-s);color:var(--red)}.closed{background:var(--gray);color:var(--mute)}
.t-ok{color:var(--grn)}.t-warn{color:var(--amb)}.t-bad{color:var(--red)}.t-closed{color:var(--mute)}
.scroll{overflow-x:auto;margin:0 -4px;padding:0 4px}
.grid{display:grid;grid-template-columns:110px repeat(7,minmax(90px,1fr));min-width:770px;gap:6px}
.dh{text-align:center;padding:8px 4px;border-radius:14px;font-weight:600;font-size:13px}.dh small{display:block;font-weight:500;font-size:11.5px}
.emp{position:sticky;left:0;background:var(--card);z-index:2;display:flex;align-items:center;gap:8px;padding:4px 6px 4px 0}
.av{width:34px;height:34px;border-radius:50%;display:grid;place-items:center;font-weight:700;font-size:13px;flex:none;object-fit:cover;background:var(--pri-s);color:var(--pri)}
.av.big{width:64px;height:64px;font-size:22px}
.emp b{display:block;font-size:13.5px;line-height:1.2}.emp small{font-size:11.5px;color:var(--mute)}
.cell{min-height:56px;border-radius:12px;background:var(--bg);display:flex}.cell.x{background:repeating-linear-gradient(45deg,var(--gray),var(--gray) 6px,var(--bg) 6px,var(--bg) 12px)}
.cell .add{width:100%;color:var(--mute);font-size:18px;opacity:.6;border-radius:12px;border:1.5px dashed var(--line)}
.shift{width:100%;border-radius:12px;padding:6px 8px;text-align:left;border-left:4px solid var(--pri);background:var(--pri-s);font-size:12px}.shift b{display:block;font-size:12.5px}.shift span{color:var(--mute);font-size:11px}
.stp{display:flex;justify-content:center;gap:6px;margin-top:4px}.stp button{width:22px;height:22px;border-radius:50%;background:var(--card);border:1px solid var(--line);line-height:1}
.hint{font-size:13px;color:var(--mute);margin:0 0 12px}
.item{display:flex;gap:12px;align-items:flex-start;padding:13px;border-radius:16px;margin-bottom:10px}.item p{margin:0}.item .t{font-weight:600}
.act{margin-top:8px;display:flex;gap:8px;flex-wrap:wrap;align-items:center}
.btn{padding:9px 15px;border-radius:12px;font-weight:600;font-size:13.5px;background:var(--pri);color:var(--bg)}.btn.ghost{background:var(--card);color:var(--ink);border:1px solid var(--line)}
.btn[disabled]{opacity:.45}a.btn{display:inline-block;text-decoration:none}
.req{border:1px solid var(--line);border-radius:18px;padding:16px;margin-bottom:12px;background:var(--card)}.req h3{margin:0 0 2px;font-size:15.5px}
.steps{display:flex;gap:4px;margin:14px 0 4px}.steps div{flex:1;font-size:11px;text-align:center;color:var(--mute)}
.steps div:before{content:"";display:block;height:5px;border-radius:3px;background:var(--line);margin-bottom:5px}.steps .on{color:var(--pri);font-weight:600}.steps .on:before{background:var(--pri)}
.tag{display:inline-block;padding:2px 10px;border-radius:10px;font-size:12px;font-weight:600;white-space:nowrap}
.empty{text-align:center;color:var(--mute);padding:30px 10px}
.dot{width:10px;height:10px;border-radius:50%;background:currentColor;margin-top:8px;flex:none}
.inp{border:1px solid var(--line);background:var(--bg);border-radius:12px;padding:9px 12px;min-width:0}
.days{display:flex;gap:6px;flex-wrap:wrap;margin-top:8px}
.days button{padding:9px 13px;border-radius:12px;background:var(--gray);color:var(--mute);font-size:14px;font-weight:600}
.days button.on{background:var(--grn-s);color:var(--grn);box-shadow:inset 0 0 0 1.5px var(--grn)}.days button.n{background:var(--red-s);color:var(--red)}
.avr{display:grid;grid-template-columns:78px 1fr 1fr;gap:8px;align-items:center;margin-top:8px}.avr b{font-size:14px}.avr button{padding:11px 6px;border-radius:12px;background:var(--gray);color:var(--mute);font-weight:600;font-size:14px}
.avr button.g.on{background:var(--grn-s);color:var(--grn);box-shadow:inset 0 0 0 1.5px var(--grn)}.avr button.r.on{background:var(--red-s);color:var(--red);box-shadow:inset 0 0 0 1.5px var(--red)}.days button.off.on{background:var(--red-s);color:var(--red);box-shadow:inset 0 0 0 1.5px var(--red)}
.days button[disabled]{opacity:.4}
.pg{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:12px}
.pcard{background:var(--card);border:1px solid var(--line);border-radius:22px;padding:18px 10px;display:flex;flex-direction:column;align-items:center;gap:6px;font-weight:600}
.mask{position:fixed;inset:0;background:rgba(10,20,12,.45);display:none;align-items:flex-end;justify-content:center;z-index:20}.mask.show{display:flex}
.sheet{background:var(--card);width:100%;max-width:520px;border-radius:26px 26px 0 0;padding:20px 18px calc(22px + env(safe-area-inset-bottom,0px));max-height:85vh;overflow:auto;animation:up .25s ease-out}
@keyframes up{from{transform:translateY(40px);opacity:.4}}
@media(prefers-reduced-motion:reduce){.sheet{animation:none}}
.sheet h2{margin:0 0 2px;font-size:18px}.cand{border:1px solid var(--line);border-radius:16px;padding:12px;margin-top:10px}.cand .row{display:flex;align-items:center;gap:10px}
#bar{position:fixed;left:12px;right:12px;bottom:calc(12px + env(safe-area-inset-bottom,0px));max-width:560px;margin:0 auto;background:var(--ink);color:var(--bg);border-radius:18px;padding:10px 12px 10px 16px;display:none;align-items:center;gap:10px;z-index:15;font-size:14px}
#bar.show{display:flex}#bar span{flex:1}#bar .btn{background:var(--bg);color:var(--ink)}#bar .btn.ghost{background:transparent;color:var(--bg);border-color:rgba(128,128,128,.5)}
.toast{position:fixed;left:50%;bottom:calc(84px + env(safe-area-inset-bottom,0px));transform:translateX(-50%) translateY(20px);background:var(--pri);color:var(--bg);padding:10px 18px;border-radius:14px;font-size:14px;opacity:0;pointer-events:none;transition:.25s;z-index:30;max-width:90%}.toast.show{opacity:1;transform:translateX(-50%)}
</style>
</head>
<body>
<div class="wrap">
  <header><div class="lg" id="lg"><img class="logo" alt="Aegean" src="data:image/jpeg;base64,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"></div><div class="hd"><div class="brand">Aegean</div><h1 id="title"></h1><div class="sub" id="sub"></div><div class="sub" id="clock" aria-live="off"></div></div><div class="circs" id="circs"></div></header>
  <nav class="tabs" id="tabs"></nav>
  <main id="main"></main>
</div>
<div class="mask" id="mask"><div class="sheet" id="sheet"></div></div>
<div class="toast" id="toast"></div>
<script>
const DAYS=['จ.','อ.','พ.','พฤ.','ศ.','ส.','อา.'],DATES=[23,24,25,26,27,28,29];
const FULL=['วันจันทร์','วันอังคาร','วันพุธ','วันพฤหัสบดี','วันศุกร์','วันเสาร์','วันอาทิตย์'];
const KEY='aegean-v4',SK='aegean-sub',CLOSED=[2],NW='30 พ.ย. – 6 ธ.ค.';
const DATES2=[30,1,2,3,4,5,6];
const STL={ok:'ครบ',bad:'ขาด',warn:'ขาด',closed:'หยุด'};
const cols=['#2B5A3A','#9A5B3E','#3E6E8C','#8A7A2B','#6B4E8C','#8C3E5E'];
const TITLE={me:'ของฉัน',home:'ภาพรวมวันนี้',roster:'ตารางพนักงาน',reqs:'คำขอสลับกะ',alerts:'แจ้งเตือน',staff:'จัดการพนักงาน'};
const TABS=[['roster','ตาราง'],['staff','พนักงาน']],TABS_S=[['me','ของฉัน'],...TABS];
const I={back:'<path d="M15 5l-7 7 7 7"/>',home:'<path d="M4 11l8-7 8 7v9H4z"/>',bell:'<path d="M6 17V11a6 6 0 0112 0v6l1.5 2h-15zM10 21h4"/>',trash:'<path d="M4 7h16M10 11v6M14 11v6M6 7l1 12a2 2 0 002 2h6a2 2 0 002-2l1-12M9 7V4h6v3"/>',x:'<path d="M6 6l12 12M18 6L6 18"/>',cam:'<path d="M4 8h3l1.5-2h7L17 8h3v11H4z"/><circle cx="12" cy="13" r="3.2"/>'};
const ic=k=>`<svg viewBox="0 0 24 24">${I[k]}</svg>`;
const SEED=()=>({need:[4,4,0,4,4,2,1],reqs:[],logs:[],E:[
 {id:0,n:'นิ่ม',av:[0,1,3,4,5],s:[0,1,3,4]},{id:1,n:'ต้น',av:[0,1,3,4,5],s:[0,1,3,4]},
 {id:2,n:'มิ้นท์',av:[0,1,3,4,5],s:[0,1,4]},{id:3,n:'เบนซ์',av:[0,1,3,4],s:[0,1,3,4]},
 {id:4,n:'ฟ้า',av:[0,3,4,5,6],s:[5]},{id:5,n:'โอ๊ต',av:[0,1,4,5],s:[0,1,4]}]});
const raw=k=>{try{const v=localStorage.getItem(k);return v?JSON.parse(v):null}catch(e){return null}};
const cl=s=>String(s==null?'':s).replace(/[<>&"'`]/g,''),cn=s=>cl(s).slice(0,30);
const dd=a=>Array.isArray(a)?[...new Set(a.map(Number).filter(d=>d>=0&&d<=6&&!CLOSED.includes(d)))].sort((x,y)=>x-y):[];
const tt=x=>Array.isArray(x)&&x.length===2&&x[0]>=0&&x[1]<=24&&x[0]<x[1]?[Number(x[0]),Number(x[1])]:[9,17];
const uid=()=>Math.random().toString(36).slice(2,9),tok=()=>(uid()+uid()).slice(0,10);
function sane(o){try{if(!o||!Array.isArray(o.E)||!Array.isArray(o.need)||o.need.length!==7)return null;
 const seen=new Set(),E=[];o.E.forEach(e=>{const id=Number(e&&e.id);if(!Number.isInteger(id)||seen.has(id))return;seen.add(id);const s=dd(e.s),t={};s.forEach(d=>t[d]=tt(e.t&&e.t[d]));E.push({id,n:cn(e.n)||'พนักงาน',av:dd(e.av),s,t,tk:(/^[a-z0-9]{6,12}$/.test(e.tk)?e.tk:tok()),tel:cl(e.tel).slice(0,20),fn:cl(e.fn).slice(0,60),addr:cl(e.addr).slice(0,200),...(typeof e.ph==='string'&&e.ph.startsWith('data:image/')?{ph:e.ph}:{})})});
 E.sort((a,b)=>a.id-b.id);
 const need=o.need.map((n,d)=>CLOSED.includes(d)?0:Math.max(0,Math.min(20,parseInt(n)||0)));
 const reqs=(Array.isArray(o.reqs)?o.reqs:[]).filter(r=>r&&seen.has(r.b)&&(r.k==='assign'||seen.has(r.a))&&Number.isInteger(r.d)&&['wait_b','wait_owner','done','no'].includes(r.st)).map(r=>({id:String(r.id||uid()),k:r.k==='assign'?'assign':'swap',a:r.k==='assign'?null:r.a,b:r.b,d:r.d,e:Number.isInteger(r.e)?r.e:null,t:tt(r.t),st:r.st,at:Number(r.at)||0}));
 const logs=(Array.isArray(o.logs)?o.logs:[]).slice(0,50).map(l=>({t:cl(l&&l.t)}));
 return{need,rate:(o.rate!=null&&Number.isFinite(Number(o.rate)))?Math.max(0,Math.min(9999,Math.round(Number(o.rate)))):40,E,reqs,logs}}catch(e){return null}}
const saneSub=o=>{const r={};if(o&&typeof o==='object')Object.keys(o).forEach(k=>{const s=o[k];if(s&&Array.isArray(s.av)&&Array.isArray(s.off))r[k]={av:dd(s.av),off:dd(s.off),at:Number(s.at)||0}});return r};
const route=()=>{const m=/^#s-(\d+)-([a-z0-9]+)$/.exec(location.hash);return m?{id:+m[1],tk:m[2]}:null},isStaff=()=>!!route();
function units(){return{core:JSON.stringify({need:S.need,rate:S.rate,logs:S.logs}),emp:Object.fromEntries(S.E.map(e=>[e.id,JSON.stringify(e)])),rq:Object.fromEntries(S.reqs.map(r=>[r.id,JSON.stringify(r)]))}}
let S=sane(raw(KEY)||raw('aegean-v3'))||sane(SEED()),U=units(),stack=[route()?'me':'roster'],edit=false,SUB=saneSub(raw(SK)),DB=null,PF=null,ready=false,preview=false,quiet=0,rbt=0,lastSave=0,sv=0;
const $=s=>document.querySelector(s),emp=i=>S.E.find(e=>e.id===i),rq=id=>S.reqs.find(r=>r.id===id),cur=()=>stack[stack.length-1];
const me=()=>{const r=route();if(!r)return null;const e=S.E.find(x=>x.id===r.id&&x.tk===r.tk);return e?e.id:null};
const OWN=()=>!isStaff(),can=id=>OWN()||id===me();
function pending(){const u=units(),w=[],x=[],o=OWN(),m=me();
 if(o&&u.core!==U.core)w.push(['app/core','core',u.core]);
 for(const k in u.emp)if((o||+k===m)&&u.emp[k]!==U.emp[k])w.push(['emp/'+k,'emp:'+k,u.emp[k]]);
 for(const k in u.rq)if(u.rq[k]!==U.rq[k])w.push(['rq/'+k,'rq:'+k,u.rq[k]]);
 if(o){for(const k in U.emp)if(!(k in u.emp))x.push('emp/'+k);for(const k in U.rq)if(!(k in u.rq))x.push('rq/'+k)}
 return{w,x}}
const dirty=()=>{const p=pending();return p.w.length>0||p.x.length>0};
const cov=d=>S.E.filter(e=>e.s.includes(d)).length;
const lvl=d=>CLOSED.includes(d)?'closed':cov(d)>=S.need[d]?'ok':cov(d)===0?'bad':'warn';
const lc=d=>{const l=lvl(d);return l==='warn'?'bad':l};
const col=e=>cols[e.id%6];
const avatar=(e,b)=>e.ph?`<img class="av${b?' big':''}" src="${e.ph}" alt="">`:`<span class="av${b?' big':''}">${e.n.slice(0,1)}</span>`;
const dl=a=>a.map(d=>DAYS[d]).join(' ')||'—';
const ft=x=>String(Math.floor(x)).padStart(2,'0')+':'+(x%1?'30':'00');
const sh=(e,d)=>(e.t&&e.t[d])||[9,17],hrs=e=>e.s.reduce((n,d)=>n+sh(e,d)[1]-sh(e,d)[0],0),thb=h=>Math.round(h*S.rate).toLocaleString('th-TH'),fh=h=>String(Math.round(h*10)/10),totH=()=>S.E.reduce((n,e)=>n+hrs(e),0);
const BASE='https://claude.ai/artifact/Bbx2WV8XLgqa82gvsvCLBB',lk=e=>BASE+'#s-'+e.id+'-'+e.tk;
const lmsg=e=>`สวัสดี ${e.n} กรุณากดลิงก์นี้เพื่อส่งวันว่าง ดูตารางงาน และตอบรับคำขอสลับกะของคุณ: ${lk(e)}`;
const pa=(d,id)=>S.reqs.some(r=>r.k==='assign'&&r.d===d&&r.b===id&&(r.st==='wait_b'||r.st==='wait_owner'));
const wp=d=>{const n=S.reqs.filter(r=>r.k==='assign'&&r.d===d&&(r.st==='wait_b'||r.st==='wait_owner')).map(r=>emp(r.b).n);return n.length?' · รอยืนยัน: '+n.join(', '):''};
function toast(m){const t=$('#toast');t.textContent=m;t.classList.add('show');clearTimeout(t._);t._=setTimeout(()=>t.classList.remove('show'),2300)}
function log(t){if(OWN())S.logs=[{t},...S.logs].slice(0,50)}
function go(v){if(v!==cur())stack.push(v);edit=false;render();scrollTo(0,0)}
function cands(a,d){return S.E.filter(b=>b.id!==a.id&&!b.s.includes(d)&&b.av.includes(d)).map(b=>({b,swaps:b.s.filter(x=>!a.s.includes(x)&&a.av.includes(x))}))}
function rosterH(){
  const o=OWN(),m=me();
  let h=`<div class="card"><div class="ch"><h2>${edit?'แก้ไขตาราง':'ตารางทั้งสัปดาห์'}</h2><div class="act" style="margin:0"><button class="circ" data-a="snap" aria-label="บันทึกภาพตารางงาน">${ic('cam')}</button><button class="btn ${edit?'':'ghost'}" data-a="edit">${edit?'เสร็จสิ้น':o?'แก้ไขตาราง':'เลือกกะของฉัน'}</button></div></div>
  <p class="hint">${edit?(o?'แตะช่องว่างเพื่อเพิ่มกะ แตะกะเพื่อเลือกเวลาหรือลบ ปรับจำนวนคนที่ต้องการด้วย − / + ระบบบันทึกให้อัตโนมัติ':'แก้ไขได้เฉพาะแถวของคุณ แตะช่องว่างเพื่อเพิ่มกะ แตะกะเพื่อเลือกเวลาหรือลบ'):(o?'กด "แก้ไขตาราง" เพื่อเพิ่มหรือปรับกะ':'กด "เลือกกะของฉัน" เพื่อลงกะของคุณ')}</p><div class="scroll"><div class="grid"><div></div>`;
  for(let d=0;d<7;d++){const x=CLOSED.includes(d);h+=`<div class="dh ${lc(d)}">${DAYS[d]} ${DATES[d]}<small>${x?'ร้านหยุด':cov(d)+'/'+S.need[d]+' คน'}</small>${edit&&!x&&o?`<div class="stp"><button data-need="${d}:-1" aria-label="ลดจำนวน">−</button><button data-need="${d}:1" aria-label="เพิ่มจำนวน">+</button></div>`:''}</div>`}
  S.E.forEach(e=>{
    const c=can(e.id);
    h+=`<div class="emp">${avatar(e)}<div><b>${e.n}${e.id===m?' (คุณ)':''}</b><small>${fh(hrs(e))} ชม. · ${thb(hrs(e))} บ.</small></div></div>`;
    for(let d=0;d<7;d++){
      if(CLOSED.includes(d)){h+='<div class="cell x"></div>';continue}
      let inner='';
      if(e.s.includes(d)){const[a,b]=sh(e,d),body=`<b>${ft(a)}–${ft(b)}</b><span>${fh(b-a)} ชม. · ${thb(b-a)} บ.</span>`;inner=c&&edit?`<button class="shift" data-tg="${e.id}:${d}">${body}</button>`:`<div class="shift">${body}</div>`}
      else if(edit&&c)inner=`<button class="add" data-tg="${e.id}:${d}" aria-label="เพิ่มกะ">+</button>`;
      h+=`<div class="cell">${inner}</div>`;
    }
  });
  return h+`</div></div></div>`;
}
function staffH(){
  const o=OWN();
  let h=`<div class="ch"><span class="hint" style="margin:0">${o?'กดแก้ไขข้อมูลส่วนตัวเพื่อใส่ชื่อ รูป และเบอร์ติดต่อ':'ดูข้อมูลทุกคนได้ แก้ไขได้เฉพาะข้อมูลของคุณ'}</span>${o?'<button class="btn" data-a="addemp">+ เพิ่ม</button>':''}</div>`;
  S.E.forEach(e=>{
    const s=SUB[e.id],c=can(e.id);
    h+=`<div class="card" style="padding:14px"><div class="act" style="margin:0;flex-wrap:nowrap">${avatar(e,1)}<div style="flex:1;min-width:0"><b>${e.n}${e.fn?' · '+e.fn:''}</b><div class="sub">ตำแหน่ง: พนักงาน${e.tel?' · โทร '+e.tel:''}</div>${e.addr?`<div class="sub">${e.addr}</div>`:''}${c?`<div class="act"><button class="btn ghost" data-prof="${e.id}">แก้ไขข้อมูลส่วนตัว</button></div>`:''}</div>
    ${o?`<button class="circ" data-del="${e.id}" aria-label="ลบพนักงาน">${ic('trash')}</button>`:''}</div>
    <div class="sub" style="margin-top:10px">วันที่ว่าง</div><div class="days">${DAYS.map((x,d)=>`<button class="${e.av.includes(d)?'on':CLOSED.includes(d)?'':'n'}" ${CLOSED.includes(d)||!c?'disabled':''} data-av="${e.id}:${d}">${x}</button>`).join('')}</div>
    <div class="act" style="margin-top:12px"><span class="sub" style="flex:1">${s?`ส่งแล้ว · ว่าง ${dl(s.av)} · ขอหยุด ${dl(s.off)}`:'ยังไม่ส่งวันว่างสัปดาห์หน้า'}</span>${s&&o?`<button class="btn ghost" data-use="${e.id}">ใช้ข้อมูลนี้</button>`:''}</div></div>`;
  });
  return h;
}
function meH(){
  const m=me(),e=emp(m);if(!PF||PF.me!==m){const s=SUB[m];PF={me:m,av:s?[...s.av]:[0,1,3,4,5,6],off:s?[...s.off]:[]}}
  const rows=()=>DAYS.map((x,d)=>CLOSED.includes(d)?`<div class="avr"><b>${x} ${DATES2[d]}</b><span class="sub" style="grid-column:span 2">ร้านหยุด</span></div>`:`<div class="avr"><b>${x} ${DATES2[d]}</b><button class="g ${PF.av.includes(d)?'on':''}" data-pa="${d}">ว่าง</button><button class="r ${PF.off.includes(d)?'on':''}" data-po="${d}">ไม่ว่าง</button></div>`).join('');
  const mine=e.s.length?e.s.map(d=>{const[a,b]=sh(e,d);return`<div class="drow" style="grid-template-columns:64px 1fr auto"><b>${DAYS[d]} ${DATES[d]}</b><span>${ft(a)}–${ft(b)}</span><span class="sub">${fh(b-a)} ชม. · ${thb(b-a)} บาท</span></div>`}).join('')+`<p style="margin:10px 0 0;font-weight:600">รวม ${fh(hrs(e))} ชั่วโมง · ${thb(hrs(e))} บาท</p>`:'<div class="empty" style="padding:14px">ยังไม่มีกะในสัปดาห์นี้</div>';
  const prof=`<div class="card"><div class="act" style="margin:0;flex-wrap:nowrap">${avatar(e,1)}<div style="flex:1;min-width:0"><b>${e.n}${e.fn?' · '+e.fn:''}</b><div class="sub">${e.tel?'โทร '+e.tel:'ยังไม่ได้กรอกเบอร์โทร'}</div>${e.addr?`<div class="sub">${e.addr}</div>`:''}<div class="act"><button class="btn ghost" data-prof="${m}">แก้ไขข้อมูลส่วนตัว</button></div></div></div></div>`;
  return prof+`<div class="card"><div class="ch"><h2>ตารางงานของฉัน</h2><button class="link" data-go="roster">เลือกกะ →</button></div>${mine}</div>
  <div class="card"><div class="ch" style="margin:0"><h2>การส่งข้อมูลวันที่ว่างทำงาน</h2></div><p class="hint" style="margin:2px 0 0">สัปดาห์ ${NW} · ร้านหยุดทุกวันพุธ</p><p class="hint" style="margin:10px 0 0">แตะ "ว่าง" (เขียว) หรือ "ไม่ว่าง" (แดง) ของแต่ละวัน</p>${rows()}
  <div class="act" style="margin-top:12px"><span class="tag ok">ว่าง ${PF.av.length} วัน</span><span class="tag bad">ไม่ว่าง ${PF.off.length} วัน</span></div>
  <div class="act" style="margin-top:20px"><button class="btn" style="flex:1;padding:13px" data-psend="1">${SUB[m]?'ส่งข้อมูลอีกครั้ง':'ส่งข้อมูล'}</button></div>${SUB[m]?'<p class="hint" style="margin:10px 0 0">ส่งข้อมูลแล้ว เจ้าของร้านจะเห็นในระบบ</p>':''}</div>`;
}
let rt=0;function softRender(){const a=document.activeElement;if(a&&(a.tagName==='INPUT'||a.tagName==='TEXTAREA')&&a.type!=='file'){clearTimeout(rt);rt=setTimeout(softRender,800);return}render()}
function render(){try{draw()}catch(e){$('#main').innerHTML='<div class="card empty">เกิดข้อผิดพลาดในการแสดงผล<br>กรุณารีเฟรชหน้าอีกครั้ง</div>'}}
function draw(){
  const st=isStaff(),m=me(),hk=st?'me':'roster',exit=preview?`<button class="circ" data-a="exit" aria-label="กลับหน้าเจ้าของร้าน">${ic('x')}</button>`:'';
  if(st&&m==null){
    $('#title').textContent=ready?'ลิงก์ไม่ถูกต้อง':'กำลังโหลด…';$('#sub').textContent='พอร์ทัลพนักงาน';$('#circs').innerHTML=exit;$('#tabs').style.display='none';
    $('#main').innerHTML=`<div class="card empty">${ready?'ลิงก์นี้ไม่ถูกต้องหรือถูกยกเลิกแล้ว<br>กรุณาขอลิงก์ใหม่จากเจ้าของร้าน':'กำลังโหลดข้อมูล…'}</div>`;return}
  $('#tabs').style.display='';
  let v=cur();const V={me:meH,roster:rosterH,staff:staffH};if(!V[v]||(v==='me'&&!st))v=hk;
  $('#title').textContent=v==='me'?'สวัสดี '+emp(m).n:v==='staff'&&st?'พนักงาน':TITLE[v];$('#sub').textContent=(st?'พอร์ทัลพนักงาน · ':'')+'สัปดาห์ 23 – 29 พ.ย. 2569 · ร้านหยุดทุกวันพุธ';
  $('#circs').innerHTML=(v===hk?'':`<button class="circ" data-a="back" aria-label="ย้อนกลับ">${ic('back')}</button><button class="circ" data-a="home" aria-label="หน้าหลัก">${ic('home')}</button>`)+exit;
  $('#tabs').innerHTML=(st?TABS_S:TABS).map(([k,l])=>`<button class="tab ${k===v?'on':''}" data-go="${k}">${l}</button>`).join('');
  $('#main').innerHTML=V[v]();
  queueSave();
}
function openSheet(eid,d){
  const a=emp(eid),cs=cands(a,d);
  let h=`<h2>ขอสลับกะ${FULL[d]}</h2><p class="sub">${a.n} · ${ft(sh(a,d)[0])}–${ft(sh(a,d)[1])}<br>แสดงเฉพาะคนที่ว่างในวันนั้น</p>`;
  if(!cs.length)h+=`<div class="empty">ยังไม่มีพนักงานที่แทนได้</div>`;
  cs.forEach(c=>{h+=`<div class="cand"><div class="row">${avatar(c.b)}<div><b>${c.b.n}</b><div class="sub">ว่าง${FULL[d]} · ${fh(hrs(c.b))} ชม./สัปดาห์</div></div></div><div class="act"><button class="btn" data-send="${eid}:${c.b.id}:${d}">ขอให้รับกะแทน</button>${c.swaps.map(x=>`<button class="btn ghost" data-send="${eid}:${c.b.id}:${d}:${x}">แลกกับ${FULL[x]}</button>`).join('')}</div></div>`});
  $('#sheet').innerHTML=h+`<button class="btn ghost" style="width:100%;margin-top:16px" data-a="close">ปิด</button>`;$('#mask').classList.add('show');
}
function mv(f,t,d){const x=sh(f,d);f.s=f.s.filter(y=>y!==d);if(f.t)delete f.t[d];if(!t.s.includes(d))t.s.push(d);t.t=t.t||{};t.t[d]=x;t.s.sort((p,q)=>p-q)}
function apply(r){
  const b=emp(r.b);
  if(r.k==='assign'){if(!b.s.includes(r.d)){b.s.push(r.d);b.s.sort((p,q)=>p-q);b.t=b.t||{};b.t[r.d]=r.t||[9,17]}log(`มอบหมาย ${b.n} ลงกะ${FULL[r.d]}`);return}
  const a=emp(r.a);mv(a,b,r.d);if(r.e!=null)mv(b,a,r.e);
  log(r.e==null?`${a.n} ส่งกะ${FULL[r.d]} ให้ ${b.n}`:`${a.n} แลกกะกับ ${b.n} (${FULL[r.d]} ↔ ${FULL[r.e]})`);
}
function rdesc(r){const a=r.a==null?null:emp(r.a),b=emp(r.b);
 if(r.k==='assign'){const h=r.t[1]-r.t[0];return`มอบหมาย ${b.n} ลงกะ${FULL[r.d]} ${ft(r.t[0])}–${ft(r.t[1])} (${fh(h)} ชม. · ${thb(h)} บาท)`}
 return r.e==null?`${a.n} ให้ ${b.n} รับ${FULL[r.d]}`:`${a.n} แลกกะกับ ${b.n}: ${FULL[r.d]} ↔ ${FULL[r.e]}`}
function rateH(){const sum=`<p style="margin:0">รวมสัปดาห์นี้ <b>${fh(totH())} ชั่วโมง</b> · <b>${thb(totH())} บาท</b></p>`;
 if(!OWN())return`<div class="card"><div class="ch"><h2>ค่าจ้างต่อชั่วโมง</h2><b>${S.rate} บาท</b></div>${sum}</div>`;
 return`<div class="card"><div class="ch"><h2>ค่าจ้างต่อชั่วโมง</h2><div class="act" style="margin:0"><button class="circ" style="width:36px;height:36px" data-rate="-5" aria-label="ลดอัตราจ้าง">−</button><input class="inp" type="number" min="0" inputmode="numeric" style="width:84px;text-align:center" value="${S.rate}" data-ratein="1" aria-label="อัตราจ้างต่อชั่วโมง"><button class="circ" style="width:36px;height:36px" data-rate="5" aria-label="เพิ่มอัตราจ้าง">+</button><span class="sub">บาท</span></div></div>${sum}</div>`}
let TS=null;const TO=[...Array(49)].map((_,i)=>i/2);
function tsum(){const h=TS.en-TS.st,el=$('#tsum');if(el)el.textContent=h>0?`รวม ${fh(h)} ชั่วโมง · ${thb(h)} บาท`:'เวลาเลิกงานต้องมากกว่าเวลาเริ่ม';const b=$('#tsave');if(b)b.disabled=!(h>0)}
function openTime(e,d){const p=emp(e),has=p.s.includes(d),[st,en]=has?sh(p,d):[9,17];TS={e,d,st,en};
 const op=v=>TO.map(x=>`<option value="${x}"${x===v?' selected':''}>${ft(x)}</option>`).join('');
 $('#sheet').innerHTML=`<h2>${has?'แก้ไขกะ':'เพิ่มกะ'}${FULL[d]}</h2><p class="sub">${p.n} · อัตราจ้าง ${S.rate} บาท/ชั่วโมง</p><div class="act" style="margin-top:14px"><label class="sub">เริ่ม<br><select class="inp" data-ts="st">${op(st)}</select></label><label class="sub">เลิก<br><select class="inp" data-ts="en">${op(en)}</select></label></div><p id="tsum" style="font-weight:600;margin:14px 0 0"></p><div class="act" style="margin-top:16px"><button class="btn" id="tsave" data-tsave="1" style="flex:1">บันทึกกะ</button>${has?'<button class="btn ghost" data-tdel="1">ลบกะ</button>':''}<button class="btn ghost" data-a="close">ปิด</button></div>`;$('#mask').classList.add('show');tsum()}
function openProfile(id){const p=emp(id);if(!p)return;
 const f=(l,k,v,x)=>`<div class="sub" style="margin-top:10px">${l}</div>${k==='addr'?`<textarea class="inp" rows="3" style="width:100%;resize:vertical" data-addr="${id}" aria-label="${l}">${v}</textarea>`:`<input class="inp" style="width:100%" ${x||''} value="${v}" data-${k}="${id}" aria-label="${l}">`}`;
 $('#sheet').innerHTML=`<h2>แก้ไขข้อมูลส่วนตัว</h2><div class="act" style="flex-wrap:nowrap;margin-top:12px"><label style="cursor:pointer"><input type="file" accept="image/*" data-ph="${id}" hidden><span id="pv">${avatar(p,1)}</span></label><div class="sub">แตะรูปเพื่ออัปโหลดภาพของคุณ</div></div>${f('ชื่อจริง','fn',p.fn||'')}${f('ชื่อเล่น','name',p.n)}${f('เบอร์โทรศัพท์','tel',p.tel||'','inputmode="tel"')}${f('ที่อยู่ปัจจุบัน','addr',p.addr||'')}<button class="btn" style="width:100%;margin-top:18px" data-a="close">เสร็จสิ้น</button>`;$('#mask').classList.add('show')}
function snap(){const L=f=>document.fonts?document.fonts.load(f,'ก').catch(()=>{}):Promise.resolve();Promise.all([L('400 16px "Noto Sans Thai"'),L('600 16px "Noto Sans Thai"'),L('700 16px "Noto Sans Thai"')]).then(snapDraw)}
function snapDraw(){
 const E=S.E,P=24,NC=180,DC=128,W=P*2+NC+DC*7,HH=92,RH=66,TOP=P+86,H=TOP+HH+E.length*RH+P;
 const c=document.createElement('canvas'),sc=2;c.width=W*sc;c.height=H*sc;const g=c.getContext('2d');g.scale(sc,sc);
 const F='"Noto Sans Thai",system-ui,sans-serif',rr=(x,y,w,h,r,f)=>{g.beginPath();g.moveTo(x+r,y);g.arcTo(x+w,y,x+w,y+h,r);g.arcTo(x+w,y+h,x,y+h,r);g.arcTo(x,y+h,x,y,r);g.arcTo(x,y,x+w,y,r);g.closePath();g.fillStyle=f;g.fill()};
 const tx=(t,x,y,sz,wt,col,al,mw)=>{g.font=wt+' '+sz+'px '+F;g.fillStyle=col;g.textAlign=al||'left';g.textBaseline='middle';if(mw)g.fillText(t,x,y,mw);else g.fillText(t,x,y)};
 g.fillStyle='#fff';g.fillRect(0,0,W,H);
 tx('Aegean · ตารางงาน',P,P+26,30,700,'#1D2A1F');
 tx('สัปดาห์ 23 – 29 พ.ย. 2569 · ร้านหยุดทุกวันพุธ',P,P+62,18,400,'#737D74');
 for(let d=0;d<7;d++){const x=P+NC+d*DC+4,l=lvl(d),k=l==='ok'?['#DFF3E9','#23885A']:l==='closed'?['#EDEFEB','#737D74']:['#FBE7EA','#C8445A'];
  rr(x,TOP,DC-8,HH-10,14,k[0]);tx(DAYS[d]+' '+DATES[d],x+(DC-8)/2,TOP+28,20,700,k[1],'center');tx(l==='closed'?'ร้านหยุด':cov(d)+'/'+S.need[d]+' คน',x+(DC-8)/2,TOP+56,16,600,k[1],'center')}
 E.forEach((e,i)=>{const y=TOP+HH+i*RH;
  if(i%2===0)rr(P,y,W-P*2,RH-6,12,'#F7F8F6');
  tx(e.n,P+12,y+22,20,700,'#1D2A1F','left',NC-20);tx(fh(hrs(e))+' ชม.',P+12,y+46,14,400,'#737D74','left',NC-20);
  for(let d=0;d<7;d++){const x=P+NC+d*DC+4;
   if(CLOSED.includes(d)){rr(x,y+2,DC-8,RH-10,10,'#EDEFEB');continue}
   if(e.s.includes(d)){const[a,b]=sh(e,d);rr(x,y+2,DC-8,RH-10,10,'#E3EFE6');rr(x,y+2,5,RH-10,2,'#2B5A3A');tx(ft(a)+'–'+ft(b),x+16,y+22,16,700,'#1D2A1F','left',DC-28);tx(fh(b-a)+' ชม.',x+16,y+42,13,400,'#737D74')}
   else rr(x,y+2,DC-8,RH-10,10,'#F4F5F2')}});
 const url=c.toDataURL('image/png');
 $('#sheet').innerHTML='<h2>ภาพตารางงาน</h2><p class="sub">กดบันทึกรูป หรือกดค้างที่รูปเพื่อบันทึก</p><img src="'+url+'" alt="ตารางงาน" style="width:100%;border-radius:12px;border:1px solid var(--line);margin-top:10px"><div class="act" style="margin-top:14px"><a class="btn" style="flex:1;text-align:center" download="aegean-schedule.png" href="'+url+'">บันทึกรูป</a><button class="btn ghost" data-a="close">ปิด</button></div>';
 $('#mask').classList.add('show')}
function readPhoto(f,id){const r=new FileReader();r.onload=()=>{const im=new Image();im.onload=()=>{const c=document.createElement('canvas');c.width=c.height=96;const s=Math.min(im.width,im.height);c.getContext('2d').drawImage(im,(im.width-s)/2,(im.height-s)/2,s,s,0,0,96,96);emp(id).ph=c.toDataURL('image/jpeg',.8);const pv=$('#pv');if(pv)pv.innerHTML=avatar(emp(id),1);render()};im.src=r.result};r.readAsDataURL(f)}
const tgl=(a,d)=>a.includes(d)?a.filter(x=>x!==d):[...a,d].sort((x,y)=>x-y);
const OO=['del','del2','need','rate','fill','use'];
document.addEventListener('click',ev=>{
  const t=ev.target.closest('button,.mask');if(!t)return;const D=t.dataset,A=D.a;
  if(t.id==='mask'&&ev.target===t)return $('#mask').classList.remove('show');
  if(!OWN()&&(A==='addemp'||OO.some(k=>D[k]!==undefined)))return;
  if(D.go)return go(D.go);
  if(D.prof){const id=+D.prof;if(!can(id))return;return openProfile(id)}
  if(A==='exit'){preview=false;location.hash='';return}
  if(D.pa!==undefined&&PF){const d=+D.pa;PF.av=tgl(PF.av,d);PF.off=PF.off.filter(x=>x!==d);return render()}
  if(D.po!==undefined&&PF){const d=+D.po;PF.off=tgl(PF.off,d);PF.av=PF.av.filter(x=>x!==d);return render()}
  if(D.psend&&PF){const m=me();if(m==null)return;const rec={av:PF.av,off:PF.off,at:Date.now()};SUB[m]=rec;try{localStorage.setItem(SK,JSON.stringify(SUB))}catch(e){}if(DB)DB.collection('avail').doc(String(m)).set(rec).catch(()=>toast('ส่งไม่สำเร็จ ลองอีกครั้ง'));render();return toast('ส่งข้อมูลเรียบร้อยแล้ว')}
  if(A==='back'){if(stack.length>1)stack.pop();edit=false;return render()}
  if(A==='home'){stack=[isStaff()?'me':'roster'];edit=false;return render()}
  if(A==='close'){$('#mask').classList.remove('show');return render()}
  if(A==='edit'){edit=!edit;return render()}
  if(A==='snap')return snap();
  if(A==='addemp'){S.E.push({id:Math.max(-1,...S.E.map(e=>e.id))+1,n:'พนักงานใหม่',av:[0,1,3,4],s:[],t:{},tk:tok()});return render()}
  if(D.tg){const[e,d]=D.tg.split(':').map(Number);if(!can(e))return;return openTime(e,d)}
  if(D.tsave){const p=emp(TS.e);if(!p||!can(p.id))return;if(!p.s.includes(TS.d)){p.s.push(TS.d);p.s.sort((x,y)=>x-y);if(!p.av.includes(TS.d))toast(p.n+' ไม่ได้ลงวันว่างวันนี้ไว้')}p.t=p.t||{};p.t[TS.d]=[TS.st,TS.en];$('#mask').classList.remove('show');return render()}
  if(D.tdel){const p=emp(TS.e);if(!p||!can(p.id))return;p.s=p.s.filter(x=>x!==TS.d);if(p.t)delete p.t[TS.d];$('#mask').classList.remove('show');return render()}
  if(D.rate){S.rate=Math.max(0,Math.min(9999,S.rate+Number(D.rate)));return render()}
  if(D.need){const[d,k]=D.need.split(':').map(Number);S.need[d]=Math.max(0,S.need[d]+k);return render()}
  if(D.av){const[e,d]=D.av.split(':').map(Number),p=emp(e);if(!p||!can(e))return;p.av=tgl(p.av,d);return render()}
  if(D.use){const p=emp(+D.use),s=SUB[p.id];p.av=s.av.filter(d=>!s.off.includes(d));render();return toast('ใช้วันว่างของ '+p.n+' แล้ว')}
  if(D.del){const p=emp(+D.del);if(!p)return;$('#sheet').innerHTML=`<h2>ลบ ${p.n}?</h2><p class="sub">กะและคำขอสลับกะของคนนี้จะถูกลบด้วย</p><div class="act" style="margin-top:16px"><button class="btn" style="flex:1" data-del2="${p.id}">ลบ</button><button class="btn ghost" style="flex:1" data-a="close">ยกเลิก</button></div>`;$('#mask').classList.add('show');return}
  if(D.del2){const id=+D.del2;S.E=S.E.filter(e=>e.id!==id);S.reqs=S.reqs.filter(r=>r.a!==id&&r.b!==id);$('#mask').classList.remove('show');return render()}
});
document.addEventListener('input',ev=>{const t=ev.target;if(t.dataset.ratein!==undefined&&OWN()){const v=Number(t.value);S.rate=Number.isFinite(v)?Math.max(0,Math.min(9999,Math.round(v))):0;queueSave();return}const K={tel:20,fn:60,addr:200};for(const k in K)if(t.dataset[k]!==undefined){const p=emp(+t.dataset[k]);if(p&&can(p.id))p[k]=cl(t.value).slice(0,K[k]);queueSave();return}if(t.dataset.name!==undefined){const p=emp(+t.dataset.name);if(p&&can(p.id))p.n=cn(t.value);queueSave()}});
document.addEventListener('change',ev=>{const t=ev.target;if(t.dataset.ts&&TS){TS[t.dataset.ts]=Number(t.value);tsum();return}if(t.dataset.ratein!==undefined)return render();if(t.dataset.ph!==undefined&&t.files[0]&&can(+t.dataset.ph))readPhoto(t.files[0],+t.dataset.ph);if(t.dataset.name!==undefined){const p=emp(+t.dataset.name);if(p&&can(p.id)&&!p.n.trim())p.n='พนักงาน';render()}});
addEventListener('hashchange',()=>{stack=[isStaff()?'me':'roster'];edit=false;PF=null;if(!isStaff())preview=false;render()});
const got={},DBU={core:null,emp:{},rq:{}};
function rdy(){ready=true;if(!DB&&OWN())U={core:null,emp:{},rq:{}};render()}
function rebuild(){
  if(!(got.c&&got.e&&got.r))return;
  const p=pending();if(p.w.length||p.x.length||Date.now()<quiet){clearTimeout(rbt);rbt=setTimeout(rebuild,600);return}
  const ks=Object.keys(DBU.emp);
  if(!DBU.core&&!ks.length){ready=true;if(OWN())U={core:null,emp:{},rq:{}};softRender();return}
  let core={};try{core=JSON.parse(DBU.core||'{}')}catch(e){}
  const E=[],R=[],pj=j=>{try{return JSON.parse(j)}catch(e){return null}};
  ks.forEach(k=>{const x=pj(DBU.emp[k]);if(x)E.push(x)});Object.keys(DBU.rq).forEach(k=>{const x=pj(DBU.rq[k]);if(x)R.push(x)});
  R.sort((a,b)=>(b.at||0)-(a.at||0));
  const n=sane({need:core.need||SEED().need,rate:core.rate,logs:core.logs,E,reqs:R});
  if(n){S=n;U={core:DBU.core,emp:{...DBU.emp},rq:{...DBU.rq}}}
  ready=true;softRender();
}
(async()=>{try{if(!window.claude){rdy();return}DB=await claude.use('db');if(!DB){rdy();return}
 const dj=d=>{const x=d.data();return x&&typeof x.json==='string'?x.json:null};
 DB.doc('app/core').onSnapshot(s=>{DBU.core=s.exists?dj(s):null;got.c=1;rebuild()},()=>{got.c=1;rebuild()});
 DB.collection('emp').onSnapshot(q=>{DBU.emp={};q.docs.forEach(d=>{const j=dj(d);if(j)DBU.emp[d.id]=j});got.e=1;rebuild()},()=>{got.e=1;rebuild()});
 DB.collection('rq').onSnapshot(q=>{DBU.rq={};q.docs.forEach(d=>{const j=dj(d);if(j)DBU.rq[d.id]=j});got.r=1;rebuild()},()=>{got.r=1;rebuild()});
 DB.collection('avail').onSnapshot(q=>{const o={};q.docs.forEach(d=>o[d.id]=d.data());SUB=saneSub(o);try{localStorage.setItem(SK,JSON.stringify(SUB))}catch(e){}softRender()},()=>{});
}catch(e){rdy()}})();
function queueSave(){clearTimeout(sv);if(!dirty())return;sv=setTimeout(commit,600)}
function commit(){const p=pending();if(!p.w.length&&!p.x.length)return;
 p.w.forEach(([path,key,val])=>{if(key==='core')U.core=val;else{const[t,k]=key.split(':');U[t][k]=val}});
 p.x.forEach(path=>{const[t,k]=path.split('/');delete U[t][k]});
 if(OWN())try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}
 lastSave=Date.now();quiet=Date.now()+1200;
 if(DB){const f=()=>toast('บันทึกในเครื่องแล้ว แต่ยังซิงก์ไม่สำเร็จ');p.w.forEach(([path,key,val])=>DB.doc(path).set({json:val}).catch(f));p.x.forEach(path=>DB.doc(path).delete().catch(f))}
 tick()}
const tf=t=>new Date(t).toLocaleTimeString('th-TH',{hour12:false});
function tick(){const c=$('#clock');if(!c)return;const d=new Date();c.textContent=d.toLocaleDateString('th-TH',{weekday:'long',day:'numeric',month:'long',year:'numeric'})+' · '+tf(d)+(dirty()?' · กำลังบันทึก…':lastSave?' · บันทึกอัตโนมัติ '+tf(lastSave):' · บันทึกอัตโนมัติ')}
setInterval(tick,1000);
$('#lg').addEventListener('click',()=>{const l=$('#lg');l.classList.add('fast');clearTimeout(l._);l._=setTimeout(()=>l.classList.remove('fast'),1400)});
addEventListener('pagehide',commit);document.addEventListener('visibilitychange',()=>{if(document.hidden)commit()});
setTimeout(()=>{if(!ready)rdy()},8000);render();tick();
</script>
</body>
</html>
