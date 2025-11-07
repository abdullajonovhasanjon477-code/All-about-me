<!doctype html>
<html lang="uz">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Aloqa — Furqatli Bro</title>
<style>
  :root{
    --bg:#0f1724; --card:#0b1220; --accent:#06b6d4; --muted:#9aa6b2;
  }
  *{box-sizing:border-box;font-family:Inter,system-ui,Segoe UI,Roboto,"Helvetica Neue",Arial}
  body{margin:0; min-height:100vh; display:flex; align-items:center; justify-content:center; background:
    linear-gradient(180deg,#071026 0%, #081826 100%); color:#e6eef3;}
  .card{width:320px; max-width:92vw; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.06));
    border-radius:14px; padding:20px; box-shadow:0 10px 30px rgba(2,6,23,0.6); text-align:center}
  h1{font-size:18px; margin:0 0 12px; color:var(--accent)}
  p.sub{margin:0 0 16px; color:var(--muted); font-size:13px}
  .list{display:flex; flex-direction:column; gap:12px; align-items:center}
  .item{width:100%; display:flex; align-items:center; gap:12px; background:rgba(255,255,255,0.02);
    padding:10px 12px; border-radius:10px; cursor:pointer; transition:transform .12s, background .12s;
    border:1px solid rgba(255,255,255,0.03)}
  .item:active{transform:scale(.995)}
  .icon{width:44px; height:44px; display:grid; place-items:center; border-radius:8px; background:rgba(255,255,255,0.03)}
  .label{flex:1; text-align:left}
  .name{font-weight:600; font-size:15px}
  .hint{font-size:12px; color:var(--muted)}
  .detail{margin-top:8px; font-size:14px; color:#dbeef7; display:flex; gap:8px; align-items:center; justify-content:space-between}
  .btn{padding:8px 10px; border-radius:8px; border:0; background:var(--accent); color:#042024; font-weight:600; cursor:pointer}
  .small{font-size:12px; padding:6px 8px; border-radius:8px; background:rgba(255,255,255,0.04); color:var(--muted)}
  .hidden{display:none}
  .footer{margin-top:14px; font-size:12px; color:var(--muted)}
  @media (max-width:360px){ .card{padding:16px} .icon{width:40px;height:40px} }
</style>
</head>
<body>
  <div class="card" role="main">
    <h1>Furqatli Bro Aloqa</h1>
    <p class="sub">Pastdagi logolarga bosing — profil yoki raqam chiqadi</p>

    <div class="list">
      <!-- Instagram -->
      <div class="item" data-type="instagram" tabindex="0" aria-pressed="false">
        <div class="icon" aria-hidden="true">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none">
            <rect x="3" y="3" width="18" height="18" rx="5" stroke="currentColor" stroke-width="1.2"/>
            <circle cx="12" cy="12" r="3.2" stroke="currentColor" stroke-width="1.2" />
            <circle cx="17.5" cy="6.5" r="0.7" fill="currentColor"/>
          </svg>
        </div>
        <div class="label">
          <div class="name">Instagram</div>
          <div class="hint">@furqatli_bro</div>
          <div class="detail hidden">
            <div id="ig-text">@furqatli_bro</div>
            <div>
              <button class="small" onclick="openIG(event)">Ochil</button>
              <button class="small" onclick="copyText(event,'@furqatli_bro')">Nusxa</button>
            </div>
          </div>
        </div>
      </div>

      <!-- Telegram -->
      <div class="item" data-type="telegram" tabindex="0" aria-pressed="false">
        <div class="icon" aria-hidden="true">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none">
            <path d="M4 12l16-6-4 15-3.5-4.2L11 17l-2-2" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="label">
          <div class="name">Telegram</div>
          <div class="hint">@furqatli_bro</div>
          <div class="detail hidden">
            <div id="tg-text">@furqatli_bro</div>
            <div>
              <button class="small" onclick="openTG(event)">Ochil</button>
              <button class="small" onclick="copyText(event,'@furqatli_bro')">Nusxa</button>
            </div>
          </div>
        </div>
      </div>

      <!-- Telefon -->
      <div class="item" data-type="phone" tabindex="0" aria-pressed="false">
        <div class="icon" aria-hidden="true">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none">
            <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.86 19.86 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6A19.86 19.86 0 0 1 3.08 4.18 2 2 0 0 1 5 2h3a2 2 0 0 1 2 1.72c.12 1.21.37 2.4.72 3.53a2 2 0 0 1-.45 2.11L9.91 10.09a13.36 13.36 0 0 0 6 6l1.73-1.73a2 2 0 0 1 2.11-.45c1.13.35 2.32.6 3.53.72A2 2 0 0 1 22 16.92z" stroke="currentColor" stroke-width="1.1" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="label">
          <div class="name">Telefon</div>
          <div class="hint">+998 33 999 2011</div>
          <div class="detail hidden">
            <div id="phone-text">+998 33 999 2011</div>
            <div>
              <button class="small" onclick="callPhone(event)">Qo‘ng‘iroq</button>
              <button class="small" onclick="copyText(event,'+998339992011')">Nusxa</button>
            </div>
          </div>
        </div>
      </div>

    </div>

    <div class="footer">© 2025 · Furqatli Bro aloqa havolalari</div>
  </div>

<script>
document.querySelectorAll('.item').forEach(item=>{
  item.addEventListener('click', function(e){
    if(e.target.closest('button')) return;
    const detail = this.querySelector('.detail');
    const shown = !detail.classList.contains('hidden');
    document.querySelectorAll('.detail').forEach(d=>d.classList.add('hidden'));
    if(!shown) detail.classList.remove('hidden'); else detail.classList.add('hidden');
  });
});

function copyText(event, text){
  event.stopPropagation();
  navigator.clipboard.writeText(text).then(()=> showTemp(event.target,'Nusxa olindi'));
}
function showTemp(el,msg){
  const note=document.createElement('span');
  note.textContent=msg;
  note.style.position='absolute';
  note.style.transform='translateY(-40px)';
  note.style.background='rgba(0,0,0,0.6)';
  note.style.padding='6px 8px';
  note.style.borderRadius='6px';
  note.style.fontSize='12px';
  note.style.color='#fff';
  el.style.position='relative';
  el.appendChild(note);
  setTimeout(()=> note.remove(),1200);
}

function openIG(e){
  e.stopPropagation();
  const username="furqatli_bro";
  window.open(`https://instagram.com/${username}`,'_blank');
}
function openTG(e){
  e.stopPropagation();
  const username="furqatli_bro";
  window.open(`https://t.me/${username}`,'_blank');
}
function callPhone(e){
  e.stopPropagation();
  window.location.href='tel:+998339992011';
}
</script>
</body>
</html>
