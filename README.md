# -xiyanzxd.github.io
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Xiyanz X'D - Jubel Akun, Joki & Top Up Murah</title>
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
  body{font-family:'Poppins',sans-serif;background:#070a12;color:#f8fafc}
  .glow-blue{box-shadow:0 0 30px rgba(59,130,246,.35)} 
  .card-hover:hover{transform:translateY(-5px);border-color:#3b82f6}
</style>
</head>
<body>

<!-- HEADER -->
<header class="sticky top-0 z-50 bg-[#0b0f19]/80 backdrop-blur-xl border-b border-white/10">
  <div class="max-w-7xl mx-auto px-5 py-4 flex justify-between items-center">
    <h1 class="text-2xl font-black">XIYANZ <span class="text-blue-500">X'D</span></h1>
    <a href="https://wa.me/6285177480449" class="bg-blue-600 px-5 py-2 rounded-full font-bold text-sm glow-blue"><i class="fab fa-whatsapp mr-1"></i> 0851-7748-0449</a>
  </div>
</header>

<!-- HERO -->
<section class="max-w-7xl mx-auto px-5 py-12 text-center">
  <h2 class="text-4xl md:text-5xl font-black leading-tight">TOKO GAME <span class="text-blue-500">TERPERCAYA</span><br>AMUNTAI</h2>
  <p class="text-white/50 text-sm mt-3 max-w-2xl mx-auto">Jual Beli Akun, Joki Quest & Top Up Murah untuk 5 Game Meta. Proses Kilat & Garansi Full.</p>
  
  <div class="grid grid-cols-3 gap-3 max-w-2xl mx-auto mt-8">
    <div class="bg-[#121827] border border-white/10 p-4 rounded-2xl"><i class="fas fa-store text-blue-500 text-xl"></i><p class="font-bold text-sm mt-2">Jubel Akun</p></div>
    <div class="bg-white text-black p-4 rounded-2xl"><i class="fas fa-gamepad text-xl"></i><p class="font-bold text-sm mt-2">Joki Akun</p></div>
    <div class="bg-[#121827] border border-white/10 p-4 rounded-2xl"><i class="fas fa-coins text-blue-500 text-xl"></i><p class="font-bold text-sm mt-2">Top Up Murah</p></div>
  </div>
</section>

<!-- FILTER MENU -->
<div class="max-w-7xl mx-auto px-5">
  <p class="text-xs font-bold tracking-widest text-white/40 mb-3">PILIH LAYANAN:</p>
  <div class="flex gap-2 overflow-x-auto pb-2" id="service-filter">
    <button onclick="setService('all')" class="srv bg-white text-black px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Semua</button>
    <button onclick="setService('Jubel')" class="srv bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Jubel Akun</button>
    <button onclick="setService('Joki')" class="srv bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Joki Akun</button>
    <button onclick="setService('TopUp')" class="srv bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Top Up Murah</button>
  </div>
  <p class="text-xs font-bold tracking-widest text-white/40 mt-5 mb-3">PILIH GAME:</p>
  <div class="flex gap-2 overflow-x-auto pb-2" id="game-filter">
    <button onclick="setGame('all')" class="gm bg-blue-600 text-white px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Semua Game</button>
    <button onclick="setGame('Genshin')" class="gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Genshin Impact</button>
    <button onclick="setGame('HSR')" class="gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Honkai Star Rail</button>
    <button onclick="setGame('ZZZ')" class="gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">ZZZ</button>
    <button onclick="setGame('WuWa')" class="gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Wuthering Waves</button>
    <button onclick="setGame('MLBB')" class="gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap">Mobile Legends</button>
  </div>
</div>

<!-- PRODUK LIST -->
<section id="list" class="max-w-7xl mx-auto px-5 py-8 grid md:grid-cols-3 gap-5"></section>

<footer class="border-t border-white/10 py-8 text-center text-white/30 text-xs">© 2026 Xiyanz X'D • WA 0851-7748-0449 • Amuntai, Kalsel</footer>

<script>
const WA="6285177480449";
const produk=[
  // JUBEL AKUN
  {service:'Jubel', game:'Genshin', title:'Genshin - Neuvillette C6R5 + Furina C2', price:'Rp 1.450.000', tag:'ENDGAME', img:'https://images.unsplash.com/photo-1511512578047-dfb367046420?w=500'},
  {service:'Jubel', game:'HSR', title:'HSR - Acheron E6S5 + Sunday + Robin', price:'Rp 2.200.000', tag:'SULTAN', img:'https://images.unsplash.com/photo-1538481199705-c710c4e965fc?w=500'},
  {service:'Jubel', game:'ZZZ', title:'ZZZ - Miyabi M6 + Lighter + Yanagi', price:'Rp 950.000', tag:'META', img:'https://images.unsplash.com/photo-1493711662062-fa541adb3fc8?w=500'},
  {service:'Jubel', game:'WuWa', title:'WuWa - Camellya S6 + Shorekeeper S6', price:'Rp 850.000', tag:'FULL EXPLOR', img:'https://images.unsplash.com/photo-1542751371-adc38448a05e?w=500'},
  {service:'Jubel', game:'MLBB', title:'MLBB - 900 Skin, Legend 5, WR 78%', price:'Rp 1.800.000', tag:'SULTAN', img:'https://images.unsplash.com/photo-1542751110-97427bbecf20?w=500'},

  // JOKI AKUN
  {service:'Joki', game:'Genshin', title:'Joki Spiral Abyss 12-3 Full Star', price:'Rp 25.000', tag:'JOKI', img:'https://images.unsplash.com/photo-1518709268805-4e9042af9f23?w=500'},
  {service:'Joki', game:'Genshin', title:'Joki Eksplor 100% - 1 Region', price:'Rp 80.000', tag:'JOKI', img:'https://images.unsplash.com/photo-1518709268805-4e9042af9f23?w=500'},
  {service:'Joki', game:'HSR', title:'Joki Memory of Chaos Full Star', price:'Rp 30.000', tag:'JOKI', img:'https://images.unsplash.com/photo-1511512578047-dfb367046420?w=500'},
  {service:'Joki', game:'MLBB', title:'Joki Rank Epic ke Mythic', price:'Rp 150.000', tag:'JOKI', img:'https://images.unsplash.com/photo-1542751110-97427bbecf20?w=500'},

  // TOP UP
  {service:'TopUp', game:'Genshin', title:'6050 Genesis Crystal', price:'Rp 890.000', tag:'TOP UP', img:'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=500'},
  {service:'TopUp', game:'HSR', title:'8080 Oneiric Shard + Bonus', price:'Rp 1.250.000', tag:'TOP UP', img:'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=500'},
  {service:'TopUp', game:'MLBB', title:'1000 Diamond MLBB Fast', price:'Rp 240.000', tag:'TOP UP', img:'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=500'},
  {service:'TopUp', game:'WuWa', title:'1980 Lunite - WuWa', price:'Rp 310.000', tag:'TOP UP', img:'https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=500'},
];

let curService='all', curGame='all';
const listEl=document.getElementById('list');

function render(){
  listEl.innerHTML='';
  produk.filter(p=>(curService==='all'||p.service===curService)&&(curGame==='all'||p.game===curGame)).forEach(p=>{
    const waText=`Halo Xiyanz X'D, mau pesan ${p.service} - ${p.title} harga ${p.price}`;
    listEl.innerHTML+=`
    <div class="bg-[#121827] border border-white/10 rounded-[20px] overflow-hidden card-hover transition">
      <img src="${p.img}" class="w-full h-[180px] object-cover">
      <div class="p-5">
        <div class="flex justify-between items-center">
          <span class="text-[10px] font-black tracking-widest bg-white text-black px-3 py-1 rounded-full">${p.game}</span>
          <span class="text-[10px] font-bold text-blue-400">${p.tag}</span>
        </div>
        <h3 class="font-bold mt-3 leading-tight text-sm">${p.title}</h3>
        <p class="text-[11px] text-white/50 mt-1">${p.service} • Garansi Aman</p>
        <p class="text-xl font-black mt-3">${p.price}</p>
        <a href="https://wa.me/${WA}?text=${encodeURIComponent(waText)}" target="_blank" class="mt-4 block w-full bg-white text-black text-center py-3 rounded-full font-bold text-sm hover:bg-blue-600 hover:text-white transition">
          <i class="fab fa-whatsapp"></i> Pesan Sekarang
        </a>
      </div>
    </div>`;
  });
}
function setService(s){curService=s; document.querySelectorAll('#service-filter .srv').forEach(b=>b.className='srv bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap'); event.target.className='srv bg-white text-black px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap'; render();}
function setGame(g){curGame=g; document.querySelectorAll('#game-filter .gm').forEach(b=>b.className='gm bg-[#121827] border border-white/10 px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap'); event.target.className='gm bg-blue-600 text-white px-5 py-2 rounded-full text-sm font-bold whitespace-nowrap'; render();}
render();
</script>
</body>
</html>
